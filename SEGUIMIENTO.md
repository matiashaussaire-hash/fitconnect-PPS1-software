

# Conversación con Gabriel (Product Manager)

  

**Fecha de la consulta:** 15/06/2026

**Fecha de respuesta:** 16/06/2026

**Participantes:** Equipo 6 – Gabriel (Product Manager)

  

## Consulta realizada

  

Hola Gabriel, buenas tardes.

  

Somos el Grupo 6 y nos encontramos realizando el análisis inicial del proyecto **FitConnect**.

  

Nos gustaría conocer su visión como Product Manager sobre los problemas que dieron origen a la plataforma. A partir de la lectura del enunciado identificamos inicialmente los siguientes:

  

### 1. Limitaciones de tiempo y espacio

  

-  **Descripción del problema:** Muchas personas tienen horarios de trabajo, estudio u otras actividades que les dificultan asistir regularmente a un gimnasio o coordinar entrenamientos presenciales.

-  **¿A quién afecta?** A personas que desean ejercitarse pero no disponen de horarios compatibles con gimnasios o entrenadores.

-  **¿Cómo FitConnect resuelve este problema?** Permite acceder a rutinas, programas y material de entrenamiento desde cualquier lugar y en cualquier momento.

  

### 2. Costos elevados de entrenamiento

  

-  **Descripción del problema:** Algunas personas no pueden afrontar el costo de una membresía de gimnasio o de un entrenador personal.

-  **¿A quién afecta?** A personas con recursos económicos limitados que desean realizar actividad física.

-  **¿Cómo FitConnect resuelve este problema?** Ofrece una modalidad **freemium** con acceso gratuito a parte del contenido y programas básicos de entrenamiento.

  

### 3. Limitación geográfica para entrenadores

  

-  **Descripción del problema:** Los entrenadores de calistenia suelen depender de clientes de su zona geográfica o de un gimnasio determinado, lo que limita sus oportunidades de crecimiento profesional.

-  **¿A quién afecta?** A entrenadores y profesionales de la calistenia.

-  **¿Cómo FitConnect resuelve este problema?** Les permite ofrecer programas y sesiones personalizadas a usuarios de distintas ubicaciones.

  

También le consultamos:

  

1. ¿Considera que estos son los principales problemas que busca resolver FitConnect?

2. ¿Hay algún problema importante que no hayamos identificado?

3. Si tuviera que priorizarlos, ¿en qué orden lo haría y por qué?

  

---

  

## Respuesta de Gabriel

  

Gabriel indicó que los problemas planteados por el equipo son reales, pero aclaró que existe uno aún más importante: **el abandono de los usuarios**.

  

Explicó que el principal desafío del proyecto es reducir la fricción durante el proceso de incorporación, ya que una gran cantidad de usuarios abandona la aplicación durante las primeras semanas. Por ese motivo, estableció como objetivo prioritario que un usuario pueda configurar su perfil y comenzar una rutina con un entrenador **en menos de tres pasos**, reduciendo al mínimo la barrera de entrada.

  

En función de esto, propuso el siguiente orden de prioridad para el MVP:

  

1.  **Reducir la fricción de inicio y mejorar la adherencia del usuario.**

2.  **Facilitar el acceso mediante un modelo freemium**, ofreciendo programas gratuitos y una biblioteca de ejercicios.

3.  **Permitir entrenar en cualquier momento y lugar**, eliminando la necesidad de gimnasios y equipamiento.

4.  **Brindar oportunidades de crecimiento a los entrenadores**, ampliando su alcance geográfico, aunque aclaró que esto depende primero de contar con una base suficiente de usuarios activos.

  

Además, señaló un aspecto que el equipo no había considerado inicialmente: **la necesidad de generar confianza mediante la verificación de los entrenadores**. Indicó que este tema debía profundizarse con **Mara (Legal)**, ya que la plataforma necesita validar la identidad y la documentación de quienes ofrecen sus servicios.

  

