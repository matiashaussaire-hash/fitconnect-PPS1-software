\# 2. Identificación de Requisitos



Los requisitos de FitConnect fueron identificados a partir de la definición inicial del producto, las decisiones tomadas durante la primera etapa y la información obtenida mediante el relevamiento con los distintos stakeholders.



Para organizarlos, se diferenciaron los requisitos funcionales, los requisitos no funcionales de calidad, las restricciones, los requerimientos de negocio, los requisitos técnicos y los requisitos de infraestructura.



\## a) Requisitos Funcionales



Los requisitos funcionales describen las funciones, los servicios y los comportamientos que deberá proporcionar FitConnect.



Para expresarlos se utilizó el modelo de Historia de Usuario:



\* \*\*Como:\*\* identifica el rol que necesita la funcionalidad.

\* \*\*Quiero:\*\* expresa la acción o capacidad requerida.

\* \*\*Para:\*\* establece el beneficio o la razón que justifica su incorporación.



Las historias no fueron planteadas exclusivamente desde la perspectiva del usuario que entrena. También se consideraron otros actores que interactuarán con la plataforma, como los entrenadores y el personal responsable de verificar sus credenciales.



\### HU-01: Configurar el perfil y comenzar una rutina



\*\*Como\*\* usuario activo

\*\*Quiero\*\* configurar mi perfil e iniciar una rutina adaptada a mis características

\*\*Para\*\* comenzar a entrenar rápidamente y recibir una propuesta adecuada a mis necesidades.



\#### Criterios de aceptación



1\. Dado que el usuario ingresa por primera vez, cuando configura su perfil, entonces puede informar su objetivo, nivel de experiencia, días y tiempo disponibles, equipamiento, edad, condición física general, lesiones, limitaciones y preferencias de entrenamiento.

2\. Dado que el usuario completó la información obligatoria, cuando confirma su perfil, entonces el sistema presenta una rutina acorde con su objetivo, nivel, disponibilidad y equipamiento.

3\. Dado que el usuario informa una lesión, molestia o limitación, cuando el sistema propone la rutina, entonces muestra una advertencia y ofrece alternativas de ejercicios previamente consideradas seguras para esa condición.



\### HU-02: Buscar y seleccionar un entrenador



\*\*Como\*\* usuario activo

\*\*Quiero\*\* buscar entrenadores y consultar la información de sus perfiles

\*\*Para\*\* seleccionar al profesional que mejor se adapte a mis necesidades y posibilidades.



\#### Criterios de aceptación



1\. Dado que el usuario accede al marketplace, cuando realiza una búsqueda, entonces puede filtrar a los entrenadores por especialidad, tarifa, disponibilidad y modalidad de atención.

2\. Dado que el usuario selecciona un entrenador, cuando consulta su perfil, entonces puede visualizar su experiencia, certificaciones, especialidad, calificaciones, disponibilidad, tarifa final, servicios incluidos y tiempo estimado de respuesta.

3\. Dado que una credencial fue revisada por FitConnect, cuando el usuario consulta el perfil del entrenador, entonces el sistema diferencia claramente las credenciales verificadas de aquellas declaradas por el profesional.



\### HU-03: Consultar la biblioteca de ejercicios



\*\*Como\*\* usuario activo

\*\*Quiero\*\* acceder a una biblioteca de ejercicios de calistenia

\*\*Para\*\* comprender cómo realizar cada ejercicio y encontrar opciones adecuadas a mi nivel.



\#### Criterios de aceptación



1\. Dado que el usuario accede a la biblioteca, cuando realiza una búsqueda, entonces puede filtrar los ejercicios por nivel, grupo muscular y equipamiento disponible.

2\. Dado que el usuario selecciona un ejercicio, cuando consulta su información, entonces puede visualizar una explicación de su ejecución y los videos demostrativos disponibles desde diferentes ángulos.

3\. Dado que un ejercicio posee diferentes niveles de dificultad, cuando el usuario consulta su detalle, entonces puede acceder a sus progresiones, regresiones y alternativas disponibles.



\### HU-04: Seguir un programa de entrenamiento



\*\*Como\*\* usuario activo

