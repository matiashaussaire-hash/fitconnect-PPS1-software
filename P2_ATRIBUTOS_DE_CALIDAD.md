# 7. Atributos de Calidad

Los atributos de calidad describen cómo debe comportarse FitConnect, además de las funciones que debe ofrecer. Para este análisis se tomó como base el enunciado del proyecto y se consideró el relevamiento realizado con los stakeholders.

Es importante distinguir que algunos atributos aparecen de manera directa en el enunciado, mientras que otros se deducen de las características del sistema. La eficiencia se encuentra expresada mediante condiciones concretas; la usabilidad y la portabilidad surgen del problema y del contexto de uso; y la mantenibilidad y la seguridad son necesidades implícitas que posteriormente fueron confirmadas durante el relevamiento.

## 1. Usabilidad

**Atributo identificado:** facilidad de aprendizaje y operabilidad durante la configuración inicial y el comienzo de una rutina.

**Justificación del enunciado:** el enunciado señala que muchas personas desean entrenar, pero no saben por dónde empezar, y presenta a FitConnect como una solución accesible para personas con distintos niveles de condición física. Esto implica que la aplicación debe guiar al usuario con claridad y permitirle comprender rápidamente qué información ingresar, qué programa utilizar y cómo comenzar a entrenar.

El relevamiento permitió precisar esta necesidad: el proceso principal deberá realizarse mediante **registro mínimo, confirmación del programa recomendado e inicio de la rutina**, con un máximo de tres pasos principales y un tiempo inferior a tres minutos hasta el comienzo del primer entrenamiento.

**¿Por qué es importante para FitConnect?**

La dificultad para comenzar y el abandono temprano constituyen el principal problema priorizado del proyecto. Si el registro es extenso, la navegación resulta confusa o el usuario no comprende la rutina propuesta, es probable que abandone la aplicación antes de experimentar su valor.

## 2. Eficiencia (Performance)

**Atributo identificado:** tiempo de inicio reducido y utilización controlada de los recursos del dispositivo.

**Justificación del enunciado:** el enunciado establece expresamente que la aplicación debe iniciar en menos de tres segundos, ocupar menos de 200 MB y funcionar en dispositivos de gama media-baja. Estas condiciones corresponden al tiempo de respuesta y a la utilización de recursos, subcaracterísticas propias de la eficiencia.

**¿Por qué es importante para FitConnect?**

FitConnect incluirá videos, programas, seguimiento de entrenamientos, chat y videollamadas. Sin una administración eficiente de los recursos, estas funciones podrían provocar tiempos de carga elevados, un consumo excesivo de almacenamiento, memoria o batería y una experiencia deficiente en los dispositivos a los que se dirige el producto.

## 3. Mantenibilidad

**Atributo identificado:** modificabilidad del sistema mediante una organización modular que permita corregir o ampliar una función sin afectar innecesariamente a las demás.

**Justificación del enunciado:** la mantenibilidad no aparece formulada como una condición explícita o medible en el enunciado. Sin embargo, se desprende del alcance del producto, que reúne áreas funcionales diferentes, como marketplace de entrenadores, biblioteca de ejercicios, programas, seguimiento del progreso, comunidad, pagos y herramientas profesionales. Además, el proyecto prevé que FitConnect evolucione mediante distintos incrementos.

Esta necesidad fue considerada posteriormente en la arquitectura propuesta, donde el backend se organizó como un monolito modular y en capas para mantener separadas las distintas responsabilidades.

**¿Por qué es importante para FitConnect?**

El sistema deberá recibir correcciones, incorporar nuevas funciones y adaptarse a decisiones futuras. Una estructura mantenible permitirá realizar esos cambios con menor esfuerzo y riesgo de introducir errores en funcionalidades que ya se encuentren operativas.

## 4. Portabilidad

**Atributo identificado:** adaptabilidad de la aplicación a diferentes dispositivos y entornos móviles compatibles.

**Justificación del enunciado:** FitConnect se presenta como una plataforma móvil y se exige que funcione en dispositivos de gama media-baja. Esto requiere que la aplicación pueda instalarse y operar correctamente en equipos con diferentes capacidades de hardware y en las versiones de los sistemas operativos que el proyecto decida admitir.

El enunciado no especifica las versiones mínimas de Android e iOS ni los modelos que se utilizarán como referencia. Esa definición será necesaria para construir la matriz definitiva de pruebas, pero no impide identificar la portabilidad como atributo de calidad.

**¿Por qué es importante para FitConnect?**

La propuesta busca reducir barreras de acceso al entrenamiento. Si la aplicación solo funcionara correctamente en dispositivos recientes o de gama alta, excluiría a una parte de los usuarios a los que pretende alcanzar.

## 5. Seguridad

**Atributo identificado:** confidencialidad e integridad de la información personal y sensible administrada por la plataforma.

**Justificación del enunciado:** el enunciado no establece controles de seguridad concretos, pero indica que FitConnect registrará entrenamientos y progreso, almacenará fotos, gestionará perfiles de entrenadores certificados y procesará transacciones. Estas funciones implican el tratamiento de información personal, documentación y datos económicos que deben protegerse frente a accesos o modificaciones no autorizados.

Durante el relevamiento se confirmó la necesidad de aplicar cifrado en tránsito y en reposo, autorización por roles, auditoría, consentimientos y acceso limitado a los datos sensibles.

**¿Por qué es importante para FitConnect?**

Una falla de seguridad podría exponer información privada, alterar registros de entrenamiento, comprometer documentación profesional o afectar operaciones económicas. Además del posible impacto legal, esto perjudicaría directamente la confianza de usuarios y entrenadores en la plataforma.

## Otros atributos de calidad críticos para FitConnect