También aclaró que algunas funcionalidades propuestas, como la incorporación de nutrición o informes avanzados para entrenadores, **no forman parte del MVP** y fueron planificadas para una segunda fase del proyecto.

  

Finalmente, nos orientó hacia otros stakeholders según cada temática:

  

-  **Mara (Legal):** verificación de entrenadores y aspectos legales.

-  **Ana (Head de Entrenadores):** proceso de verificación y esquema de comisiones.

-  **Diego (CTO / DevOps):** arquitectura, sensores y decisiones técnicas.

  

---

  

## Impacto en el proyecto

  

Esta conversación permitió:

  

- Replantear completamente el **Punto 2 – Identificación de Problemas**.

- Incorporar el concepto de **onboarding con baja fricción** como prioridad del producto.

- Comprender que el principal objetivo del MVP es mejorar la **retención de usuarios**.

- Detectar la necesidad de entrevistar posteriormente a **Mara**, **Ana** y **Diego** para profundizar aspectos legales, funcionales y técnicos del proyecto.
# Conversación con Mara (Legal - Risk & Insurance)

  

**Fecha de la consulta:** 17/06/2026

**Fecha de respuesta:** 19/06/2026

**Participantes:** Equipo 6 – Mara (Legal / Risk & Insurance)

  

## Consulta realizada

  

Hola Mara, buenas tardes.

  

Somos el Grupo 6 y nos encontramos realizando el análisis inicial del proyecto **FitConnect**.

  

Durante una entrevista con Gabriel surgió que uno de los aspectos fundamentales para el crecimiento de la plataforma es generar confianza entre los usuarios y los entrenadores. En particular, nos comentó que la verificación de identidad y de los certificados de los entrenadores será un requisito clave para que la plataforma resulte confiable.

  

A partir de esto, identificamos preliminarmente que, antes de habilitar a un entrenador para ofrecer sus servicios, sería necesario validar su identidad y la documentación que acredite su formación.

  

Nos gustaría conocer su perspectiva sobre este proceso.

  

### Consultas

  

1. ¿Considera que la validación de identidad y de certificados profesionales es suficiente para generar confianza en la plataforma o existen otros aspectos que deberíamos contemplar?

  

2. ¿Qué tipo de documentación o verificaciones considera indispensables antes de habilitar a un entrenador dentro de FitConnect?

  

3. Desde el punto de vista legal y de gestión del riesgo, ¿qué aspectos debería tener en cuenta el equipo de desarrollo al diseñar este proceso de verificación?

  

---

  

## Respuesta de Mara

  

Mara explicó que la validación de identidad y de certificados **es necesaria, pero no suficiente** para garantizar la confianza en la plataforma.

  

Indicó que la confianza jurídica de FitConnect debe apoyarse en tres pilares fundamentales:

  

-  **Verificación documental con trazabilidad**, distinguiendo claramente entre certificaciones verificadas y credenciales auto declaradas (*self-report*).

-  **Aceptación expresa de los Términos y Condiciones de Uso (TOS)** antes de iniciar cualquier sesión de entrenamiento, mediante una pantalla de aceptación obligatoria.

-  **Consentimiento informado para el tratamiento de datos sensibles**, ya que la plataforma administrará información relacionada con la salud y la actividad física de los usuarios, debiendo cumplir normativas como **HIPAA** y **GDPR**.

  

Respecto al proceso de habilitación de entrenadores, indicó que como mínimo deberían solicitarse:

  

- Verificación de identidad mediante documento vigente.

- Certificados o títulos emitidos por instituciones reconocidas.

- Identificación explícita de las credenciales verificadas y de aquellas solamente declaradas por el entrenador.

- Aceptación de un acuerdo específico para entrenadores con obligaciones y limitaciones de responsabilidad.

  

Además, recomendó incorporar desde el diseño del sistema diversas medidas para disminuir el riesgo legal, entre ellas:

  

- Pantalla obligatoria de exoneración de responsabilidad antes de cada entrenamiento.