\*\*Quiero\*\* acceder a un programa de entrenamiento estructurado

\*\*Para\*\* organizar mis sesiones y avanzar progresivamente hacia mi objetivo.



\#### Criterios de aceptación



1\. Dado que el usuario selecciona un programa, cuando consulta su información, entonces puede visualizar su duración, sus objetivos, las sesiones previstas y los ejercicios que lo componen.

2\. Dado que el usuario utiliza la versión gratuita, cuando consulta los programas disponibles, entonces puede acceder a los dos programas básicos incluidos en el plan freemium.

3\. Dado que el usuario posee una suscripción premium, cuando consulta los programas, entonces puede acceder a todos los programas habilitados para ese nivel de suscripción.



\### HU-05: Registrar y consultar el progreso



\*\*Como\*\* usuario activo

\*\*Quiero\*\* registrar los resultados de mis entrenamientos y consultar mi evolución

\*\*Para\*\* saber si estoy progresando y mantener la motivación.



\#### Criterios de aceptación



1\. Dado que el usuario realiza una sesión, cuando completa un ejercicio, entonces puede registrar y corregir manualmente las series, repeticiones, tiempo y resultado alcanzado.

2\. Dado que el usuario finaliza una sesión, cuando consulta su progreso, entonces puede visualizar las sesiones completadas, las repeticiones realizadas, el tiempo entrenado, el volumen de entrenamiento, las progresiones alcanzadas y sus récords personales.

3\. Dado que existen registros de diferentes fechas, cuando el usuario consulta su evolución, entonces puede comparar su progreso semanal y mensual y recibir una devolución sobre los resultados alcanzados.



\### HU-06: Crear y administrar programas de entrenamiento



\*\*Como\*\* entrenador

\*\*Quiero\*\* crear, guardar y asignar programas de entrenamiento

\*\*Para\*\* planificar el trabajo de mis clientes de manera organizada y eficiente.



\#### Criterios de aceptación



1\. Dado que el entrenador crea una rutina, cuando accede al constructor, entonces puede seleccionar ejercicios de la biblioteca y organizarlos mediante una herramienta de arrastrar y soltar.

2\. Dado que el entrenador finaliza una rutina, cuando decide guardarla, entonces puede almacenarla como una plantilla reutilizable.

3\. Dado que el entrenador consulta el perfil de un cliente, cuando asigna o modifica un programa, entonces puede considerar sus objetivos, experiencia, disponibilidad, condición física y limitaciones registradas.



\### HU-07: Verificar las credenciales de los entrenadores



\*\*Como\*\* responsable de verificación de FitConnect

\*\*Quiero\*\* revisar la identidad y las credenciales presentadas por los entrenadores

\*\*Para\*\* determinar si pueden ofrecer sus servicios dentro de la plataforma.



\#### Criterios de aceptación



1\. Dado que un entrenador solicita su incorporación, cuando presenta su documentación, entonces el responsable puede consultar su documento de identidad, certificados, institución emisora, fecha de emisión y vigencia.

2\. Dado que la documentación fue revisada, cuando finaliza la verificación, entonces el responsable puede aprobarla, rechazarla o solicitar información adicional.

3\. Dado que se completa una acción relacionada con la verificación, cuando el sistema registra el resultado, entonces conserva la identidad del responsable, la fecha, la documentación revisada y la decisión tomada.



\### HU-08: Comunicarse con un entrenador



\*\*Como\*\* usuario activo

\*\*Quiero\*\* comunicarme con mi entrenador mediante chat o videollamada

\*\*Para\*\* recibir orientación sin necesidad de asistir presencialmente a un gimnasio.



\#### Criterios de aceptación



1\. Dado que el usuario se encuentra vinculado con un entrenador, cuando accede al chat, entonces puede enviar y recibir mensajes y consultar el historial de la conversación.

2\. Dado que existe una sesión virtual acordada, cuando el usuario y el entrenador ingresan a la videollamada, entonces pueden comunicarse mediante audio y video.

3\. Dado que no puede establecerse la videollamada principal, cuando se detecta el fallo de conexión, entonces el sistema proporciona el enlace alternativo previsto para realizar la sesión.



