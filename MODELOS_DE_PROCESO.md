
# 3. Modelos de Proceso

| Modelo de Proceso            | Ventaja para FitConnect                                                                                                                                                          | Desventaja para FitConnect                                                                                                                                                               |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Modelo Cascada**           | Permite una planificación y documentación completa antes de comenzar el desarrollo, lo que resulta útil para organizar requisitos técnicos y legales.                            | Presenta poca flexibilidad ante cambios. Durante el relevamiento surgieron nuevos requisitos aportados por distintos stakeholders, por lo que este modelo dificultaría su incorporación. |
| **Modelo en V**              | Favorece la validación y verificación de cada etapa del desarrollo, aspecto importante para los requisitos legales y de seguridad identificados en FitConnect.                   | Requiere que los requisitos estén claramente definidos desde el inicio y resulta poco flexible frente a nuevas necesidades.                                                              |
| **Modelo Incremental**       | Permite desarrollar primero un MVP con las funcionalidades esenciales e incorporar nuevas funcionalidades en versiones posteriores sin retrasar la entrega inicial del producto. | Requiere una buena planificación de cada incremento para evitar dependencias o retrabajos entre versiones.                                                                               |
| **Modelo Iterativo**         | Permite mejorar progresivamente las funcionalidades utilizando el feedback obtenido de los usuarios durante el desarrollo.                                                       | Algunas funcionalidades pueden requerir varias revisiones antes de alcanzar su versión definitiva, aumentando el esfuerzo del equipo.                                                    |
| **Modelo de Prototipos**     | Facilita validar con los usuarios la interfaz, el proceso de registro y la experiencia de uso antes de desarrollar el producto definitivo.                                       | Los usuarios pueden interpretar el prototipo como una versión terminada del sistema, generando expectativas incorrectas.                                                                 |
| **Modelo en Espiral**        | Permite identificar y gestionar riesgos técnicos, legales y de seguridad desde las primeras etapas del proyecto.                                                                 | Es un modelo complejo y costoso de implementar para un proyecto como FitConnect.                                                                                                         |
| **Modelo Ágil (Scrum / XP)** | Favorece la organización del trabajo en equipo, la comunicación con el cliente y la entrega frecuente de software funcional durante el desarrollo.                               | No define por sí mismo la planificación de las distintas versiones del producto, por lo que debe complementarse con una estrategia de desarrollo.                                        |

## ¿Qué modelo de proceso recomendaríamos para FitConnect y por qué?

Recomendamos utilizar el **Modelo Incremental**.

Durante el relevamiento realizado con los distintos stakeholders y, especialmente, a partir de la entrevista con **Gabriel (Product Manager)**, se confirmó que la estrategia del proyecto consiste en desarrollar un **MVP** con un conjunto de funcionalidades claramente definidas (biblioteca de ejercicios, programas de entrenamiento, seguimiento manual y chat) y, una vez validado su funcionamiento mediante métricas de uso, incorporar nuevas funcionalidades en versiones posteriores, como inteligencia artificial, integración con wearables o gamificación.

Gabriel explicó que los cambios surgidos durante el relevamiento no modifican el alcance del MVP, sino que se incorporan al backlog de futuras versiones. De esta manera, cada incremento posee un alcance definido y se entrega como una versión funcional del producto.

Asimismo, indicó que **los sprints constituyen una herramienta de ejecución utilizada dentro de cada incremento**, pero que **el modelo de proceso adoptado por FitConnect es Incremental**, ya que el desarrollo se organiza en versiones sucesivas con objetivos y alcance previamente establecidos.

## ¿Qué factores del proyecto influyeron en esta decisión?

Los principales factores fueron:

- La existencia de un **MVP** con alcance claramente definido.
- La planificación explícita de funcionalidades para futuras versiones (Fase 2 y posteriores).
- La necesidad de entregar una versión funcional en el menor tiempo posible para validar la aceptación del producto.
- La incorporación de nuevas funcionalidades únicamente en incrementos posteriores, evitando modificar el alcance de la versión en desarrollo.
- La confirmación del Product Manager de que la estrategia de desarrollo del proyecto es incremental y que los sprints se utilizan únicamente como mecanismo de ejecución de cada incremento.

**Fuente de esta decisión:** [2026_07_06_Gabriel_Modelo_procesos.md](./2026_07_06_Gabriel_Modelo_procesos.md)
