# 1. Técnicas de Recolección de Requisitos

Para obtener los requisitos de FitConnect seleccionamos las técnicas de **entrevista** y **prototipado**. La entrevista ya se está utilizando durante el relevamiento con los distintos stakeholders del proyecto, mientras que el prototipado se aplicaría posteriormente para representar y validar los principales recorridos de la plataforma antes de desarrollarlos.

Ambas técnicas se complementan: las entrevistas permiten conocer en profundidad las necesidades, problemas y expectativas de los stakeholders, y el prototipado permite comprobar mediante una representación visual si el equipo interpretó correctamente la información relevada.

---

## Técnica 1: Entrevistas

### Descripción del proceso

La entrevista consiste en realizar reuniones individuales o grupales con usuarios y stakeholders para obtener información directa sobre sus procesos, problemas y necesidades.

Esta técnica ya se viene utilizando durante todo el relevamiento de FitConnect. Para cada consulta, el equipo define previamente qué información necesita obtener y selecciona al stakeholder que posee los conocimientos o la experiencia correspondiente.

Hasta el momento se realizaron entrevistas con:

* **Gabriel (Product Manager):** para conocer los objetivos del negocio, las prioridades del producto, el alcance del MVP, la composición del equipo y el modelo de proceso.
* **Mara (Legal):** para relevar las condiciones legales relacionadas con la verificación de entrenadores, el consentimiento de los usuarios y la protección de datos sensibles.
* **Diego (CTO / DevOps):** para identificar necesidades técnicas y de infraestructura vinculadas con la disponibilidad, la seguridad, el funcionamiento offline y las videollamadas.
* **Ana (Head de Entrenadores):** para comprender cómo trabajan los entrenadores y qué información y herramientas necesitan para crear rutinas y realizar el seguimiento de sus clientes.
* **Enzo (usuario activo):** para conocer las dificultades, preferencias y expectativas de los usuarios finales al comenzar una rutina, elegir un entrenador y consultar su progreso.

En cada entrevista se prepara una guía de preguntas relacionada con el objetivo de la consulta. Se utilizan principalmente preguntas abiertas para que el stakeholder pueda explicar su experiencia y sus necesidades, junto con preguntas cerradas, hipotéticas o de validación cuando es necesario obtener información más precisa, explorar posibles soluciones o confirmar que la respuesta fue interpretada correctamente.

Las consultas y las respuestas obtenidas se documentan indicando la fecha, el stakeholder, su rol, los temas tratados y el impacto de la información en el proyecto. De esta manera se mantiene la trazabilidad de las decisiones tomadas durante el relevamiento.

### Información obtenida y que podría seguir obteniéndose

Las entrevistas realizadas permitieron obtener información sobre:

* Los objetivos y prioridades del negocio.
* El alcance y las funcionalidades principales del MVP.
* Las causas que pueden provocar el abandono temprano de los usuarios.
* Las necesidades de los usuarios y de los entrenadores.
* La información necesaria para recomendar rutinas y seleccionar entrenadores.
* Las condiciones legales relacionadas con el consentimiento, la verificación de entrenadores y la protección de datos sensibles.
* Las necesidades técnicas y de infraestructura de la plataforma.
* Los requisitos de disponibilidad, rendimiento, seguridad y funcionamiento offline.
* Las funcionalidades previstas para versiones posteriores.

La entrevista también podría seguir utilizándose durante el proyecto cuando aparezcan dudas, información incompleta o decisiones que requieran la participación de un stakeholder determinado.

### Dificultad

Una dificultad de esta técnica es que los stakeholders pueden expresar necesidades o prioridades diferentes. Por ejemplo, una funcionalidad considerada importante por un usuario puede no coincidir con las prioridades del negocio o puede presentar dificultades técnicas o legales.

En esos casos, el equipo debe analizar las distintas perspectivas y consultar al stakeholder responsable antes de definir el requisito y decidir si corresponde incorporarlo al MVP o reservarlo para una versión posterior.

---

## Técnica 2: Prototipado

### Descripción del proceso

