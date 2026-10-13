
# Conversación con Gabriel (Product Manager)

**Fecha de la consulta:** 15/06/2026  
**Fecha de respuesta:** 16/06/2026  
**Participantes:** Equipo 6 – Gabriel (Product Manager)

## Consulta realizada

Hola Gabriel, buenas tardes.

Somos el Grupo 6 y nos encontramos realizando el análisis inicial del proyecto **FitConnect**.

Nos gustaría conocer su visión como Product Manager sobre los problemas que dieron origen a la plataforma. A partir de la lectura del enunciado identificamos inicialmente los siguientes:

### 1. Limitaciones de tiempo y espacio

- **Descripción del problema:** Muchas personas tienen horarios de trabajo, estudio u otras actividades que les dificultan asistir regularmente a un gimnasio o coordinar entrenamientos presenciales.
- **¿A quién afecta?** A personas que desean ejercitarse pero no disponen de horarios compatibles con gimnasios o entrenadores.
- **¿Cómo FitConnect resuelve este problema?** Permite acceder a rutinas, programas y material de entrenamiento desde cualquier lugar y en cualquier momento.

### 2. Costos elevados de entrenamiento

- **Descripción del problema:** Algunas personas no pueden afrontar el costo de una membresía de gimnasio o de un entrenador personal.
- **¿A quién afecta?** A personas con recursos económicos limitados que desean realizar actividad física.
- **¿Cómo FitConnect resuelve este problema?** Ofrece una modalidad **freemium** con acceso gratuito a parte del contenido y programas básicos de entrenamiento.

### 3. Limitación geográfica para entrenadores

- **Descripción del problema:** Los entrenadores de calistenia suelen depender de clientes de su zona geográfica o de un gimnasio determinado, lo que limita sus oportunidades de crecimiento profesional.
- **¿A quién afecta?** A entrenadores y profesionales de la calistenia.
- **¿Cómo FitConnect resuelve este problema?** Les permite ofrecer programas y sesiones personalizadas a usuarios de distintas ubicaciones.

También le consultamos:

1. ¿Considera que estos son los principales problemas que busca resolver FitConnect?
2. ¿Hay algún problema importante que no hayamos identificado?
3. Si tuviera que priorizarlos, ¿en qué orden lo haría y por qué?

---

## Respuesta de Gabriel

Gabriel indicó que los problemas planteados por el equipo son reales, pero aclaró que existe uno aún más importante: **el abandono de los usuarios**.

Explicó que el principal desafío del proyecto es reducir la fricción durante el proceso de incorporación, ya que una gran cantidad de usuarios abandona la aplicación durante las primeras semanas. Por ese motivo, estableció como objetivo prioritario que un usuario pueda configurar su perfil y comenzar una rutina con un entrenador **en menos de tres pasos**, reduciendo al mínimo la barrera de entrada.

En función de esto, propuso el siguiente orden de prioridad para el MVP:

1. **Reducir la fricción de inicio y mejorar la adherencia del usuario.**
2. **Facilitar el acceso mediante un modelo freemium**, ofreciendo programas gratuitos y una biblioteca de ejercicios.
3. **Permitir entrenar en cualquier momento y lugar**, eliminando la necesidad de gimnasios y equipamiento.
4. **Brindar oportunidades de crecimiento a los entrenadores**, ampliando su alcance geográfico, aunque aclaró que esto depende primero de contar con una base suficiente de usuarios activos.

Además, señaló un aspecto que el equipo no había considerado inicialmente: **la necesidad de generar confianza mediante la verificación de los entrenadores**. Indicó que este tema debía profundizarse con **Mara (Legal)**, ya que la plataforma necesita validar la identidad y la documentación de quienes ofrecen sus servicios.

También aclaró que algunas funcionalidades propuestas, como la incorporación de nutrición o informes avanzados para entrenadores, **no forman parte del MVP** y fueron planificadas para una segunda fase del proyecto.

Finalmente, nos orientó hacia otros stakeholders según cada temática:

- **Mara (Legal):** verificación de entrenadores y aspectos legales.
- **Ana (Head de Entrenadores):** proceso de verificación y esquema de comisiones.
- **Diego (CTO / DevOps):** arquitectura, sensores y decisiones técnicas.

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

- **Verificación documental con trazabilidad**, distinguiendo claramente entre certificaciones verificadas y credenciales auto declaradas (*self-report*).
- **Aceptación expresa de los Términos y Condiciones de Uso (TOS)** antes de iniciar cualquier sesión de entrenamiento, mediante una pantalla de aceptación obligatoria.
- **Consentimiento informado para el tratamiento de datos sensibles**, ya que la plataforma administrará información relacionada con la salud y la actividad física de los usuarios, debiendo cumplir normativas como **HIPAA** y **GDPR**.

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

- **Overcoming Gravity**, de Steven Low.
- **Periodization: Theory and Methodology of Training**, de Bompa & Buzzichelli.
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

---
# SEGUNDA ETAPA

# Conversación con Enzo (Futuro usuario) 

**Fecha de la consulta:** 06/09/2026  
**Fecha de respuesta:** 07/09/2026  
**Participantes:** Equipo 6 – Enzo (Futuro usuario)

## Consulta realizada

Hola Enzo, buenas tardes.

Somos el Grupo 6 y estamos comenzando la segunda etapa del análisis del proyecto **FitConnect**. Como futuro usuario de la plataforma, nos gustaría conocer tus necesidades, dificultades y expectativas relacionadas con el entrenamiento y con el uso de una aplicación de estas características.

Queríamos consultarte:

1. ¿Cómo organizás actualmente tus entrenamientos y qué dificultades encontrás para mantener una rutina de manera constante?
2. Si comenzaras a utilizar FitConnect, ¿qué información te parecería indispensable ingresar para que la aplicación pueda recomendarte una rutina adecuada?
3. ¿Qué aspectos podrían dificultarte el registro y el comienzo de un entrenamiento o llevarte a abandonar la plataforma durante las primeras semanas?
4. ¿Qué información necesitarías conocer antes de elegir un entrenador, por ejemplo, experiencia, certificaciones, especialidad, calificaciones, tarifa o disponibilidad?
5. ¿Qué herramientas o información te resultarían útiles para observar tu progreso y mantener la motivación?
6. Cuando contemos con un prototipo del proceso de registro y comienzo de una rutina, ¿qué aspectos considerarías importantes evaluar durante una prueba de usuario?

La respuesta permitirá incorporar la perspectiva del usuario final y comprender mejor qué debería ofrecer FitConnect para brindar una experiencia sencilla y útil.

---

## Respuesta de Enzo

Enzo explicó sus necesidades y expectativas desde la perspectiva de un futuro usuario de FitConnect.

### 1. Organización de los entrenamientos y dificultades

Actualmente organiza sus entrenamientos según el tiempo que tiene disponible y, en algunas ocasiones, utiliza rutinas obtenidas de Internet.

Señaló que su principal dificultad es mantener la constancia. Cuando no tiene claro qué ejercicios realizar, cuánto tiempo descansar o cómo adaptar una rutina si dispone de poco tiempo, suele terminar abandonando. También manifestó que le resulta difícil determinar si está progresando realmente.

### 2. Información necesaria para recomendar una rutina

Enzo indicó que preferiría ingresar solamente la información indispensable para recibir una recomendación adecuada:

- Objetivo principal.
- Nivel de experiencia.
- Días disponibles para entrenar.
- Tiempo disponible por sesión.
- Equipamiento disponible.
- Edad y condición física general.
- Lesiones, molestias o limitaciones.
- Preferencias de entrenamiento.

También señaló que, si el usuario informa una lesión, dolor o molestia, la aplicación debería advertirle sobre los posibles riesgos y ofrecerle alternativas seguras. Consideró especialmente importantes las advertencias relacionadas con hombros, muñecas y codos.

### 3. Factores que podrían dificultar el inicio o provocar el abandono

Entre los principales factores que podrían desmotivarlo o llevarlo a abandonar la aplicación, mencionó:

- Un proceso de registro demasiado extenso.
- La solicitud de información sin explicar para qué se utilizará.
- Una cantidad excesiva de opciones y menús.
- Una primera rutina que no se adapte al nivel del usuario.
- Ejercicios explicados de manera poco clara.
- Registros automáticos incorrectos de las repeticiones.

Enzo expresó que necesitaría comenzar rápidamente y consideró útil contar con una opción similar a un **“entrenamiento de 20 minutos”**. También manifestó que sería importante poder reprogramar una sesión o seleccionar una versión más corta de la rutina sin perder el progreso registrado.

### 4. Información necesaria para elegir un entrenador

Antes de contratar a un entrenador, Enzo consideró necesario consultar:

- Experiencia profesional.
- Certificaciones.
- Especialidad.
- Tipo de entrenamiento ofrecido.
- Calificaciones y opiniones de otros usuarios.
- Disponibilidad.
- Modalidad de atención.
- Tarifa final.
- Servicios incluidos en la tarifa.
- Tiempo estimado de respuesta.

También indicó que preferiría probar previamente la aplicación mediante rutinas gratuitas antes de decidir la contratación de un entrenador.

### 5. Seguimiento del progreso y motivación

Para observar su evolución y mantener la motivación, Enzo consideró útiles los siguientes datos:

- Récords personales.
- Sesiones completadas.
- Repeticiones realizadas.
- Tiempo total de entrenamiento.
- Progresiones alcanzadas.
- Comparaciones semanales y mensuales.

Aclaró que preferiría observar el progreso durante períodos semanales o mensuales y no depender solamente de una racha diaria.

También señaló que los recordatorios deberían ser configurables y no invasivos. Al finalizar una sesión, le resultaría útil recibir una devolución clara que le indique, por ejemplo, si realizó más repeticiones que la semana anterior o cuál debería ser su próximo objetivo.

