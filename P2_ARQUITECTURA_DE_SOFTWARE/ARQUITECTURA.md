
# 5. Arquitectura de Software




## Arquitectura propuesta

Para FitConnect se propone una **arquitectura cliente-servidor**, con un **backend monolítico modular organizado en capas**. Además, se utilizará procesamiento asíncrono mediante una cola de mensajes para aquellas operaciones que no necesiten resolverse inmediatamente.

La arquitectura combinará los siguientes estilos:

- **Cliente-servidor:** la aplicación móvil actuará como cliente y se comunicará con el servidor mediante una API REST sobre HTTPS.

- **Monolito modular:** el backend se implementará y desplegará como una sola aplicación, pero estará dividido internamente en módulos con responsabilidades claramente separadas.

- **Arquitectura en capas:** se separarán la presentación y la API, la lógica de negocio y el acceso a los datos.

- **Procesamiento asíncrono:** se utilizará una cola para notificaciones, sincronización de información, procesamiento de pagos, webhooks y otras tareas que no deban bloquear las solicitudes de los usuarios.


## ¿Por qué se eligió esta arquitectura para FitConnect?

Esta arquitectura fue elegida porque ofrece un equilibrio adecuado entre simplicidad, organización, rendimiento y posibilidades de crecimiento.

FitConnect se encuentra en la etapa de desarrollo de un MVP y se estima inicialmente un volumen aproximado de 15.000 usuarios activos. En este contexto, una arquitectura basada en microservicios agregaría complejidad de despliegue, comunicación, monitoreo y consistencia de datos sin aportar todavía un beneficio suficiente.

El monolito modular permite mantener un único despliegue y una única API, mientras que la división interna en módulos evita concentrar toda la lógica en componentes desorganizados. Cada módulo tendrá una responsabilidad específica y podrá evolucionar con cierto grado de independencia.

La arquitectura cliente-servidor permitirá centralizar:

- Las reglas de negocio.

- La autenticación y autorización.

- La gestión de usuarios y entrenadores.

- La verificación de identidad y credenciales.

- Los programas y entrenamientos.

- Las reservas y los pagos.

- Los consentimientos.

- La auditoría y la seguridad.

La organización en capas evitará que la aplicación móvil acceda directamente a la base de datos central. Todas las operaciones deberán pasar por la API y por la lógica de negocio correspondiente.


## ¿Qué características del proyecto hacen apropiada esta arquitectura?

Las principales características de FitConnect que justifican esta elección son:

1. **Aplicación móvil con servicios centralizados**

  Los usuarios y entrenadores utilizarán una aplicación móvil que necesitará acceder a información compartida, como perfiles, programas, ejercicios, reservas, mensajes y pagos.

2. **Funcionamiento offline-first**

  La aplicación deberá permitir registrar entrenamientos sin conexión. Para ello, utilizará una base de datos SQLite local y sincronizará posteriormente las operaciones con el servidor.

3. **Diversidad de funcionalidades**

  El backend deberá organizarse en módulos relacionados con:

  - Autenticación.

  - Usuarios.

  - Entrenadores.

  - Verificaciones.

  - Ejercicios.

  - Programas.

  - Entrenamientos.

  - Progreso.

  - Reservas.

  - Chat.

  - Videollamadas.

  - Pagos.

  - Notificaciones.

  - Consentimientos.

  - Auditoría.

  - Sincronización offline.

4. **Necesidad de consistencia y trazabilidad**

  Los registros de entrenamiento, las modificaciones de programas, las reservas, los pagos, los reembolsos, las verificaciones y los consentimientos deberán conservar un historial verificable.

5. **Tratamiento de información sensible**

  FitConnect administrará datos personales, datos relacionados con la salud y documentación de los entrenadores. Por este motivo, necesita reglas de acceso centralizadas, cifrado, auditoría y autorización por roles.

6. **Integración con servicios externos**

  El sistema utilizará servicios especializados como Stripe para pagos, WebRTC con servidores STUN/TURN para videollamadas y Zoom como alternativa ante fallos de conexión.

7. **Necesidad de disponibilidad y recuperación**

  El sistema deberá mantener una disponibilidad mensual mínima del 99,5 %, utilizar copias de seguridad y contar con mecanismos de monitoreo, alertas y recuperación.


## Diagrama de arquitectura de alto nivel

El diagrama de alto nivel deberá representar los siguientes componentes:

- Aplicación móvil.