El prototipado consiste en crear una versión preliminar del sistema para representar sus pantallas y principales recorridos. Su finalidad es validar la comprensión de los requisitos y descubrir problemas antes de construir la versión definitiva.

En una primera instancia se podría desarrollar un prototipo de baja fidelidad, mediante bocetos en papel o wireframes, enfocado en el proceso de incorporación del usuario. El prototipo representaría las pantallas necesarias para:

1. Registrarse e ingresar la información indispensable.
2. Seleccionar el objetivo y las condiciones de entrenamiento.
3. Recibir e iniciar una rutina adecuada.

El prototipo se presentaría a Enzo, identificado como usuario activo, y se le pediría que complete tareas concretas sin recibir instrucciones detalladas. El equipo observaría dónde encuentra dificultades, qué opciones no comprende, qué información considera innecesaria y si puede comenzar una rutina de manera rápida y sin ayuda.

También podrían representarse otras acciones mencionadas durante el relevamiento, como consultar la explicación de un ejercicio, utilizar el temporizador de descanso, registrar o corregir resultados, finalizar una sesión y observar el progreso alcanzado.

Posteriormente se podría crear un prototipo orientado a los entrenadores y solicitar la participación de Ana para validar procesos como la creación de rutinas, el seguimiento de clientes y la administración de la disponibilidad.

Los comentarios, dudas y problemas detectados durante las pruebas serían registrados. Luego se modificaría el prototipo y se repetirían las pruebas hasta lograr que los recorridos principales resulten claros.

El uso del prototipado como técnica de recolección y validación de requisitos no modifica el **Modelo Incremental** seleccionado para FitConnect. Los prototipos se utilizarían dentro de la definición y validación de cada incremento, sin convertirse en el modelo general de desarrollo del proyecto.

### Información que permitiría obtener

El prototipado permitiría conocer:

* Si el proceso de registro y comienzo de una rutina resulta sencillo.
* Si el usuario comprende por qué se solicita cada dato.
* Si la organización de las pantallas, menús y opciones es clara.
* Si una persona puede iniciar un entrenamiento sin ayuda.
* Si las explicaciones de los ejercicios son comprensibles.
* Si el usuario puede registrar, corregir y consultar sus resultados.
* Qué errores, dudas o dificultades aparecen durante cada recorrido.
* Qué información o funcionalidades fueron omitidas.
* Qué cambios deberían realizarse antes de desarrollar la aplicación.
* Si la interpretación del equipo coincide con las expectativas de los usuarios y entrenadores.

### Dificultad

Una dificultad del prototipado es que los participantes pueden interpretar el prototipo como una versión terminada de la aplicación y concentrarse en aspectos visuales, como los colores o las imágenes, en lugar de evaluar los recorridos y las funcionalidades representadas.

Para disminuir esta dificultad, antes de comenzar la prueba se debería explicar que se trata de una representación preliminar, creada para validar ideas y detectar problemas, y que todavía no contiene el diseño ni el funcionamiento definitivo de FitConnect.

---

## Justificación de la selección

Seleccionamos estas dos técnicas porque permiten obtener información en momentos diferentes y complementarios del relevamiento.

Las entrevistas permiten descubrir y profundizar las necesidades de los distintos stakeholders. El prototipado permite transformar esas necesidades en una representación visual y comprobar si los recorridos diseñados son comprendidos por quienes utilizarán la plataforma.

Esta combinación es especialmente adecuada para FitConnect porque uno de sus principales objetivos es reducir la fricción durante el inicio y evitar el abandono temprano. Las entrevistas permiten comprender las causas de ese problema, mientras que el prototipado permite evaluar si una persona puede registrarse y comenzar una rutina de manera rápida, clara y sin ayuda.

---

## Referencias

* Kendall, K. E., & Kendall, J. E. *Análisis y Diseño de Sistemas*. 8.ª edición. Capítulos 4 y 5.
* Pressman, R. S. *Ingeniería del Software: Un Enfoque Práctico*. 7.ª edición. Capítulo 6.