### 6. Aspectos que deberían evaluarse en una prueba de usuario

Enzo consideró que la prueba debería permitir comprobar si una persona que nunca utilizó FitConnect puede registrarse, seleccionar un objetivo e iniciar una rutina en pocos minutos y sin ayuda.

También propuso evaluar si el usuario puede:

- Comprender qué ejercicio debe realizar.
- Identificar cuántas series y repeticiones corresponden.
- Utilizar el temporizador de descanso.
- Registrar manualmente sus resultados.
- Corregir un resultado ingresado incorrectamente.
- Finalizar una sesión.
- Consultar el progreso alcanzado.
- Cerrar la aplicación sin perder los datos.
- Perder la conexión sin que se eliminen los registros.
- Recibir una alternativa segura cuando declara una molestia o limitación.

Para Enzo, la prueba sería exitosa si pudiera entrenar sin sentirse perdido, si los registros fueran confiables y si la aplicación lo ayudara a mantener el hábito aun cuando dispusiera de poco tiempo.

Por el contrario, consideró que un proceso con demasiados datos obligatorios o información confusa podría provocar que dejara de utilizar la aplicación.

---

## Impacto en el proyecto

Esta conversación permitió:

- Incorporar la perspectiva de Enzo como **futuro usuario de FitConnect**.
- Confirmar que la falta de constancia, la dificultad para organizar una rutina y la imposibilidad de observar claramente el progreso son problemas importantes para los usuarios.
- Identificar los datos mínimos necesarios para configurar el perfil y recomendar un programa de entrenamiento.
- Respaldar la necesidad de reducir la cantidad de pasos y datos solicitados durante el proceso de incorporación.
- Identificar factores que podrían aumentar el abandono, como los registros extensos, los menús excesivos, la falta de explicaciones y una rutina inicial mal adaptada.
- Definir la información que debería presentarse en los perfiles de los entrenadores para facilitar su comparación y selección.
- Identificar los datos de progreso más relevantes para el usuario, como sesiones completadas, repeticiones, tiempo entrenado, récords personales y progresiones.
- Incorporar la necesidad de permitir el registro y la corrección manual de resultados.
- Respaldar el funcionamiento offline, evitando que el usuario pierda sus registros al cerrar la aplicación o perder la conexión.
- Definir criterios concretos para evaluar posteriormente el prototipo mediante una prueba de usuario.
- Confirmar que Enzo participará en las pruebas desde la perspectiva del usuario final y no como integrante del equipo de QA.

También surgieron necesidades adicionales que deberán analizarse y priorizarse antes de incorporarlas como requisitos definitivos:

- Ofrecer entrenamientos breves, por ejemplo, de 20 minutos.
- Permitir reprogramar una sesión.
- Permitir seleccionar una versión más corta de una rutina sin perder el progreso.
- Incorporar recordatorios configurables y no invasivos.
- Proporcionar una devolución comparativa al finalizar cada sesión.
- Informar el tiempo estimado de respuesta de los entrenadores.

La preocupación de Enzo sobre los errores del contador automático de repeticiones se conserva como información relevada. Sin embargo, no modifica el alcance actual del MVP, ya que el seguimiento automático mediante sensores no fue incluido en esta primera versión.

---

# Conversación con Gabriel (Product Manager) – Validación del relevamiento y de los requisitos del MVP

**Fecha del primer mensaje:** 19/09/2026  
**Fecha de la primera respuesta:** 20/09/2026  
**Fecha del segundo mensaje:** 23/09/2026  
**Fecha de la respuesta final:** 24/09/2026  
**Participantes:** Equipo 6 – Gabriel (Product Manager)

## Desarrollo de la conversación

La conversación con Gabriel se desarrolló mediante dos rondas de consulta. En la primera se buscó validar las técnicas de relevamiento y el recorrido inicial del usuario. A partir de su respuesta se realizó una segunda consulta para confirmar las funcionalidades, los requisitos de calidad, las restricciones y los objetivos de negocio del MVP.

---

## Primer mensaje del equipo – Validación de las técnicas de relevamiento

El equipo informó que venía utilizando entrevistas para conocer las prioridades del producto y las perspectivas de los usuarios, entrenadores y responsables de las áreas legal y técnica.

Se propuso continuar aplicando entrevistas cuando surgieran decisiones que necesitaran profundización o validación.

Como segunda técnica de relevamiento, se propuso utilizar un prototipo del recorrido inicial de FitConnect. El objetivo sería observar si una persona puede configurar su perfil, comprender el programa recomendado y comenzar a entrenar sin ayuda.

Enzo participaría en esta actividad desde la perspectiva del usuario. Durante la prueba se buscaría detectar:

- Pasos confusos.
- Información solicitada en exceso.
- Dificultades para configurar el perfil.
- Problemas para comprender el programa recomendado.
- Obstáculos para comenzar una rutina.

Se consultó a Gabriel:

1. Si las entrevistas y la prueba del prototipo eran técnicas adecuadas para validar las necesidades prioritarias de FitConnect.
2. Si el recorrido **configurar perfil → revisar rutina → comenzar entrenamiento** representaba correctamente la experiencia inicial esperada.
3. Si existía alguna decisión o dificultad importante que debiera investigarse mediante estas actividades.

---

## Primera respuesta de Gabriel

Gabriel confirmó que las dos actividades propuestas eran adecuadas y complementarias.

### Entrevistas

Indicó que las entrevistas debían continuar durante el relevamiento para profundizar decisiones relacionadas con:

- Prioridades del producto.
- Seguridad.
- Aspectos legales.
- Necesidades de los entrenadores.
- Viabilidad técnica.

### Prueba del prototipo

Consideró que la prueba del prototipo era apropiada para comprobar si un usuario puede comenzar a entrenar sin asistencia e identificar pasos confusos o datos innecesarios.

También corrigió el recorrido inicial propuesto. El flujo definitivo debería ser:

**Registro mínimo → confirmación del programa recomendado → inicio de la rutina.**

Gabriel estableció dos objetivos diferentes:

- El usuario deberá poder configurar su perfil en menos de tres toques.
- El usuario deberá poder comenzar su primer entrenamiento en menos de tres minutos.

Durante la prueba del prototipo recomendó evaluar:

- Tiempo necesario para iniciar la primera rutina.
- Porcentaje de usuarios que completa el onboarding.
- Comprensión de las series, repeticiones y descansos.
- Posibilidad de corregir un resultado registrado.
- Pérdida o duplicación de información ante una interrupción de la conexión.
- Claridad de las advertencias de seguridad.
- Claridad del consentimiento legal.

Además, solicitó profundizar mediante el relevamiento los siguientes aspectos:

- Qué datos relacionados con la salud son indispensables.
- Quiénes podrán acceder a esos datos.
- Cómo comunicar molestias o lesiones sin proporcionar recomendaciones riesgosas.
- Qué funciones mínimas necesitan los entrenadores en el MVP.
- Cómo funcionará el servicio ante cancelaciones, fallos o reembolsos.
- Qué métricas permitirán determinar el éxito del producto.

Gabriel indicó que las métricas principales deberían considerar especialmente la finalización del primer entrenamiento y la retención de los usuarios.

También definió como prioridades iniciales del MVP:

- Programas de entrenamiento.
- Biblioteca de ejercicios.
- Registro manual de resultados.
- Temporizador.
- Chat con entrenadores.
- Experiencia inicial sencilla.

Las siguientes funcionalidades quedaron fuera del MVP y deberán considerarse para incrementos posteriores:

- Sensores.
- Wearables.
- Gamificación avanzada.
- Reportes completos para entrenadores.

---

## Segundo mensaje del equipo – Validación de los requisitos del MVP

A partir de la primera respuesta, el equipo adoptó el recorrido:

**Registro mínimo → confirmación del programa recomendado → inicio de la rutina.**

También diferenció los objetivos de configurar el perfil en menos de tres toques y comenzar a entrenar en menos de tres minutos.

Posteriormente se envió una segunda consulta para validar la identificación y clasificación de los requisitos de FitConnect.

### 1. Funcionalidades consideradas para el MVP

El equipo propuso incluir:

- Registro mínimo.
- Configuración del perfil.
- Programa recomendado.
- Biblioteca de ejercicios con explicaciones, videos, progresiones y regresiones.
- Programas gratuitos y premium.
- Inicio y seguimiento de rutinas.
- Indicaciones de series, repeticiones y descansos.
- Temporizador.
- Registro manual de resultados.
- Corrección manual de resultados.
- Consulta del progreso.
- Consulta de sesiones completadas y resultados alcanzados.
- Chat con entrenadores.

También se solicitó confirmar si el marketplace básico debía formar parte del MVP. Las funciones consideradas fueron:

- Búsqueda de entrenadores por especialidad, tarifa y disponibilidad.
- Consulta de experiencia, certificaciones, calificaciones y modalidad de atención.
- Verificación de identidad y credenciales.
- Diferenciación entre credenciales verificadas e información declarada.

Finalmente, se consultó si las videollamadas formarían parte del MVP o quedarían para una etapa posterior.

### 2. Programa recomendado

El equipo interpretó que el sistema recomendaría automáticamente un programa después del registro mínimo, considerando la información proporcionada por el usuario.

Se solicitó confirmar si la recomendación automática formaría parte del MVP o si el usuario debería seleccionar manualmente un programa utilizando opciones o filtros.

### 3. Requisitos de calidad y restricciones

Se presentó para validación la siguiente lista:

- Inicio de la aplicación en menos de tres segundos.
- Configuración del perfil en menos de tres toques.
- Inicio del primer entrenamiento en menos de tres minutos.
- Compatibilidad con dispositivos móviles de gama media-baja.
- Tamaño inferior a 200 MB.
- Disponibilidad mínima del 99,5 %.
- Protección de los datos personales y de salud.
- Protección de la documentación de los entrenadores.
- Conservación local de los registros cuando no exista conexión.
- Sincronización posterior sin pérdidas ni duplicaciones.
- Modelo de negocio freemium.