- Consentimiento independiente para el tratamiento de datos sensibles.

- Registro de auditoría de todo el proceso de verificación.

- Cifrado de la documentación personal almacenada.

- Posibilidad de suspender inmediatamente a un entrenador ante documentación fraudulenta o incumplimientos.

- Videollamadas protegidas mediante cifrado de extremo a extremo.

  

Finalmente, remarcó que la verificación documental constituye únicamente el punto de partida y que todas estas salvaguardas deben incorporarse desde el diseño de la plataforma.

  

---

  

## Impacto en el proyecto

  

Esta conversación permitió:

  

- Definir los requisitos legales asociados al proceso de incorporación y verificación de entrenadores.

- Identificar requisitos no funcionales relacionados con la seguridad, privacidad y protección de datos.

- Incorporar conocimientos técnicos vinculados a normativas de protección de datos, gestión del riesgo y trazabilidad documental.

- Comprender la importancia de diseñar el sistema contemplando el cumplimiento legal desde las primeras etapas del desarrollo.

- Fundamentar decisiones tomadas en los puntos de **Conocimientos**, **Problemas** y **Roles** del trabajo práctico.






# Conversación con Diego (CTO / DevOps)

  

**Fecha de la consulta:** 20/06/2026

**Fecha de respuesta:** 23/06/2026

**Participantes:** Equipo 6 – Diego (CTO / DevOps)

  

## Consulta realizada

  

Hola Diego, buenas tardes.

  

Somos el Grupo 6 y nos encontramos realizando el análisis inicial del proyecto **FitConnect**.

  

Durante las entrevistas con Gabriel y Mara fueron surgiendo distintos requisitos que creemos pueden influir en las decisiones técnicas del proyecto. Entre ellos identificamos que la aplicación deberá:

  

- Iniciar en menos de 3 segundos.

- Ocupar menos de 200 MB.

- Funcionar correctamente en dispositivos de gama media-baja.

- Almacenar de forma segura documentación de entrenadores y datos personales sensibles.

- Registrar el proceso de verificación de entrenadores.

- Permitir videollamadas entre usuarios y entrenadores.

  

A partir de estos requisitos, suponemos que será necesario investigar aspectos relacionados con la optimización del rendimiento en aplicaciones móviles, el almacenamiento seguro de información, el manejo de contenido multimedia y la arquitectura del sistema.

  

Consultamos:

  

1. ¿Considera que estos son los principales desafíos técnicos del proyecto o existen otros aspectos que deberíamos contemplar desde las primeras etapas del desarrollo?

  

2. ¿Qué decisiones de arquitectura o qué áreas de conocimiento técnico considera importante definir o investigar al inicio del proyecto para poder cumplir con estos requisitos y permitir que la plataforma pueda crecer en el futuro?

  

---

  

## Respuesta de Diego

  

Diego confirmó que los requisitos identificados por el equipo representan los pilares técnicos del MVP, pero señaló otros desafíos que considera fundamentales desde el comienzo del proyecto.

  

Como prioridades de infraestructura destacó:

  

- Garantizar un **99,5 % de disponibilidad (uptime)** de la plataforma.

- Implementar un funcionamiento **offline-first**, utilizando SQLite local y un mecanismo de reintentos para sincronizar la información cuando el dispositivo recupere conexión.

- Incorporar un mecanismo de respaldo para las videollamadas, utilizando **WebRTC** como solución principal y un enlace de Zoom como alternativa en caso de fallos.

  

También aclaró que algunas funcionalidades, como el seguimiento mediante sensores (acelerómetro) y la gamificación avanzada, **no forman parte del MVP**, ya que incrementarían considerablemente la complejidad del sistema. Estas funcionalidades quedaron previstas para versiones posteriores.

  

Respecto a la arquitectura del sistema, recomendó investigar y definir desde el inicio aspectos como:

  

- Arquitectura desacoplada mediante separación de servicios.

- Estrategias de replicación de bases de datos y copias de seguridad.