- Base de datos local SQLite.

- API REST sobre HTTPS.

- Backend monolítico modular.

- Base de datos PostgreSQL.

- Redis para caché y coordinación.

- Cola de tareas asíncronas.

- Almacenamiento de objetos.

- CDN para contenido multimedia.

- Stripe para pagos y reembolsos.

- WebRTC con servidores STUN/TURN.

- Zoom como alternativa para videollamadas.

- Servicios de monitoreo, auditoría y alertas.

El diagrama será incorporado posteriormente en esta sección.

## ¿Qué ventajas aporta esta arquitectura al proyecto?

### Simplicidad inicial

El monolito modular es más sencillo de desarrollar, probar y desplegar que una arquitectura basada en microservicios.

### Separación de responsabilidades

La división en módulos y capas permite organizar el sistema según las diferentes áreas funcionales de FitConnect.

### Centralización de las reglas de negocio

La autenticación, los permisos, los pagos, las reservas, los consentimientos y las verificaciones pueden controlarse desde el servidor.

### Consistencia de los datos

La utilización de PostgreSQL como base de datos principal facilita el manejo de transacciones y relaciones entre usuarios, entrenadores, programas, reservas y pagos.

### Compatibilidad con el funcionamiento offline

SQLite permite almacenar información y operaciones pendientes en el dispositivo para sincronizarlas cuando se recupere la conexión.

### Integración controlada con proveedores externos

Los servicios de pagos, videollamadas, notificaciones y almacenamiento pueden integrarse mediante módulos específicos, evitando que su lógica se mezcle con el resto del sistema.

### Posibilidad de crecimiento

Aunque el backend se despliegue inicialmente como una sola aplicación, la separación modular permitirá extraer determinados módulos como servicios independientes si el crecimiento futuro lo justifica.

### Facilidad para realizar pruebas y detectar errores

La organización en capas y módulos facilita la realización de pruebas sobre la lógica de negocio y permite identificar con mayor claridad dónde se produce un problema.

## ¿Qué desventajas o desafíos presenta?

### Escalado conjunto

Al tratarse de un único despliegue, inicialmente se escalará toda la aplicación aunque solamente un módulo necesite más recursos.

### Riesgo de acoplamiento interno

Si no se respetan los límites entre módulos, el monolito puede volverse difícil de mantener y evolucionar.

### Impacto de los fallos

Un error grave dentro del backend podría afectar varias funcionalidades del sistema. Para reducir este riesgo será necesario implementar monitoreo, manejo de errores y pruebas adecuadas.


### Dependencia de la conectividad

Aunque los entrenamientos podrán registrarse sin conexión, otras funciones como reservas, pagos, chat y videollamadas necesitarán acceso a Internet.

### Complejidad de la sincronización offline

Será necesario controlar identificadores únicos, versiones, reintentos e idempotencia para evitar pérdidas o duplicaciones de registros.

### Dependencia de proveedores externos

Las fallas de servicios como Stripe, TURN o Zoom pueden afectar determinadas funciones. El sistema deberá registrar los errores, reintentar las operaciones y proporcionar alternativas cuando corresponda.

### Disciplina en el diseño modular

El equipo deberá mantener interfaces y responsabilidades claras para impedir que los módulos accedan directamente a información o funciones que no les corresponden.

## Conclusión

La arquitectura más apropiada para FitConnect es una arquitectura cliente-servidor con un backend monolítico modular organizado en capas y complementado con procesamiento asíncrono.

Esta alternativa responde adecuadamente al alcance del MVP, permite implementar las funcionalidades necesarias sin incorporar la complejidad prematura de los microservicios y mantiene una estructura que puede evolucionar si el crecimiento futuro del producto lo requiere.

## Referencias

- Bass, L., Clements, P. y Kazman, R. (2013). *Software Architecture in Practice*. 3.ª ed. Addison-Wesley. Capítulos 1, 3, 4 y 5.

- Pressman, R. S. (2010). *Ingeniería del Software: Un Enfoque Práctico*. 7.ª ed. McGraw-Hill. Capítulos 3, 8 y 9.

- Richards, M. y Ford, N. (2020). *Fundamentals of Software Architecture*. O’Reilly. Capítulos 2, 3 y 14.

## Fuente de la información relevada

- [SEGUIMIENTO.md](./SEGUIMIENTO.md), especialmente la consulta respondida por Diego el 30/09/2026.