Se aclaró que las decisiones técnicas serían profundizadas con Diego y que los requisitos relacionados con datos personales, consentimiento y documentación serían consultados con Mara.

### 4. Objetivos de negocio

El equipo propuso los siguientes objetivos:

- Reducir el abandono durante las primeras semanas.
- Aumentar la finalización del onboarding y del primer entrenamiento.
- Mejorar la retención y la continuidad de los usuarios.
- Permitir que los entrenadores ofrezcan sus servicios a usuarios de distintas ubicaciones.
- Sostener el producto mediante el modelo freemium.

Se solicitó a Gabriel que confirmara si estos objetivos representaban correctamente las prioridades del producto y si era necesario agregar, eliminar o modificar alguno.

---

## Segunda respuesta de Gabriel

Gabriel respondió cada uno de los puntos y confirmó el alcance general del MVP.

### 1. Funcionalidades confirmadas para el MVP

Gabriel confirmó la inclusión de:

- Registro mínimo.
- Configuración del perfil.
- Programa recomendado.
- Biblioteca de ejercicios.
- Programas gratuitos y premium.
- Inicio y seguimiento de rutinas.
- Temporizador.
- Registro manual de resultados.
- Corrección manual de resultados.
- Consulta del progreso básico.
- Chat con entrenadores.

También confirmó que el marketplace básico formará parte del MVP e incluirá:

- Búsqueda de entrenadores.
- Filtros por especialidad, tarifa y disponibilidad.
- Perfiles con experiencia, certificaciones, calificaciones y modalidad de atención.
- Verificación de identidad y credenciales.
- Diferenciación entre información verificada e información declarada.

Gabriel aclaró que ningún entrenador podrá publicar su perfil sin que previamente se haya verificado su identidad.

Las funciones avanzadas de gestión y los reportes completos para entrenadores quedaron planificados para una etapa posterior.

### Videollamadas

Gabriel confirmó que las videollamadas individuales también formarán parte del MVP.

Estableció las siguientes condiciones:

- No se grabarán por defecto.
- No se transcribirán por defecto.
- Deberá existir una alternativa cuando falle la conexión principal.
- Una falla en la videollamada no deberá impedir que el usuario realice su entrenamiento.

### 2. Programa recomendado

Gabriel confirmó que la recomendación del programa será automática.

El sistema deberá considerar principalmente:

- Objetivo del usuario.
- Nivel de experiencia.
- Tiempo y duración disponibles.
- Equipamiento disponible.
- Limitaciones o molestias informadas.

El sistema deberá explicar brevemente el motivo de la recomendación.

El usuario deberá confirmar el programa recomendado y también podrá cambiarlo manualmente.

El flujo definitivo quedó establecido de la siguiente manera:

**Registro mínimo → confirmación del programa recomendado → inicio de la rutina.**

### 3. Requisitos de calidad y restricciones

Gabriel confirmó los siguientes requisitos y objetivos:

- Inicio de la aplicación en menos de tres segundos.
- Configuración del perfil en menos de tres toques.
- Inicio del primer entrenamiento en menos de tres minutos.
- Compatibilidad con dispositivos móviles de gama media-baja.
- Tamaño inferior a 200 MB como objetivo del MVP.
- Disponibilidad mínima del 99,5 % como objetivo técnico.
- Protección obligatoria de los datos personales y de salud.
- Protección obligatoria de la documentación presentada por los entrenadores.
- Consentimiento obligatorio para el tratamiento de la información.
- Acceso restringido a los datos sensibles.
- Funcionamiento offline para los registros de entrenamiento.
- Sincronización posterior sin pérdidas ni duplicaciones.
- Modelo freemium.
- Ausencia de equipamiento especial como requisito para utilizar el MVP.

Gabriel mantuvo fuera del MVP:

- Wearables.
- Sensores.
- Funciones avanzadas de gestión para entrenadores.
- Reportes completos para entrenadores.

También indicó que Diego debía validar la factibilidad y las condiciones técnicas, mientras que Mara debía definir los requisitos legales específicos.

### 4. Objetivos de negocio

Gabriel confirmó los objetivos planteados y estableció el siguiente orden de prioridad:

1. Aumentar la finalización del onboarding y del primer entrenamiento.
2. Reducir el abandono durante las primeras semanas.
3. Mejorar la retención y la continuidad de los usuarios.
4. Ofrecer entrenadores a usuarios de distintas ubicaciones.
5. Sostener el producto mediante el modelo freemium.

Además, definió las siguientes métricas de negocio:

- Conversión al primer entrenamiento.
- Finalización de la primera sesión.
- Retención a los 30 días.
- Retención a los 60 días.
- Utilización de los programas de entrenamiento.
- Adopción del marketplace.

Gabriel concluyó que la prioridad del MVP es permitir que el usuario pueda comenzar a entrenar de manera rápida, sencilla y confiable.

El marketplace deberá crecer de manera paralela, pero no deberá desplazar ni dificultar la experiencia principal de comenzar a entrenar.

---

## Impacto en el proyecto

Esta conversación permitió:

- Validar las entrevistas semiestructuradas y la prueba de prototipo como técnicas complementarias de relevamiento.
- Confirmar que las entrevistas deberán mantenerse durante todo el relevamiento.
- Definir el recorrido inicial del usuario.
- Establecer métricas concretas para evaluar la prueba del prototipo.
- Confirmar las funcionalidades que forman parte del MVP.
- Incorporar el marketplace básico y la verificación de entrenadores dentro del MVP.
- Confirmar la inclusión de videollamadas individuales.
- Establecer que las videollamadas no serán grabadas ni transcritas por defecto.
- Confirmar que una falla en la videollamada no debe impedir la realización del entrenamiento.
- Definir el funcionamiento automático del programa recomendado.
- Establecer que el usuario deberá confirmar la recomendación y podrá cambiarla manualmente.
- Validar los principales requisitos de calidad y las restricciones del producto.
- Confirmar los objetivos de negocio y su orden de prioridad.
- Definir las métricas que permitirán evaluar el éxito del producto.
- Diferenciar las funcionalidades del MVP de aquellas planificadas para incrementos posteriores.
- Identificar los temas que debían profundizarse con Diego y Mara.

La información obtenida se utilizó principalmente para completar y validar:

- El **Punto 1 – Técnicas de Recolección de Requisitos**.
- El **Punto 2 – Identificación de Requisitos**.
- El **Punto 3 – Casos de Uso**.
- El **Punto 4 – Diagramas de Interacción**.
- El **Punto 5 – Arquitectura de Software**.
- El **Punto 6 – Modelado de Base de Datos**.
- El **Punto 7 – Atributos de Calidad**.

---

# Conversación con Diego (CTO / DevOps) – Segunda etapa

**Fecha de la consulta:** 24/09/2026 – 19:59 hs.  
**Fecha de respuesta:** 25/09/2026 – 20:08 hs.  
**Participantes:** Equipo 6 – Diego (CTO / DevOps)

## Consulta realizada

Hola Diego, buenas tardes.

Somos el Grupo 6 y estamos avanzando con la identificación de requisitos de la segunda etapa de FitConnect.

A partir del relevamiento anterior y de las últimas definiciones realizadas con Gabriel, identificamos los siguientes requisitos técnicos y de infraestructura para el MVP:

- La aplicación deberá iniciar en menos de tres segundos.
- Deberá funcionar correctamente en dispositivos móviles de gama media-baja.
- Su tamaño deberá ser inferior a 200 MB.
- La plataforma deberá mantener una disponibilidad mínima del 99,5 %.
- Los resultados de los entrenamientos deberán guardarse localmente cuando no exista conexión y sincronizarse posteriormente, evitando pérdidas o duplicaciones.
- La videollamada formará parte del MVP para encuentros individuales.
- Las videollamadas no se grabarán ni transcribirán por defecto.
- Si la conexión principal falla, deberá existir una alternativa que permita continuar la comunicación.
- Un fallo en la videollamada no deberá impedir que el usuario realice su entrenamiento.
- La infraestructura deberá contemplar copias de seguridad, replicación, monitoreo y alertas.

En la consulta anterior nos recomendaste utilizar SQLite para el almacenamiento local, un mecanismo de reintentos para la sincronización, WebRTC con servidores TURN/STUN para las videollamadas y un enlace de Zoom como alternativa ante fallos.

Antes de incorporar definitivamente estos requisitos a la documentación, queremos consultarte:

1. ¿Considerás que estos requisitos son técnicamente viables para el MVP y que se encuentran formulados correctamente?
2. ¿Qué mecanismo debería utilizarse para evitar que la sincronización offline produzca registros perdidos o duplicados?
3. ¿WebRTC con servidores TURN/STUN y un enlace alternativo continúa siendo la solución adecuada para las videollamadas del MVP?
4. ¿Qué medidas deberían contemplarse para cumplir simultáneamente con el tiempo de inicio, el límite de tamaño y la compatibilidad con dispositivos de gama media-baja?
5. ¿La replicación, las copias de seguridad, el monitoreo y las alertas son suficientes para sostener el objetivo de disponibilidad del 99,5 %?
6. ¿Existe algún requisito técnico o de infraestructura indispensable que todavía no hayamos contemplado?

La intención de esta consulta es validar los requisitos técnicos y de infraestructura antes de incorporarlos definitivamente a la documentación del proyecto.

Muchas gracias por tu tiempo.

Saludos,  
Grupo 6

---

## Respuesta de Diego

Buenas tardes, Grupo 6.

Los requisitos son técnicamente viables para el MVP, pero algunos deben formularse con condiciones medibles. Mantengo las decisiones conversadas anteriormente: SQLite para almacenamiento local, reintentos con backoff, WebRTC con STUN/TURN y Zoom como alternativa.