- Cifrado de datos en reposo y en tránsito, considerando desde el diseño el cumplimiento de normativas como HIPAA y GDPR.

- Infraestructura necesaria para videollamadas mediante WebRTC y servidores TURN/STUN.

- Estrategias de sincronización offline-first y resolución de conflictos entre datos locales y remotos.

- Uso de redes de distribución de contenido (CDN) y técnicas de compresión para optimizar la carga de imágenes y videos.

- Implementación de herramientas de observabilidad mediante registros centralizados, métricas y alertas.

  

Finalmente, recomendó diseñar la arquitectura contemplando el crecimiento futuro mediante **feature flags**, permitiendo incorporar nuevas funcionalidades en etapas posteriores sin afectar la estabilidad del sistema.

  

---

  

## Impacto en el proyecto

  

Esta conversación permitió:

  

- Identificar los principales desafíos técnicos asociados al desarrollo del MVP.

- Definir conocimientos técnicos relacionados con arquitectura de software, sincronización offline, seguridad de la información y escalabilidad.

- Comprender qué funcionalidades forman parte del MVP y cuáles fueron planificadas para fases posteriores.

- Fundamentar la elección del **Modelo Incremental**, ya que la arquitectura propuesta acompaña un crecimiento por etapas claramente definidas.

- Complementar los requisitos no funcionales del proyecto relacionados con rendimiento, disponibilidad, seguridad y mantenibilidad.



# Conversación con Ana (Head de Entrenadores)

  

**Fecha de la consulta:** 26/06/2026

**Fecha de respuesta:** 26/06/2026

**Participantes:** Equipo 6 – Ana (Head de Entrenadores)

  

## Consulta realizada

  

Hola Ana, buenas tardes.

  

Somos el Grupo 6 y nos encontramos realizando el análisis inicial del proyecto **FitConnect**.

  

Durante las entrevistas con Gabriel, Mara y Diego fuimos conociendo distintos aspectos del proyecto desde la perspectiva del producto, los requisitos legales y las decisiones técnicas. Nos gustaría ahora comprender mejor las necesidades de los entrenadores que utilizarán la plataforma.

  

Sabemos que FitConnect permitirá a los entrenadores crear programas de entrenamiento, ofrecer sesiones personalizadas y gestionar sus servicios dentro de la aplicación. Para poder diseñar correctamente esas funcionalidades, nos gustaría conocer su punto de vista.

  

### Consultas

  

1. ¿Qué información considera indispensable que un entrenador pueda registrar o administrar dentro de FitConnect para poder trabajar de forma cómoda y eficiente?

  

2. Desde su experiencia, ¿qué funcionalidades deberían estar presentes en el MVP para que un entrenador considere útil la plataforma desde el primer día?

  

3. Al momento de diseñar los programas de entrenamiento, ¿existen criterios, metodologías o material de referencia que el equipo de desarrollo debería conocer para comprender cómo trabajan habitualmente los entrenadores?

  

---

  

## Respuesta de Ana

  

Ana explicó que el principal objetivo de la plataforma debe ser permitir que los entrenadores trabajen de forma cómoda y eficiente.

  

Respecto a la información que deberían administrar, indicó que resulta indispensable contar con:

  

- Perfil completo del cliente (datos antropométricos, historial de lesiones, experiencia, objetivos y disponibilidad).

- Gestión de programas de entrenamiento personalizados.

- Seguimiento del progreso de cada cliente mediante métricas y evolución.

- Administración de pagos, comisiones y calificaciones.

- Calendario de disponibilidad y reservas.

  

En relación con el MVP, consideró imprescindibles funcionalidades como:

  

- Constructor de rutinas (*drag-and-drop*).

- Biblioteca de ejercicios con filtros.

- Plantillas reutilizables.

- Registro y seguimiento de clientes.

- Chat y videollamadas integradas.

- Calendario de reservas.

- Panel de ingresos y comisiones.