### Fiabilidad

La fiabilidad es crítica porque los usuarios necesitan consultar sus rutinas y registrar sus resultados aun cuando la conectividad sea limitada, mientras que las reservas, los pagos, el chat y las videollamadas requieren servicios centrales disponibles.

El relevamiento estableció como objetivos una disponibilidad mensual mínima del 99,5 %, conservación local de las operaciones pendientes, sincronización sin pérdida ni duplicación de información y mecanismos de recuperación ante fallos. También se definió que la videollamada no debe convertirse en un punto único de falla y debe contar con una alternativa cuando no pueda establecerse la conexión principal.

### Compatibilidad

La compatibilidad también resulta crítica debido a que FitConnect deberá intercambiar información con distintos componentes y proveedores: la aplicación móvil, el backend, el almacenamiento local, los servicios de pagos y las soluciones de videollamada.

Las integraciones deberán utilizar interfaces definidas y mantener el funcionamiento esperado aunque un proveedor presente un error. Esto permitirá cambiar o actualizar un servicio externo sin afectar innecesariamente al resto de la aplicación.

## Medición de los atributos de calidad

| Atributo | Indicadores o métricas | Forma de evaluación |
|---|---|---|
| **Usabilidad** | Tiempo hasta iniciar la primera rutina; cantidad de pasos principales; porcentaje de usuarios que completa el onboarding; tasa de finalización sin ayuda; cantidad de errores o dudas durante la tarea. | Realizar pruebas de prototipo con usuarios representativos. Verificar que el recorrido principal no supere tres pasos y que el usuario pueda comenzar a entrenar en menos de tres minutos. |
| **Eficiencia** | Tiempo de inicio en frío; tamaño de descarga e instalación; consumo de memoria, CPU y batería durante las funciones principales. | Ejecutar varias pruebas en dispositivos de referencia de gama media-baja y registrar los tiempos y consumos. El inicio deberá producirse en menos de tres segundos y la aplicación deberá respetar el límite de 200 MB. Para evitar la ambigüedad del enunciado, deberán registrarse por separado el tamaño descargado y el tamaño instalado. |
| **Mantenibilidad** | Cobertura de pruebas automatizadas; tiempo necesario para localizar y corregir un defecto; tiempo requerido para implementar un cambio; cantidad de módulos afectados por cada modificación; defectos de regresión. | Revisar las dependencias entre módulos, ejecutar pruebas unitarias y de integración y comparar el esfuerzo y los errores producidos en cada cambio. La cobertura deberá informarse como porcentaje, sin fijar un valor mínimo hasta que el equipo adopte formalmente ese criterio. |
| **Portabilidad** | Cantidad de sistemas operativos, versiones y dispositivos soportados; porcentaje de pruebas aprobadas en cada entorno; tasa de instalaciones correctas; cantidad de cambios específicos requeridos por plataforma. | Definir una matriz de dispositivos y versiones compatibles y ejecutar en cada combinación las pruebas de instalación, inicio y flujos críticos. Las versiones mínimas y los modelos de referencia deberán incorporarse cuando queden confirmados. |
| **Seguridad** | Cantidad y severidad de vulnerabilidades; porcentaje de datos sensibles cifrados; resultados de pruebas de autenticación y autorización; porcentaje de eventos críticos registrados por auditoría; accesos no autorizados detectados. | Realizar análisis de vulnerabilidades, pruebas de penetración y pruebas de permisos por rol. Verificar el cifrado de los datos en tránsito y en reposo, así como la integridad y trazabilidad de los registros sensibles. |
| **Fiabilidad** | Porcentaje mensual de disponibilidad; cantidad y duración de incidentes; tiempo medio de recuperación; operaciones offline perdidas o duplicadas; sincronizaciones fallidas; utilización de la alternativa de videollamada. | Utilizar monitoreo continuo, alertas, registros de incidentes y pruebas de recuperación. Verificar una disponibilidad mínima del 99,5 % y probar que las operaciones locales se sincronicen sin pérdidas ni duplicaciones. |
| **Compatibilidad** | Porcentaje de pruebas de integración aprobadas; errores en intercambios de información; webhooks procesados correctamente; conexiones de videollamada establecidas; activaciones correctas del mecanismo alternativo. | Ejecutar pruebas de contrato e integración con los servicios externos, simular indisponibilidad de proveedores y comprobar que los errores se registren y que las alternativas previstas funcionen. |

## Conclusión

Los atributos de calidad más directamente expresados por el enunciado son la eficiencia y la adaptabilidad a dispositivos móviles, mientras que la usabilidad surge del problema que FitConnect pretende resolver. La mantenibilidad y la seguridad no se presentan originalmente como requisitos medibles, pero resultan necesarias por la variedad de funciones, la evolución prevista y la información administrada por el sistema.

Además, la fiabilidad y la compatibilidad deben considerarse críticas debido al funcionamiento offline, la disponibilidad requerida y la dependencia de servicios externos. Para que estos atributos puedan verificarse, deberán asociarse con métricas concretas y evaluarse mediante pruebas, monitoreo y registros durante el desarrollo y la operación.

## Referencias

- Pressman, R. S. (2010). *Ingeniería del Software: Un Enfoque Práctico*. 7.ª edición. McGraw-Hill. Capítulo 9.
- Kendall, K. E. y Kendall, J. E. *Análisis y Diseño de Sistemas*. 8.ª edición. Capítulos 14 y 16.
- ISO/IEC 25010:2011. *Systems and Software Quality Requirements and Evaluation (SQuaRE)*. Secciones 4 y 6.

## Fuentes del proyecto

- Enunciado oficial del proyecto FitConnect.
- [SEGUIMIENTO.md](./SEGUIMIENTO.md).