### 1. Viabilidad y formulación

Son viables, con estos ajustes:

- “Iniciar en menos de tres segundos” debe medirse como arranque en frío, sobre dispositivos de referencia de gama media-baja.
- “Funcionar en dispositivos de gama media-baja” requiere especificar modelos o versiones mínimas de Android e iOS.
- “Tamaño inferior a 200 MB” debe indicar si se refiere al tamaño descargado o al espacio instalado.
- El 99,5 % debe definirse como disponibilidad mensual del servicio, excluyendo mantenimientos programados previamente comunicados.
- El almacenamiento offline debe garantizar que no haya pérdida ni duplicación observable de registros.
- La videollamada debe ser opcional y nunca bloquear el registro o la realización del entrenamiento.

### 2. Sincronización offline

SQLite debe complementarse con una bandeja local de operaciones pendientes.

Cada operación tendrá un `operation_id` único generado en el dispositivo. El flujo será:

1. Guardar el entrenamiento localmente antes de informar éxito.
2. Guardar la operación pendiente junto con su identificador único.
3. Enviar la operación al servidor cuando haya conexión.
4. Procesarla de forma idempotente: si llega nuevamente el mismo `operation_id`, el servidor no debe crear otro registro.
5. Reintentar con backoff ante errores temporales.
6. Mantener la operación pendiente si los reintentos fallan y mostrar su estado al usuario.

En el backend debe existir una restricción única sobre `operation_id`. Para modificaciones, además, se necesitarán versiones y una política explícita de resolución de conflictos.

### 3. Videollamadas

WebRTC con STUN/TURN continúa siendo adecuado para videollamadas individuales del MVP:

- STUN intentará establecer una conexión directa.
- TURN funcionará como relay cuando existan restricciones de NAT o firewall.
- Debe contemplarse TURN sobre TCP/TLS por el puerto 443.
- La comunicación debe utilizar cifrado WebRTC.
- No se grabarán ni transcribirán llamadas por defecto.
- Deben medirse latencia, jitter, pérdida de paquetes, desconexiones y tiempo de establecimiento.

El enlace de Zoom es un fallback razonable si WebRTC no conecta o se degrada. Debe utilizarse luego de un tiempo acotado, quedar registrado como incidencia y no reemplazar una correcta configuración y capacidad de TURN.

### 4. Inicio, tamaño y dispositivos

Para cumplir simultáneamente los objetivos propongo:

- Carga diferida de imágenes, videos y contenido no esencial.
- Compresión de recursos y distribución mediante CDN.
- No descargar toda la biblioteca durante el primer inicio.
- Mostrar primero la acción principal, como “Iniciar entrenamiento”.
- Reducir dependencias y evitar procesos pesados durante el arranque.
- Probar consumo de memoria, batería, almacenamiento y rendimiento con conectividad limitada.
- Definir versiones mínimas concretas de Android e iOS.
- Ejecutar pruebas sobre dispositivos reales de referencia, no sólo emuladores.

### 5. Disponibilidad y recuperación

La replicación, los backups, el monitoreo y las alertas son necesarios, pero por sí solos no garantizan el 99,5 %.

El objetivo equivale aproximadamente a 3 horas y 39 minutos de indisponibilidad máxima mensual. Además, necesitamos:

- Réplica en otra zona de disponibilidad.
- Backups automáticos diarios y recuperación point-in-time.
- Copia de backups fuera de la zona principal.
- Pruebas periódicas de restauración.
- Health checks y monitoreo de errores, latencia, saturación y sincronizaciones pendientes.
- Alertas por errores 5xx, fallas de backup, retraso de réplicas, crecimiento de la cola offline y degradación de videollamadas.
- Un RPO inicial de 15 minutos y un RTO inicial de 1 hora.
- Procedimientos documentados de recuperación ante desastres.

Un backup que nunca fue restaurado exitosamente no constituye una estrategia confiable de recuperación.

### 6. Requisitos faltantes

Agregaría explícitamente:

- Autenticación, recuperación de cuenta y autorización por roles.
- Protección de datos de salud y documentación personal.
- Consentimiento, política de retención y eliminación de datos.
- Cifrado en tránsito y reposo, gestión segura de secretos y rotación de claves.
- Rate limiting y protección contra abuso.
- Auditoría de accesos y acciones sensibles.
- Pruebas de carga, seguridad, accesibilidad, pérdida de conexión y recuperación ante desastres.
- Compatibilidad y política de actualización de las aplicaciones móviles.
- Métricas de negocio y operación: errores offline, primer entrenamiento, uso de videollamadas y abandono.
- En pagos, webhooks idempotentes, reembolsos y conciliación.

En síntesis, los requisitos son adecuados para el MVP, pero deben incorporar métricas, condiciones de prueba, RPO/RTO y controles de seguridad. La prioridad debería ser una experiencia de entrenamiento disponible y recuperable; la videollamada debe mejorar esa experiencia sin convertirse en un punto único de falla.

Saludos,  
Diego

---

## Impacto en el proyecto

Esta conversación permitió:

- Confirmar la viabilidad técnica general de los requisitos propuestos para el MVP.
- Reformular los requisitos de rendimiento, disponibilidad, compatibilidad y tamaño mediante condiciones medibles.
- Definir el mecanismo de sincronización offline mediante SQLite, una bandeja local de operaciones, identificadores únicos, idempotencia y reintentos con backoff.
- Confirmar el uso de WebRTC con servidores STUN/TURN y Zoom como alternativa ante fallos.
- Establecer un RPO inicial de 15 minutos y un RTO inicial de una hora.
- Incorporar requisitos relacionados con autenticación, autorización, auditoría, seguridad, recuperación y protección contra abusos.
- Identificar definiciones técnicas pendientes sobre versiones móviles, dispositivos de referencia, tamaño de la aplicación y resolución de conflictos.

---

# Conversación con Mara (Legal / Risk & Insurance) – Segunda etapa

**Fecha de la consulta:** 24/09/2026 – 20:00 hs.  
**Fecha de respuesta:** 25/09/2026 – 20:13 hs.  
**Participantes:** Equipo 6 – Mara (Legal / Risk & Insurance)

## Consulta realizada

Hola Mara, buenas tardes.

Somos el Grupo 6 y estamos avanzando con la identificación de requisitos de la segunda etapa de FitConnect.

A partir del relevamiento anterior y de las últimas definiciones del producto, identificamos que FitConnect deberá tratar datos personales y de salud de los usuarios, además de documentación de identidad y certificaciones de los entrenadores.

Nuestra interpretación actual es que el MVP deberá:

- Solicitar únicamente los datos de salud necesarios para recomendar un programa y advertir sobre posibles limitaciones.
- Solicitar el consentimiento explícito para tratar información personal y sensible.
- Restringir el acceso a esos datos según el rol y la necesidad de cada participante.
- Cifrar la información durante su almacenamiento y transmisión.
- Registrar las acciones vinculadas con el acceso y la verificación documental.
- Verificar la identidad de los entrenadores antes de publicar sus perfiles.
- Diferenciar las credenciales verificadas de la información declarada por el entrenador.
- Informar advertencias claras cuando un usuario comunique una molestia, lesión o limitación.
- Evitar que la aplicación realice recomendaciones que puedan interpretarse como un diagnóstico o una indicación médica.
- No grabar ni transcribir las videollamadas por defecto.
- Informar las condiciones aplicables ante cancelaciones, fallas del servicio y posibles reembolsos.

Antes de incorporar definitivamente estos requisitos, queremos consultarte:

1. ¿Qué datos relacionados con la salud considerás indispensables para el MVP y cuáles no deberían solicitarse?
2. ¿Quiénes deberían poder acceder a esos datos: el usuario, el entrenador asignado, el personal de soporte o algún otro rol?
3. ¿Qué consentimientos y advertencias deberían presentarse durante el registro y antes de comenzar una rutina?
4. ¿Cómo debería comunicar la aplicación una molestia o lesión sin realizar recomendaciones riesgosas ni asumir funciones médicas?
5. ¿Qué documentación y controles mínimos deben exigirse para verificar y publicar el perfil de un entrenador?
6. ¿Qué condiciones deberían definirse para las cancelaciones, las fallas en sesiones virtuales y los reembolsos?
7. ¿La decisión de no grabar ni transcribir las videollamadas por defecto resulta suficiente o debería contemplarse alguna condición adicional?
8. ¿Existe algún requisito legal, de privacidad o de seguridad indispensable que todavía no hayamos considerado?

La intención de esta consulta es validar los requisitos legales y de seguridad antes de incorporarlos definitivamente a la documentación del proyecto.

Muchas gracias por tu tiempo.

Saludos,  
Grupo 6

---

## Respuesta de Mara

Reglas operativas del MVP, sin convertir la respuesta en asesoramiento legal jurisdiccional específico.

Buenas tardes, Grupo 6.

Valido el enfoque general. Para el MVP deben aplicar minimización de datos, acceso por necesidad y validación legal según la jurisdicción donde opere FitConnect.

### 1. Datos de salud indispensables

Solicitaría únicamente:

- Molestias o lesiones actuales.
- Limitaciones relevantes para realizar actividad física.
- Nivel de experiencia o entrenamiento.
- Restricciones que el usuario autorice a compartir con su entrenador.

No solicitaría inicialmente diagnósticos, historia clínica, medicación, imágenes médicas, biométricos, antecedentes familiares ni información que no sea necesaria para adaptar una rutina. El autodiagnóstico del usuario no debe presentarse como una evaluación médica.

### 2. Acceso a la información

- El usuario puede consultar y modificar sus propios datos.
- El entrenador asignado sólo debe acceder a las restricciones necesarias para prestar el servicio y con autorización del usuario.
- Soporte debe acceder únicamente a la información imprescindible para resolver un incidente.
- El área de pagos no necesita acceder a datos de salud.
- Legal o Compliance puede acceder a evidencias específicas cuando sea necesario.
- Marketing sólo debe utilizar métricas agregadas o anonimizadas.