- Sistema de feedback y calificaciones posteriores a cada sesión.

  

Finalmente, destacó que el equipo de desarrollo debería conocer diversos conceptos propios del entrenamiento para comprender las necesidades de los entrenadores y diseñar correctamente la plataforma. Entre ellos mencionó:

  

- Principios de progresión del entrenamiento (sobrecarga progresiva, volumen, intensidad y frecuencia).

- Organización de una sesión de entrenamiento.

- Periodización mediante mesociclos.

- Evaluaciones físicas iniciales y periódicas.

- Adaptación de ejercicios según lesiones o limitaciones del usuario.

  

Como material de referencia recomendó consultar:

  

-  **Overcoming Gravity**, de Steven Low.

-  **Periodization: Theory and Methodology of Training**, de Bompa & Buzzichelli.

- Las plataformas **TrainHeroic** y **TrueCoach**, utilizadas por entrenadores para la gestión de programas de entrenamiento.

  

---

  

## Impacto en el proyecto

  

Esta conversación permitió:

  

- Identificar los requisitos funcionales necesarios para que los entrenadores puedan utilizar la plataforma de forma eficiente.

- Comprender las funcionalidades mínimas que debería ofrecer el MVP desde la perspectiva de los entrenadores.

- Obtener referencias bibliográficas y metodológicas utilizadas posteriormente para fundamentar los **conocimientos científicos** del trabajo práctico.

- Entender que el equipo de desarrollo no necesita ser experto en entrenamiento, pero sí conocer cómo trabajan los entrenadores para diseñar herramientas que respondan a sus necesidades.

- Complementar la información obtenida previamente con Gabriel, Mara y Diego, incorporando la visión del principal usuario profesional de la plataforma.




# Conversación con Gabriel (Product Manager)

  

**Fecha de la consulta:** 02/07/2026

**Fecha de respuesta:** 02/07/2026

**Participantes:** Equipo 6 – Gabriel (Product Manager)

  

## Consulta realizada

  

Hola Gabriel, buenas tardes.

  

Somos el Grupo 6. Luego de las entrevistas que mantuvimos con usted, Ana, Diego y Mara, armamos una propuesta preliminar del equipo de desarrollo que consideramos necesario para llevar adelante el proyecto **FitConnect**.

  

La propuesta fue la siguiente:

  

- 2 Analistas Funcionales.

- 1 Diseñador UX/UI.

- 2 Desarrolladores Front-end Mobile.

- 2 Desarrolladores Back-end.

- 1 QA (Tester).

- 1 DevOps.

  

La idea fue definir estos roles teniendo en cuenta las necesidades identificadas durante las entrevistas. Consideramos importante contar con analistas funcionales para el relevamiento de requisitos; un diseñador UX/UI para minimizar la fricción durante el onboarding; desarrolladores front-end y back-end para implementar las funcionalidades de la plataforma; un QA para validar el correcto funcionamiento del sistema; y un DevOps para garantizar el rendimiento, la disponibilidad y la infraestructura de la aplicación.

  

Consultamos:

  

1. ¿Considera que esta propuesta cubre adecuadamente las necesidades del proyecto?

2. ¿Agregaría, quitaría o modificaría algún rol?

3. ¿La cantidad de personas asignadas a cada rol le parece razonable para un proyecto con las características de FitConnect?

  

---

  

## Respuesta de Gabriel

  

Gabriel consideró que la propuesta era adecuada como punto de partida, aunque realizó algunos ajustes.

  

En primer lugar, indicó que **no considera necesario contar con dos analistas funcionales**, ya que la visión del producto, el roadmap y las prioridades del MVP ya se encuentran definidas. Por este motivo, un único analista funcional resulta suficiente para acompañar el desarrollo.

  

También destacó la importancia de la **seguridad y el cumplimiento normativo**, señalando que al menos uno de los desarrolladores Back-end o el DevOps debe contar con conocimientos sobre protección de datos sensibles y normativas como **HIPAA** y **GDPR**, además de los mecanismos de cifrado y verificación documental mencionados durante las entrevistas con Mara y Diego.

  