\## b) Requisitos No Funcionales de Calidad



\### RNF-01: Rendimiento



La aplicación deberá iniciar en menos de tres segundos.



Este requisito busca reducir la espera inicial y evitar que el tiempo de carga contribuya a la frustración o al abandono temprano de los usuarios.



\### RNF-02: Disponibilidad



La plataforma deberá mantener una disponibilidad mínima del 99,5 %.



Esto permitirá que los usuarios y entrenadores accedan a las rutinas, registros, programas y herramientas de comunicación con un nivel reducido de interrupciones.



\### RNF-03: Seguridad y protección de la información



Los datos personales y sensibles de los usuarios, junto con la documentación presentada por los entrenadores, deberán protegerse mediante cifrado durante su almacenamiento y transmisión.



El sistema también deberá limitar el acceso a esta información según el rol de cada persona y mantener un registro de las acciones vinculadas con la consulta y verificación de la documentación.



\### RNF-04: Usabilidad



El proceso de incorporación deberá permitir que un usuario configure su perfil y comience una rutina en un máximo de tres pasos principales.



Las pantallas deberán solicitar únicamente la información necesaria, explicar de manera comprensible para qué se utiliza cada dato y evitar presentar una cantidad excesiva de opciones durante el primer ingreso.



\### RNF-05: Compatibilidad y eficiencia



La aplicación deberá funcionar correctamente en dispositivos móviles de gama media-baja, manteniendo una experiencia de uso fluida y permitiendo el acceso a las funciones principales de FitConnect.



La compatibilidad deberá comprobarse mediante un conjunto de dispositivos y versiones de sistemas operativos definido para las pruebas del producto.



\## c) Restricciones



\### REST-01: Tamaño de la aplicación



La aplicación móvil deberá ocupar menos de 200 MB.



Esta limitación condicionará la cantidad y el tamaño de los videos, imágenes y demás recursos que puedan almacenarse dentro de la aplicación.



\### REST-02: Modelo de negocio



FitConnect deberá operar mediante un modelo freemium.



La versión gratuita incluirá el acceso a la biblioteca de ejercicios y a dos programas básicos. El acceso al resto de los programas y a las funcionalidades premium requerirá una suscripción.



Los entrenadores podrán establecer sus propias tarifas y FitConnect retendrá una comisión por las transacciones realizadas mediante la plataforma.



\### REST-03: Protección de datos y cumplimiento legal



La plataforma deberá respetar las condiciones legales definidas para el tratamiento de datos personales y sensibles, contemplando los lineamientos aplicables de HIPAA y GDPR.



También deberá solicitar el consentimiento explícito del usuario para el tratamiento de sus datos sensibles y registrar la aceptación de los Términos y Condiciones correspondientes.



\## d) Requerimientos de Negocio



\### RN-01: Reducir el abandono temprano



FitConnect busca reducir el abandono de los usuarios durante las primeras semanas de utilización, disminuyendo la fricción del proceso de incorporación y facilitando el comienzo y la continuidad de una rutina de entrenamiento.



\### RN-02: Ampliar el alcance de los entrenadores



FitConnect busca permitir que los entrenadores de calistenia ofrezcan sus programas y servicios a personas de diferentes ubicaciones, superando las limitaciones geográficas del entrenamiento presencial.



\### RN-03: Sostener un modelo de negocio digital



FitConnect busca generar ingresos mediante las suscripciones premium y las comisiones obtenidas por las transacciones realizadas entre usuarios y entrenadores dentro de la plataforma.



\## e) Requisitos Técnicos



\### RT-01: Funcionamiento offline-first



La aplicación deberá utilizar un enfoque \*offline-first\* y almacenar localmente mediante SQLite la información necesaria para continuar una sesión de entrenamiento cuando no exista conexión.



Cuando el dispositivo recupere la conectividad, deberá ejecutar un mecanismo de reintentos para sincronizar con el servidor los registros que se encuentren pendientes.



\### RT-02: Videollamadas



Las videollamadas deberán implementarse mediante WebRTC y utilizar servidores TURN/STUN para establecer la comunicación.