Debe implementarse control de acceso por roles, mínimo privilegio, auditoría y revocación de permisos.

### 3. Consentimientos y advertencias

Durante el registro deben separarse:

- Aceptación de términos y condiciones.
- Política de privacidad.
- Consentimiento explícito para tratar datos de salud.
- Autorización para compartir información limitada con el entrenador.
- Consentimiento específico para comunicaciones o usos no esenciales.

Antes de comenzar una rutina debe informarse que:

- FitConnect no brinda atención médica, diagnóstico ni tratamiento.
- Las rutinas no reemplazan la consulta con un profesional de la salud.
- El usuario debe detenerse si siente dolor, malestar o síntomas inesperados.
- El usuario puede retirar su consentimiento, sujeto a las consecuencias operativas que correspondan.

La aceptación debe ser informada, registrable y revocable. No conviene utilizar una exoneración general como sustituto del consentimiento ni como forma de eliminar todas las responsabilidades de la plataforma.

### 4. Molestias o lesiones

La aplicación debe permitir informar una molestia, pausar el entrenamiento y enviar el aviso por un canal privado al entrenador.

La respuesta debe limitarse a:

- Recomendar detener o no iniciar la actividad ante señales de riesgo.
- Indicar que consulte a un profesional de la salud cuando corresponda.
- Ofrecer alternativas generales previamente aprobadas.
- Evitar diagnósticos, tratamientos, indicaciones médicas o afirmaciones de seguridad.

El entrenador tampoco debe diagnosticar por chat o videollamada. Ante síntomas graves o urgentes, la aplicación debe recomendar buscar atención médica inmediata.

### 5. Verificación de entrenadores

Antes de publicar el perfil o habilitar cobros se debería exigir:

- Verificación de identidad.
- Documento identificatorio válido.
- Certificaciones relevantes, organismo emisor y fecha de vencimiento.
- Revisión manual de la documentación.
- Aceptación de términos y código de conducta.
- Información sobre seguro de responsabilidad profesional cuando sea exigible.

El perfil debe diferenciar claramente entre “credencial verificada” e “información declarada”. Cada verificación debe conservar fecha, estado y trazabilidad. También deben existir revalidación periódica, canal de denuncias y suspensión ante documentación vencida o riesgos comprobados.

### 6. Cancelaciones, fallas y reembolsos

Antes del pago deben informarse claramente precio total, comisión, política de cancelación, reprogramación y reembolso.

Como regla del MVP:

- Si cancela el entrenador o la sesión no se presta, debe ofrecerse reprogramación o reembolso según la política publicada.
- Si falla WebRTC y no puede utilizarse el canal alternativo, no debe cobrarse una sesión no realizada.
- Si el usuario cancela, deben aplicarse las condiciones informadas previamente.
- Los pagos, reembolsos y webhooks deben registrarse de forma trazable e idempotente.
- Las incidencias deben documentarse sin almacenar el contenido de la conversación.

### 7. Videollamadas

No grabar ni transcribir por defecto es correcto, pero no alcanza por sí solo. También debe definirse:

- Qué proveedor interviene.
- Qué metadatos se generan.
- Durante cuánto tiempo se conservan.
- Dónde se almacenan y si existen transferencias internacionales.
- Cómo se eliminan o atienden solicitudes de los usuarios.
- Que no se utilizará audio o video para entrenamiento de modelos sin consentimiento específico de todos los participantes.

Los términos deben incluir reglas de conducta, contacto fuera de la plataforma, gestión de incidentes y prohibición de compartir o utilizar indebidamente la información de la sesión.

### 8. Requisitos faltantes

Agregaría explícitamente:

- Responsable y encargados del tratamiento de datos.
- Mapa de datos, finalidades, bases legales y plazos de conservación.
- Procedimiento para acceso, rectificación, eliminación y retiro del consentimiento.
- Contratos y evaluación de proveedores externos.
- Cifrado en tránsito y reposo.
- MFA para roles administrativos y entrenadores.
- Gestión segura de secretos y credenciales.
- Logs de acceso y alertas ante accesos anómalos.
- Respuesta ante incidentes y notificación de filtraciones.
- Backups protegidos y pruebas de restauración.
- Pruebas de seguridad y control de dependencias.
- Reglas específicas para menores, si fueran admitidos.

Recomiendo no habilitar perfiles pagos ni sesiones virtuales hasta cerrar estos controles. La implementación final debe ser revisada por asesoría legal especializada en las jurisdicciones donde opere FitConnect, ya que los requisitos aplicables a datos de salud, pagos y responsabilidad profesional pueden variar.

Saludos,  
Mara

---

## Impacto en el proyecto

Esta conversación permitió:

- Definir los datos de salud estrictamente necesarios para el MVP y aquellos que no deberán solicitarse.
- Establecer un esquema de acceso por roles, mínimo privilegio, auditoría y revocación de permisos.
- Separar los términos y condiciones, la política de privacidad y los distintos consentimientos requeridos.
- Establecer advertencias y límites para evitar diagnósticos, tratamientos o recomendaciones médicas.
- Ampliar los requisitos de verificación, publicación, revalidación y suspensión de entrenadores.
- Definir reglas para cancelaciones, fallas en sesiones virtuales y reembolsos.
- Incorporar condiciones adicionales de privacidad para las videollamadas.
- Identificar requisitos relacionados con conservación y eliminación de datos, proveedores externos, MFA, incidentes de seguridad y menores de edad.
- Detectar la necesidad de definir las jurisdicciones donde operará inicialmente FitConnect.

---

# Conversación con Ana (Head de Entrenadores) – Segunda etapa

**Fecha de la consulta:** 24/09/2026 – 20:01 hs.  
**Fecha de respuesta:** 29/09/2026 – 18:56 hs.  
**Participantes:** Equipo 6 – Ana (Head de Entrenadores)

## Consulta realizada

Hola Ana, buenas tardes.

Somos el Grupo 6 y estamos avanzando con la identificación de requisitos de la segunda etapa de FitConnect.

Gabriel confirmó que el MVP incluirá un marketplace básico de entrenadores con:

- Búsqueda y filtros por especialidad, tarifa y disponibilidad.
- Perfiles con experiencia, certificaciones, calificaciones y modalidad de atención.
- Verificación de identidad y credenciales.
- Diferenciación entre información verificada e información declarada.
- Chat y videollamadas individuales entre usuarios y entrenadores.

También indicó que las funciones avanzadas de gestión y los reportes completos para entrenadores quedarán para una etapa posterior.

A partir de la consulta anterior que realizamos con vos, entendemos que el entrenador también necesitará conocer cierta información del usuario, gestionar programas y adaptar los ejercicios cuando existan molestias o limitaciones. Sin embargo, necesitamos distinguir qué funciones son indispensables para el MVP y cuáles pueden postergarse.

Por este motivo, queríamos consultarte:

1. ¿Las funciones confirmadas para el marketplace son suficientes para que un entrenador pueda comenzar a utilizar FitConnect?
2. ¿Qué acciones mínimas debería poder realizar el entrenador dentro del MVP además de completar su perfil y comunicarse con los usuarios?
3. ¿El entrenador deberá poder crear y modificar programas personalizados desde el MVP o inicialmente trabajará con programas y plantillas ya disponibles?
4. ¿Qué información del usuario necesita conocer para adaptar un programa de manera segura y qué datos no serían necesarios?
5. ¿Cómo debería informarse al entrenador cuando un usuario declara una molestia, lesión o limitación?
6. ¿Qué alternativas debería poder ofrecer el entrenador sin que la plataforma brinde recomendaciones riesgosas?
7. ¿El calendario de disponibilidad y reservas es indispensable para el MVP?
8. ¿Qué funciones podrían quedar para una etapa posterior, por ejemplo, constructor avanzado de rutinas, reportes completos, panel de ingresos o herramientas avanzadas de seguimiento?
9. ¿Existe alguna función básica para los entrenadores que todavía no hayamos contemplado?

La intención de esta consulta es validar los requisitos relacionados con los entrenadores y definir con claridad qué herramientas deberán formar parte del MVP.

Muchas gracias por tu tiempo.

Saludos,  
Grupo 6

---

## Respuesta de Ana

Buenas tardes, Grupo 6:

Respondo puntualmente:

1. **¿Alcanza el marketplace confirmado?**  
   No completamente. Es suficiente para encontrar y contactar entrenadores, pero el MVP también debe permitir una operación básica: solicitudes, reservas, asignación de planes, seguimiento simple y registro de modificaciones.

2. **¿Qué acciones mínimas debe realizar el entrenador?**  
   Además de completar su perfil y comunicarse, debe poder:
   - Aceptar o rechazar solicitudes.
   - Consultar la información autorizada del usuario.
   - Asignar y modificar planes básicos.
   - Confirmar, cancelar o reprogramar sesiones.
   - Registrar observaciones y cambios realizados.
   - Dejar una devolución básica sobre la sesión.

3. **¿Debe crear programas personalizados desde el MVP?**  
   Sí, pero con alcance limitado. El MVP debería ofrecer plantillas editables, duplicación de programas, selección y orden básico de ejercicios, series, repeticiones o tiempo, descansos e instrucciones. El constructor avanzado y la periodización compleja pueden postergarse.

4. **¿Qué información del usuario necesita?**  
   Es suficiente con conocer nombre o alias, objetivo, nivel, disponibilidad, duración de las sesiones, equipamiento, preferencias y registros básicos de entrenamiento. Las molestias o limitaciones deben informarse voluntariamente y con consentimiento.

   No serían necesarios para el MVP diagnósticos, historia clínica completa, medicación, imágenes médicas ni datos biométricos.