Por último, remarcó que FitConnect es una **aplicación móvil**, por lo que los desarrolladores Front-end deben poseer experiencia en desarrollo mobile nativo o mediante tecnologías multiplataforma como **React Native** o **Flutter**. Señaló que la experiencia exclusiva en aplicaciones web no sería suficiente para cumplir con los requisitos técnicos del proyecto.

  

Finalmente, confirmó que, con esos ajustes, la cantidad total de roles propuesta resulta adecuada para el desarrollo del MVP.

  

---

  

## Impacto en el proyecto

  

Esta conversación permitió:

  

- Validar la propuesta del equipo de desarrollo elaborada por el grupo.

- Ajustar la cantidad de analistas funcionales necesarios para el proyecto.

- Incorporar la necesidad de experiencia en seguridad y protección de datos dentro del equipo técnico.

- Confirmar que el desarrollo Front-end debe estar orientado específicamente a aplicaciones móviles.

- Fundamentar la composición final del equipo presentada en el **Punto 4 – Roles en el Equipo de Desarrollo**.


# Conversación con Gabriel (Product Manager)

  

**Fecha de la consulta:** 06/07/2026

**Fecha de respuesta:** 06/07/2026

**Participantes:** Equipo 6 – Gabriel (Product Manager)

  

## Consulta realizada

  

Hola Gabriel, buenas tardes.

  

Somos el Grupo 6 y nos encontramos analizando los distintos modelos de proceso que podrían utilizarse para desarrollar **FitConnect**.

  

Observamos que gran parte de las funcionalidades del proyecto fueron planificadas para distintas etapas (MVP, Fase 2 y futuras versiones), lo que nos hizo pensar que un **Modelo Incremental** podría adaptarse adecuadamente al desarrollo.

  

Sin embargo, también vimos que durante el relevamiento fueron apareciendo nuevos requisitos y prioridades, lo que podría justificar la utilización de un modelo ágil.

  

Por este motivo, le consultamos:

  

**¿Cuál considera que representa mejor la estrategia de desarrollo del proyecto y por qué?**

  

---

  

## Respuesta de Gabriel

  

Gabriel respondió que el **Modelo Incremental** representa claramente la estrategia de desarrollo de FitConnect.

  

Explicó que los cambios observados por el equipo ocurrieron durante el **relevamiento de requisitos** y no durante el desarrollo del software. Una vez definido el MVP, el alcance de esa versión queda establecido y no se modifica durante su implementación.

  

Indicó que el MVP posee un alcance concreto, compuesto por funcionalidades como la biblioteca de ejercicios, programas de entrenamiento, seguimiento manual y chat. Una vez entregado ese incremento, se evaluarán las métricas obtenidas antes de decidir la incorporación de nuevas funcionalidades.

  

También aclaró que los requisitos surgidos posteriormente durante el relevamiento no alteran el alcance del MVP, sino que pasan a formar parte del backlog de futuras versiones, como la Fase 2.

  

Finalmente, explicó que aunque cada incremento pueda desarrollarse mediante sprints, **los sprints constituyen una herramienta de ejecución y no el modelo de proceso**. Según su criterio, el modelo utilizado sigue siendo Incremental, ya que cada versión posee un alcance definido y las nuevas funcionalidades se incorporan únicamente en incrementos posteriores.

  

---

  

## Impacto en el proyecto

  

Esta conversación permitió:

  

- Validar la elección del **Modelo Incremental** como proceso de desarrollo para FitConnect.

- Comprender la diferencia entre un **modelo de proceso** y las **metodologías utilizadas para ejecutar el desarrollo**.

- Justificar que los cambios detectados durante el relevamiento no modifican el alcance del MVP, sino que se incorporan en incrementos futuros.

- Fundamentar la respuesta correspondiente al **Punto 3 – Modelos de Proceso** del trabajo práctico.