En caso de que la conexión principal no pueda realizarse, el sistema deberá ofrecer un enlace de Zoom como alternativa para completar la sesión.



\## f) Requisitos de Infraestructura



\### RI-01: Disponibilidad y recuperación



La infraestructura deberá contar con mecanismos de replicación de datos, copias de seguridad, monitoreo y alertas que permitan sostener el objetivo de disponibilidad del 99,5 % y recuperar el servicio ante posibles fallos.



\### RI-02: Comunicación en tiempo real



La infraestructura deberá disponer de los servidores y recursos de red necesarios para soportar las videollamadas mediante WebRTC, incluyendo servidores TURN/STUN y capacidad suficiente para transmitir audio y video de manera estable.



\### RI-03: Distribución de contenido multimedia



La infraestructura deberá utilizar mecanismos de distribución y compresión de contenido que permitan proporcionar los videos e imágenes de la biblioteca sin afectar el tiempo de inicio ni el funcionamiento de la aplicación en dispositivos de gama media-baja.



\## Trazabilidad con el relevamiento



El desarrollo completo de las consultas y respuestas se encuentra registrado en \[SEGUIMIENTO.md](./SEGUIMIENTO.md). Para evitar repetir el mismo enlace en cada requisito, la relación entre las consultas y las decisiones tomadas se presenta en la siguiente matriz.



| Stakeholder consultado          | Fecha de consulta | Información relevante obtenida                                                                                                                                                                                  | Requisitos relacionados                                                  |

| ------------------------------- | ----------------: | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |

| Gabriel – Product Manager       |        15/06/2026 | Prioridad de reducir la fricción inicial y el abandono; incorporación rápida; modelo freemium; necesidad de generar confianza mediante la verificación de entrenadores.                                         | HU-01, HU-04, RNF-04, REST-02, RN-01 y RN-02                             |

| Mara – Legal / Risk \& Insurance |        17/06/2026 | Verificación documental con trazabilidad; distinción entre credenciales verificadas y declaradas; consentimiento para datos sensibles; cifrado y registro de auditoría.                                         | HU-02, HU-07, RNF-03 y REST-03                                           |

| Diego – CTO / DevOps            |        20/06/2026 | Disponibilidad del 99,5 %; funcionamiento offline-first; SQLite; sincronización mediante reintentos; WebRTC; TURN/STUN; respaldo mediante Zoom; replicación, copias de seguridad y monitoreo.                   | HU-05, HU-08, RNF-01, RNF-02, RNF-03, RT-01, RT-02, RI-01, RI-02 y RI-03 |

| Ana – Head de Entrenadores      |        26/06/2026 | Información necesaria de los clientes; constructor de rutinas; plantillas reutilizables; biblioteca de ejercicios; seguimiento de clientes y administración de programas.                                       | HU-01, HU-03, HU-05, HU-06 y RN-02                                       |

| Gabriel – Product Manager       |        02/07/2026 | Confirmación de que FitConnect será una aplicación móvil y de la necesidad de contemplar dispositivos y tecnologías orientadas al desarrollo mobile.                                                            | RNF-05                                                                   |

| Enzo – Usuario activo           |        06/09/2026 | Datos necesarios para recomendar una rutina; dificultades que pueden provocar abandono; información requerida para elegir entrenador; seguimiento del progreso; carga manual y prueba de la experiencia de uso. | HU-01, HU-02, HU-03, HU-05 y RNF-04                                      |



La consulta realizada a Gabriel el 06/07/2026 se relacionó específicamente con la elección del modelo de proceso. Por ese motivo, se encuentra documentada en `SEGUIMIENTO.md`, pero no se incorporó en esta matriz, ya que no dio origen a requisitos particulares del sistema.



\## Documentación interna relacionada



\* \[PROBLEMAS.md](./PROBLEMAS.md)

\* \[CONOCIMIENTOS.md](./CONOCIMIENTOS.md)



\## Material teórico de referencia



\* Pressman, R. S. \*Ingeniería del Software: Un Enfoque Práctico\*. 7.ª edición. Capítulos 5, 6 y 7.