5. **¿Cómo informar molestias, lesiones o limitaciones?**  
   Debe existir un aviso visible y específico dentro del perfil o del programa, indicando qué declaró el usuario y cuándo lo hizo. El entrenador debe poder pausar o excluir ejercicios y registrar la modificación. La plataforma debe aclarar que no realiza diagnósticos.

6. **¿Qué alternativas puede ofrecer el entrenador?**  
   Puede reducir la intensidad, el volumen o el rango de movimiento; reemplazar el ejercicio por otro previamente validado; o suspenderlo. Ante dolor intenso, empeoramiento o síntomas de alarma, debe indicar detener la actividad y consultar a un profesional de salud. FitConnect no debe recomendar tratamientos ni asegurar que una alternativa sea segura.

7. **¿Es indispensable el calendario?**  
   Sí, aunque con funciones básicas: disponibilidad, solicitud, confirmación, reserva, recordatorios, reprogramación y cancelación. También debe evitar dobles reservas y registrar el estado de cada sesión. La integración con calendarios externos puede quedar para después.

8. **¿Qué funciones pueden postergarse?**  
   Pueden quedar para una etapa posterior:
   - Constructor avanzado de rutinas.
   - Periodización compleja.
   - Reportes completos y dashboards comerciales.
   - Panel avanzado de ingresos.
   - Integración con wearables y sensores.
   - Automatizaciones avanzadas.
   - Grabación, transcripción y análisis automático de videollamadas.
   - Seguimiento basado en inteligencia artificial.

   No deberían postergarse la verificación, el consentimiento, las plantillas editables, las reservas, el progreso básico y el registro de cambios.

9. **¿Falta alguna función básica?**  
   Sí: consentimiento para compartir información, control de acceso a los datos, diferenciación entre información verificada y declarada, registro de modificaciones del plan, cancelaciones y sesiones realizadas. También debe existir un mecanismo básico para reportar inconvenientes o incidentes.

El criterio para considerar completo el MVP es que un entrenador verificado pueda recibir una solicitud, conocer la información necesaria y autorizada, reservar una sesión, asignar o adaptar un programa básico, comunicarse con el usuario y registrar el resultado sin exponer datos innecesarios ni brindar indicaciones médicas.

Saludos,  
**Ana**  
Head de Entrenadores — FitConnect

---

## Impacto en el proyecto

Esta conversación permitió:

- Determinar que el marketplace básico necesita incorporar funciones operativas para entrenadores.
- Identificar solicitudes, reservas, asignación de planes, seguimiento simple y registro de modificaciones como funciones necesarias.
- Definir las acciones mínimas que deberá realizar un entrenador dentro del MVP.
- Incorporar plantillas editables y una capacidad limitada de personalización de programas.
- Establecer qué información autorizada del usuario podrá consultar el entrenador.
- Definir el tratamiento funcional de molestias, lesiones y limitaciones sin realizar indicaciones médicas.
- Incorporar un calendario básico con disponibilidad, reservas, recordatorios, reprogramaciones y cancelaciones.
- Diferenciar las funciones indispensables de aquellas que podrán postergarse.
- Detectar la necesidad de validar con Gabriel la ampliación del alcance funcional del marketplace.

---

# Conversación con Gabriel (Product Manager) – Confirmación del alcance definitivo del MVP y selección de casos de uso

**Fecha de la consulta:** 29/09/2026  
**Fecha de respuesta:** 30/09/2026  
**Participantes:** Equipo 6 – Gabriel (Product Manager)

## Consulta realizada

Luego de analizar las respuestas recibidas de Ana, Mara y Diego, el equipo realizó una nueva consulta a Gabriel para cerrar el alcance funcional del MVP y evitar interpretaciones diferentes entre los requisitos, los casos de uso y los modelos posteriores.

La consulta se organizó alrededor de cinco temas principales.

### 1. Operación básica del entrenador

A partir de las necesidades señaladas por Ana, se solicitó confirmar si el marketplace del MVP también debía incluir las siguientes funciones básicas para los entrenadores:

- Recepción de solicitudes enviadas por los usuarios.
- Aceptación o rechazo de solicitudes.
- Consulta de la información del usuario previamente autorizada.
- Gestión de disponibilidad y calendario básico.
- Solicitud, confirmación y reserva de sesiones.
- Cancelación y reprogramación de sesiones.
- Prevención de dobles reservas.
- Asignación y modificación de programas mediante plantillas editables.
- Selección y ordenamiento de ejercicios.
- Configuración de series, repeticiones o tiempo.
- Configuración de descansos e instrucciones.
- Registro de las modificaciones realizadas en los programas.
- Registro de observaciones y devoluciones posteriores a una sesión.
- Registro de sesiones realizadas.
- Mecanismo para reportar inconvenientes o incidentes.

El equipo interpretó que continuarían fuera del MVP:

- Constructor avanzado de rutinas.
- Periodización compleja.
- Reportes completos.
- Dashboards comerciales.
- Panel avanzado de ingresos.
- Automatizaciones avanzadas.
- Sensores.
- Wearables.
- Seguimiento mediante inteligencia artificial.

### 2. Flujo entre el usuario y el entrenador

Se propuso el siguiente flujo básico:

**Búsqueda del entrenador → consulta del perfil → envío de solicitud → aceptación del entrenador → reserva de una sesión → asignación o adaptación de un programa → realización de la sesión → registro del resultado y devolución.**

También se solicitó confirmar:

- Si el MVP procesaría los pagos de las sesiones individuales.
- Si el pago se realizaría antes de confirmar la reserva.
- Si FitConnect cobraría una comisión.
- Si las cancelaciones, reprogramaciones y reembolsos formarían parte de la gestión básica del MVP.

### 3. Usuarios admitidos y mercado inicial

Teniendo en cuenta que Mara había señalado que las obligaciones legales dependen de la jurisdicción, se consultó:

- Si el MVP estaría destinado solamente a personas mayores de 18 años.
- Si la incorporación de menores requeriría la autorización de sus responsables legales.
- En qué país o mercado se realizaría inicialmente el lanzamiento.

El objetivo era evitar que el equipo asumiera una legislación específica como aplicable a todos los usuarios.

### 4. Prioridades ante una posible reducción del alcance

El equipo propuso el siguiente orden:

1. Registro mínimo, configuración del perfil, recomendación del programa e inicio de la primera rutina.
2. Biblioteca, programas, temporizador y registro manual del entrenamiento.
3. Conservación y sincronización de resultados sin pérdidas ni duplicaciones.
4. Comunicación mediante chat.
5. Verificación y búsqueda de entrenadores.
6. Solicitudes, reservas y asignación básica de programas.
7. Videollamadas individuales.
8. Pagos, cancelaciones y reembolsos.

Se solicitó confirmar si este orden representaba correctamente las prioridades del MVP.

### 5. Selección de procesos para el modelado

Para continuar con los casos de uso y los diagramas de interacción, el equipo propuso trabajar con los siguientes procesos:

1. **Configurar el perfil, obtener y confirmar un programa recomendado e iniciar la primera rutina.**
2. **Realizar una rutina, registrar o corregir los resultados y sincronizarlos sin pérdidas ni duplicaciones.**
3. **Buscar un entrenador, enviar una solicitud, reservar una sesión y recibir la asignación o adaptación de un programa.**

Se consultó si la selección era adecuada o si alguno de los procesos debía ser reemplazado.

---

## Respuesta de Gabriel

Gabriel confirmó las decisiones necesarias para cerrar el alcance del MVP.

### 1. Operación básica del entrenador

Gabriel confirmó que las siguientes funciones formarán parte del MVP:

- Envío de solicitudes de usuarios.
- Aceptación y rechazo de solicitudes.
- Consulta de la información del usuario previamente autorizada.
- Disponibilidad y calendario básico.
- Solicitud de sesiones.
- Confirmación y reserva de sesiones.
- Cancelación y reprogramación.
- Prevención de dobles reservas.
- Asignación y adaptación de programas mediante plantillas editables.
- Configuración de ejercicios.
- Configuración de series, repeticiones o tiempo.
- Configuración de descansos e instrucciones.
- Registro de modificaciones efectuadas en los programas.
- Observaciones y devolución básica posteriores a una sesión.
- Registro de las sesiones realizadas.
- Reporte de inconvenientes o incidentes.

Los entrenadores deberán tener su identidad y documentación profesional verificadas. La plataforma deberá diferenciar claramente la información verificada de aquella declarada por el entrenador.

Quedaron fuera del MVP:

- Constructor avanzado de rutinas.
- Periodización compleja.
- Reportes completos.
- Dashboards comerciales.
- Automatizaciones avanzadas.
- Sensores.
- Wearables.
- Seguimiento mediante inteligencia artificial.

### 2. Flujo entre el usuario y el entrenador

Gabriel confirmó el siguiente flujo:

**Búsqueda del entrenador → consulta del perfil → envío de solicitud → aceptación → reserva → asignación o adaptación del programa → realización de la sesión → registro y devolución.**

También confirmó que el MVP procesará los pagos de las sesiones mediante **Stripe**.

Antes de confirmar la operación deberán mostrarse:

- Importe total de la sesión.
- Comisión cobrada por FitConnect.

La comisión de FitConnect será del **20 %**.

Gabriel estableció las siguientes reglas:

- El pago se realizará antes de confirmar la reserva.
- No se cobrará una sesión que no se haya realizado.
- Las cancelaciones, reprogramaciones y solicitudes de reembolso estarán contempladas mediante una política publicada.
- Si el entrenador cancela o el servicio no se presta, deberá ofrecerse una reprogramación o un reembolso.

Las videollamadas individuales también formarán parte del MVP y deberán cumplir estas condiciones:

- No se grabarán por defecto.
- No se transcribirán por defecto.
- Deberá existir un mecanismo alternativo cuando falle la conexión.
- Una falla en la videollamada no deberá impedir que el usuario pueda realizar su entrenamiento.

### 3. Usuarios admitidos y mercado inicial

Gabriel indicó que el lanzamiento comercial se limitará inicialmente a las jurisdicciones que sean aprobadas por el área legal y por el responsable de privacidad.

El equipo no deberá asumir una normativa específica como aplicable universalmente. Las normas y los consentimientos deberán definirse según los mercados en los que se autorice el lanzamiento.

Como criterio inicial del MVP, solamente se admitirán personas mayores de 18 años.

La incorporación de menores requeriría:

- Una decisión legal específica.
- Consentimiento del padre, madre o responsable legal.
- Controles adicionales.

Por este motivo, los menores no formarán parte del primer alcance.

Gabriel también estableció que la aplicación no deberá solicitar:

- Historia clínica.
- Diagnósticos.
- Medicación.
- Información biométrica.

Para recomendar programas se utilizarán solamente los datos mínimos necesarios:

- Nivel de experiencia.
- Objetivo.
- Disponibilidad.
- Duración disponible.
- Equipamiento.
- Preferencias.
- Molestias declaradas opcionalmente.

La plataforma no realizará diagnósticos médicos ni garantizará resultados físicos o deportivos.

### 4. Prioridades del MVP

Gabriel confirmó el siguiente orden de prioridad:

1. Registro mínimo, configuración del perfil, recomendación del programa e inicio de la primera rutina.
2. Biblioteca, programas, temporizador y registro manual del entrenamiento.
3. Conservación y sincronización de resultados sin pérdidas ni duplicaciones.
4. Comunicación mediante chat.
5. Verificación y búsqueda de entrenadores.
6. Solicitudes, reservas y asignación básica de programas.
7. Videollamadas individuales.
8. Pagos, cancelaciones y reembolsos.

La prioridad principal será permitir que el usuario pueda entrenar y volver a hacerlo.

El marketplace crecerá en paralelo, pero no deberá comprometer la confiabilidad de las funciones principales de entrenamiento.

Gabriel también confirmó que el registro manual deberá:

- Funcionar sin conexión.
- Confirmar al usuario el almacenamiento local de la información.
- Reintentar posteriormente la sincronización.
- Evitar la generación de registros duplicados.

### 5. Procesos seleccionados para el modelado

Gabriel consideró adecuada la selección de los tres procesos:

1. **Configurar el perfil, confirmar un programa recomendado e iniciar la primera rutina.**
2. **Realizar una rutina, registrar o corregir resultados y sincronizarlos sin pérdidas ni duplicaciones.**
3. **Buscar un entrenador, enviar una solicitud, reservar una sesión y recibir la asignación o adaptación de un programa.**

Los pagos, las cancelaciones y los reembolsos deberán representarse como reglas transversales del tercer proceso.

No será necesario convertirlos en un cuarto proceso principal.

Gabriel concluyó que el MVP deberá caracterizarse por ofrecer:

- Entrenamiento manual.
- Programas editables.
- Marketplace seguro.
- Pagos transparentes.
- Controles legales previos al lanzamiento.
- Funcionamiento simple y confiable.

Las funcionalidades más sofisticadas deberán permanecer fuera del MVP hasta que existan evidencias suficientes de adopción y retención.

---

## Impacto en el proyecto

Esta conversación permitió:

- Cerrar el alcance funcional definitivo del MVP.
- Confirmar las funciones básicas necesarias para que los entrenadores puedan operar dentro de la plataforma.
- Confirmar el flujo completo entre el usuario y el entrenador.
- Incorporar solicitudes, reservas, cancelaciones y reprogramaciones.
- Incorporar la prevención de dobles reservas.
- Confirmar la asignación y adaptación de programas mediante plantillas editables.
- Incorporar el registro de modificaciones realizadas en los programas.
- Confirmar el registro de sesiones, observaciones, devoluciones e incidentes.
- Establecer la verificación obligatoria de la identidad y documentación profesional de los entrenadores.
- Confirmar el procesamiento de pagos mediante Stripe.
- Establecer una comisión del 20 % para FitConnect.
- Incorporar reglas para cancelaciones, reprogramaciones y reembolsos.
- Confirmar la inclusión de videollamadas individuales.
- Establecer que las videollamadas no se grabarán ni transcribirán por defecto.
- Limitar inicialmente el MVP a personas mayores de 18 años.
- Determinar que el lanzamiento solo se realizará en jurisdicciones previamente aprobadas por las áreas legal y de privacidad.
- Aplicar el principio de minimización de datos.
- Excluir la recopilación de historia clínica, diagnósticos, medicación y datos biométricos.
- Confirmar el orden definitivo de prioridades del MVP.
- Confirmar que el registro manual deberá funcionar sin conexión y sincronizarse sin pérdidas ni duplicaciones.
- Validar los tres procesos seleccionados para los casos de uso y los diagramas de interacción.
- Definir los pagos, cancelaciones y reembolsos como reglas transversales del tercer proceso.
- Diferenciar claramente las funcionalidades del MVP de aquellas previstas para incrementos posteriores.

La información obtenida se utilizó para mantener la consistencia entre:

- El **Punto 2 – Identificación de Requisitos**.
- El **Punto 3 – Casos de Uso**.
- El **Punto 4 – Diagramas de Interacción**.
- El **Punto 5 – Arquitectura de Software**.
- El **Punto 6 – Modelado de Base de Datos**.
- El **Punto 7 – Atributos de Calidad**.

---

# Conversación con Diego (CTO / DevOps) – Arquitectura y almacenamiento del MVP

**Fecha de la consulta:** 29/09/2026 – 19:33 hs.  
**Fecha de respuesta:** 30/09/2026 – 20:31 hs.  
**Participantes:** Equipo 6 – Diego (CTO / DevOps)

## Consulta realizada

Hola Diego, buenas tardes.

Somos el Grupo 6. Gracias por las precisiones proporcionadas sobre rendimiento, funcionamiento offline, videollamadas, disponibilidad, recuperación y seguridad.

Para cerrar los requisitos técnicos y utilizar las mismas decisiones en el diseño de la arquitectura y del almacenamiento de FitConnect, necesitamos definir los siguientes puntos.

## 1. Compatibilidad, dispositivos y tamaño

Respecto de las condiciones medibles que señaló:

- ¿Qué versiones mínimas de Android e iOS recomienda admitir en el MVP?
- ¿Qué dispositivos concretos podríamos utilizar como referencia de gama media-baja para las pruebas?
- ¿El objetivo de menos de 200 MB debería aplicarse al tamaño de descarga, al espacio instalado o a ambos?
- ¿Qué consumo máximo de memoria, almacenamiento o batería considera razonable establecer como referencia?
- ¿Las pruebas de arranque en frío deberían realizarse con conectividad normal y también con conectividad limitada?

## 2. Arquitectura general del MVP

Considerando el alcance actual, la disponibilidad mensual del 99,5 %, el funcionamiento offline y la proyección de aproximadamente 15.000 usuarios activos:

- ¿Recomienda comenzar con un monolito modular, una arquitectura basada en servicios o microservicios?
- ¿Qué módulos o servicios deberían mantenerse separados desde el MVP?
- ¿Conviene contar con una única API de backend o utilizar un API Gateway?
- ¿El chat, las notificaciones, los pagos y las videollamadas deberían resolverse mediante servicios propios o proveedores externos?
- ¿Qué componentes considera indispensables para representar correctamente la arquitectura inicial?

Como propuesta preliminar, identificamos los siguientes componentes:

- Aplicación móvil.
- Base local SQLite.
- API o backend.
- Autenticación y autorización.
- Gestión de usuarios y entrenadores.
- Programas, ejercicios y rutinas.
- Reservas y calendario.
- Seguimiento del progreso.
- Chat y notificaciones.
- Videollamadas WebRTC.
- Pagos y reembolsos.
- Almacenamiento de imágenes, videos y documentación.
- Sincronización de operaciones offline.
- Auditoría, monitoreo y alertas.

¿Esta separación es adecuada o recomienda reorganizarla?

## 3. Persistencia y organización de datos

Para el almacenamiento central necesitamos confirmar:

- ¿Recomienda una base de datos relacional como almacenamiento principal?
- ¿Qué motor sería adecuado para el MVP?
- ¿Los mensajes del chat, los registros de auditoría y las operaciones pendientes deberían almacenarse en la misma base o en servicios separados?
- ¿Las imágenes, los videos y la documentación de los entrenadores deberían almacenarse en un servicio de objetos, conservando solamente sus referencias en la base de datos?
- ¿Conviene separar lógica o físicamente los datos de salud, consentimientos y documentación sensible?
- ¿Cómo recomienda representar el historial de cambios realizados en un programa de entrenamiento?
- ¿Qué información debe conservarse para asegurar la trazabilidad de reservas, cancelaciones, pagos, reembolsos y verificaciones?

## 4. Sincronización y conflictos

Usted indicó la necesidad de utilizar una bandeja local de operaciones, identificadores únicos, idempotencia, versionado y una política explícita de resolución de conflictos.

Para completar esa definición:

- ¿Qué política recomienda para el MVP cuando el usuario modifica un registro offline que también fue modificado en el servidor?
- ¿Debe prevalecer la última versión, la versión del servidor o requerirse una resolución explícita?
- ¿El estado de sincronización debería mostrarse por cada registro o mediante un estado general?
- ¿Durante cuánto tiempo deberían conservarse las operaciones pendientes o fallidas?
- ¿Qué acciones deberían ejecutarse cuando una operación no puede sincronizarse después de varios reintentos?

## 5. Infraestructura y despliegue

Tomando como base el RPO de 15 minutos, el RTO de una hora y la réplica en otra zona:

- ¿Recomienda utilizar servicios administrados para la base de datos, backups, almacenamiento de objetos, monitoreo y colas?
- ¿La infraestructura inicial debería incluir balanceador de carga, múltiples instancias del backend y escalado automático?
- ¿Se necesita una cola de mensajes para sincronización, notificaciones, procesamiento de pagos u otras tareas?
- ¿Qué mecanismo de caché recomienda para programas, biblioteca de ejercicios y contenido de consulta frecuente?
- ¿Cómo debería distribuirse el contenido multimedia para no afectar el inicio de la aplicación ni el límite de tamaño?
- ¿Qué ambientes mínimos deberían existir, por ejemplo desarrollo, pruebas y producción?

## 6. Integraciones externas

Para evitar que servicios externos se conviertan en puntos únicos de falla:

- ¿Qué criterios deberían utilizarse para seleccionar proveedores de pagos, notificaciones, almacenamiento y videollamadas?
- ¿Cómo debería registrarse una falla de WebRTC y la utilización del enlace alternativo de Zoom?
- ¿Conviene utilizar un proveedor externo de calendario o mantener inicialmente un calendario propio?
- ¿Qué información deberían conservar los webhooks de pagos para garantizar idempotencia, conciliación y trazabilidad?

La intención es que estas definiciones se utilicen de manera consistente en los requisitos técnicos, la arquitectura, el modelo de datos y las decisiones de infraestructura del MVP.

Muchas gracias por su tiempo.

Saludos,  
Grupo 6

---

## Respuesta de Diego

Buenas tardes, Grupo 6:

Revisé la consulta y dejo establecidas las decisiones técnicas del MVP.

**1. Compatibilidad y dispositivos**

- Android mínimo: Android 10, API 29.
- iOS mínimo: iOS 16.
- Referencias de prueba: Motorola Moto G9 Play, Samsung Galaxy A32, Xiaomi Redmi Note 9, iPhone SE de segunda generación e iPhone 11.
- El límite de 200 MB se aplicará al espacio instalado. El paquete de descarga inicial también deberá mantenerse por debajo de ese límite.
- Memoria objetivo: menos de 250 MB durante una rutina normal.
- SQLite tendrá un límite inicial de 50 MB y el caché multimedia, de 500 MB.
- La prueba de arranque en frío se realizará con 4G estable, Wi-Fi limitado, modo avión y recuperación de conectividad.
- El objetivo de arranque menor a tres segundos se medirá en un dispositivo Android de gama media.

Los videos no se incluirán en la instalación. Se descargarán bajo demanda y se eliminarán sin perder los registros de entrenamiento.

**2. Arquitectura**

No recomiendo microservicios para este volumen. Utilizaremos un monolito modular con:

- Aplicación móvil multiplataforma.
- API REST sobre HTTPS.
- Backend Node.js con TypeScript.
- PostgreSQL administrado.
- SQLite local.
- Redis para caché y coordinación limitada.
- Cola administrada para tareas asincrónicas.
- Object storage y CDN para contenido multimedia.
- Balanceador y al menos dos instancias del backend.
- Monitoreo, auditoría y alertas.

Los módulos serán autenticación, usuarios, entrenadores, ejercicios, programas, entrenamientos, progreso, reservas, chat, videollamadas, pagos, verificaciones, notificaciones, consentimientos, auditoría y sincronización offline. Compartirán el despliegue, pero mantendrán responsabilidades claramente separadas.

Stripe se utilizará para pagos y reembolsos. WebRTC será la opción principal para videollamadas, con TURN administrado y Zoom como alternativa. Chat, notificaciones, multimedia y pagos se resolverán mediante servicios especializados o administrados, no mediante implementaciones propias innecesarias.

**3. Persistencia**

La base principal será PostgreSQL administrado, con alta disponibilidad, cifrado, backups y recuperación puntual.

SQLite almacenará en el dispositivo programas descargados, ejercicios, sesiones incompletas, registros manuales, operaciones pendientes y estados de sincronización.

- Los mensajes podrán permanecer inicialmente en PostgreSQL, con índices y políticas de retención.
- La auditoría se almacenará en PostgreSQL como registros append-only.
- Las operaciones pendientes se almacenarán en SQLite y se enviarán mediante la API.
- Las imágenes, videos y documentos se conservarán en object storage; la base guardará únicamente referencias, metadatos, permisos y versiones.
- Los datos sensibles, consentimientos y documentación tendrán controles de acceso separados, aunque inicialmente puedan residir en la misma base física.

Los programas se versionarán. Cada modificación conservará autor, fecha, versión anterior, versión nueva, motivo y tipo de cambio. También se trazará el historial de reservas, cancelaciones, reprogramaciones, pagos, reembolsos, verificaciones y consentimientos.

**4. Sincronización y conflictos**

Cada operación tendrá un `operation_id` único, versión, fecha de creación y estado de sincronización.

- Los registros de entrenamiento se tratarán como eventos y no se sobrescribirán silenciosamente.
- Las correcciones se almacenarán como cambios trazables o eventos compensatorios.
- En perfiles se utilizará última escritura válida con control de versión.
- En programas asignados por entrenadores prevalecerá la versión del servidor.
- En conflictos relevantes se conservarán ambas versiones y se solicitará resolución explícita.
- Nunca se eliminarán datos sin informar al usuario.

El estado deberá mostrarse por registro y también mediante un resumen general. Las operaciones se reintentarán automáticamente hasta tres veces. Luego quedarán visibles como pendientes o fallidas, sin eliminarse.

Las operaciones pendientes se conservarán hasta confirmación, resolución manual o una política de retención definida para cada tipo de dato. Los errores permanentes deberán mostrar una explicación y permitir reintentar o solicitar asistencia.

**5. Infraestructura y despliegue**

Recomiendo utilizar servicios administrados:

- ECS Fargate para API y workers.
- Application Load Balancer.
- RDS PostgreSQL Multi-AZ.
- Redis administrado.
- S3 para objetos y respaldos.
- CloudFront como CDN.
- SQS para tareas asincrónicas.
- CloudWatch y Sentry para monitoreo.
- Secrets Manager para credenciales.

Habrá dos instancias del backend en zonas diferentes, con posibilidad de escalado automático. La cola se utilizará para notificaciones, sincronización, procesamiento de pagos, webhooks y tareas que no deban bloquear la respuesta de la API.

Redis se utilizará para biblioteca de ejercicios, programas publicados, perfiles públicos, configuraciones, rate limiting y datos temporales. No será fuente definitiva ni contendrá mensajes privados, pagos o datos de salud.

Los videos se servirán desde object storage mediante CDN y URLs firmadas cuando corresponda. Se utilizará MP4/H.264, hasta 720p, sin incluirlos en la aplicación.

Existirán tres ambientes separados:

- Desarrollo, con datos sintéticos.
- Staging, con configuración similar a producción.
- Producción, con datos reales, backups y monitoreo.

El RPO será de 15 minutos y el RTO, de una hora. La disponibilidad objetivo del 99,5% implica aproximadamente 3 horas y 39 minutos máximos de indisponibilidad mensual.

**6. Integraciones externas**

Los proveedores se seleccionarán considerando:

- Disponibilidad y acuerdos de nivel de servicio.
- Seguridad, cifrado y cumplimiento legal.
- Soporte de idempotencia y webhooks.
- Capacidad de exportar datos.
- Costos previsibles.
- Posibilidad de reemplazo sin rediseñar el dominio.
- Monitoreo, reintentos y documentación técnica.

Toda falla de WebRTC registrará estado, fecha, usuario técnico afectado, motivo y si se utilizó el enlace alternativo de Zoom. No se almacenará el contenido de la llamada.

El calendario será inicialmente propio, porque solo necesitamos disponibilidad, reservas, cancelaciones y reprogramaciones internas. No integraremos Google Calendar o Apple Calendar en el MVP.

Los webhooks de pagos conservarán proveedor, identificador del evento, tipo, fecha, payload validado, firma, estado de procesamiento, cantidad de reintentos y referencia interna de la operación. Serán idempotentes y auditables. Si un proveedor falla, la operación quedará pendiente; nunca se informará como exitosa sin confirmación.

En síntesis, la arquitectura inicial será un monolito modular, con PostgreSQL administrado, SQLite offline, almacenamiento de objetos, servicios administrados, colas, CDN, WebRTC con fallback y fuerte trazabilidad. Dejamos microservicios y componentes más sofisticados para una etapa posterior, cuando el crecimiento los justifique.

Saludos,

Diego  
CTO / DevOps — FitConnect

---

## Impacto en el proyecto

Esta conversación permitió:

- Definir las versiones mínimas de Android e iOS y los dispositivos de referencia para las pruebas.
- Establecer límites medibles para el tamaño de la aplicación, el consumo de memoria, SQLite y el caché multimedia.
- Definir las condiciones para medir el arranque en frío y el funcionamiento ante distintos estados de conectividad.
- Seleccionar un monolito modular como arquitectura inicial del backend.
- Definir las tecnologías principales: Node.js con TypeScript, PostgreSQL, SQLite, Redis, servicios de cola, object storage y CDN.
- Identificar los módulos funcionales que conformarán el backend.
- Definir la distribución de responsabilidades entre PostgreSQL, SQLite, Redis y el almacenamiento de objetos.
- Establecer el versionado y la trazabilidad de programas, reservas, pagos, reembolsos, verificaciones y consentimientos.
- Definir las políticas de sincronización, corrección y resolución de conflictos.
- Establecer la infraestructura de AWS y los ambientes de desarrollo, staging y producción.
- Confirmar el RPO de 15 minutos, el RTO de una hora y la disponibilidad mensual del 99,5%.
- Definir los criterios de selección y utilización de proveedores externos.
- Confirmar el uso de Stripe, WebRTC, TURN y Zoom.
- Establecer que el calendario será propio y que no se integrarán calendarios externos en el MVP.