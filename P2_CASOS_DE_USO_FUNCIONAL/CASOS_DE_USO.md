# 3. Casos de Uso



Para el modelado se seleccionaron tres requisitos funcionales debido a su importancia para el MVP, la cantidad de acciones involucradas, la participación de diferentes actores y la existencia de múltiples escenarios alternativos.



Los procesos seleccionados fueron validados por Gabriel (Product Manager) el 30/09/2026:



1. Configurar el perfil, confirmar un programa recomendado e iniciar la primera rutina.

2. Realizar una rutina, registrar o corregir resultados y sincronizarlos sin pérdidas ni duplicaciones.

3. Buscar un entrenador, enviar una solicitud, reservar una sesión y recibir la asignación o adaptación de un programa.



Los pagos, cancelaciones, reprogramaciones y reembolsos fueron incorporados como reglas transversales del tercer caso de uso.



---



# CU-01: Configurar el perfil e iniciar la primera rutina



## Objetivo



Permitir que una persona mayor de 18 años realice el registro mínimo, configure su perfil, reciba una recomendación automática, confirme el programa propuesto y comience su primera rutina de entrenamiento.



## Actor principal



- Usuario.



## Precondiciones



1. El usuario debe tener instalada la aplicación FitConnect.

2. El usuario debe ser mayor de 18 años.

3. El usuario no debe tener una cuenta activa o debe tener pendiente la configuración inicial de su perfil.

4. La aplicación debe poder acceder a los servicios necesarios para completar el registro y obtener el programa recomendado.

5. Los términos y condiciones, la política de privacidad y los consentimientos aplicables deben encontrarse disponibles para su consulta.



## Flujo básico



1. El usuario abre FitConnect por primera vez.

2. El sistema presenta la opción de registrarse.

3. El usuario selecciona la opción de registro.

4. El sistema informa que el MVP está destinado exclusivamente a personas mayores de 18 años.

5. El usuario confirma que cumple con la edad mínima requerida.

6. El sistema solicita los datos indispensables para crear la cuenta.

7. El usuario ingresa sus datos de identificación y acceso.

8. El sistema presenta por separado:

&nbsp;  - Los términos y condiciones.

&nbsp;  - La política de privacidad.

&nbsp;  - El consentimiento para el tratamiento de datos relacionados con molestias o limitaciones.

&nbsp;  - La autorización para compartir información limitada con un entrenador.

&nbsp;  - Los consentimientos para comunicaciones o usos no esenciales.

9. El usuario acepta los términos obligatorios y selecciona los consentimientos opcionales que desea otorgar.

10. El sistema solicita la información necesaria para configurar el perfil:

&nbsp;   - Objetivo de entrenamiento.

&nbsp;   - Nivel de experiencia.

&nbsp;   - Días disponibles.

&nbsp;   - Duración disponible para cada sesión.

&nbsp;   - Equipamiento disponible.

&nbsp;   - Preferencias de entrenamiento.

&nbsp;   - Molestias o limitaciones, de manera opcional.

11. El usuario completa la información requerida.

12. El sistema valida que los campos obligatorios estén completos.

13. El sistema crea la cuenta y registra el perfil, los consentimientos y las autorizaciones otorgadas.

14. El sistema analiza el objetivo, nivel, disponibilidad, duración, equipamiento, preferencias y limitaciones informadas.

15. El sistema selecciona automáticamente un programa adecuado entre los programas disponibles.

16. El sistema presenta el programa recomendado e informa brevemente los motivos de la recomendación.

17. El usuario consulta el objetivo, la duración, las sesiones y los ejercicios principales del programa.

18. El usuario confirma el programa recomendado.

19. El sistema asigna el programa al perfil del usuario.

20. El sistema presenta la primera rutina correspondiente al programa.

21. El usuario selecciona la opción de iniciar la rutina.

22. El sistema registra el inicio del primer entrenamiento y presenta el primer ejercicio.



## Flujos alternativos



### FA-01: El usuario es menor de 18 años



1. En el paso 5 del flujo básico, el usuario indica que no cumple con la edad mínima.

2. El sistema informa que el MVP de FitConnect está disponible únicamente para personas mayores de 18 años.

3. El sistema no permite continuar con el registro.

4. El caso de uso finaliza sin crear la cuenta.



### FA-02: Datos obligatorios incompletos



1. En el paso 12 del flujo básico, el sistema detecta que falta información obligatoria.

2. El sistema identifica los campos que deben completarse.

3. El usuario completa o corrige la información.

4. El flujo continúa desde el paso 12.



### FA-03: El usuario no acepta los términos obligatorios



1. En el paso 9 del flujo básico, el usuario no acepta los términos y condiciones o la política de privacidad.

2. El sistema informa que esas aceptaciones son necesarias para utilizar FitConnect.

3. El usuario puede volver a consultar los documentos o cancelar el registro.

4. Si cancela, el caso de uso finaliza sin crear la cuenta.



### FA-04: El usuario no autoriza el tratamiento de datos opcionales



1. En el paso 9 del flujo básico, el usuario no autoriza el tratamiento de molestias, limitaciones o comunicaciones no esenciales.

2. El sistema permite continuar con el registro sin solicitar esa información.

3. El sistema registra que el consentimiento opcional no fue otorgado.

4. El flujo continúa desde el paso 10 utilizando únicamente los datos autorizados.



### FA-05: El usuario informa una molestia o limitación



1. En el paso 10 del flujo básico, el usuario informa voluntariamente una molestia o limitación.

2. El sistema registra la información junto con la fecha de declaración.

3. El sistema informa que FitConnect no brinda atención médica, diagnósticos ni tratamientos.

4. El sistema indica que el usuario debe detener la actividad y consultar a un profesional de la salud ante dolor, malestar o síntomas inesperados.

5. La información se utiliza únicamente para evitar programas o ejercicios incompatibles y sólo se comparte con un entrenador cuando existe autorización.

6. El flujo continúa desde el paso 11.



### FA-06: No se encuentra un programa completamente compatible



1. En el paso 15 del flujo básico, el sistema no encuentra un programa que cumpla con todas las condiciones informadas.

2. El sistema presenta las opciones disponibles más cercanas.

3. El sistema explica qué condiciones no pudieron satisfacerse completamente.

4. El usuario puede modificar sus preferencias, consultar otros programas o cancelar el proceso.

5. Si modifica sus preferencias, el flujo regresa al paso 14.



### FA-07: El usuario no acepta el programa recomendado



1. En el paso 18 del flujo básico, el usuario decide no confirmar el programa recomendado.

2. El sistema permite consultar otros programas compatibles.

3. El usuario selecciona manualmente otro programa.

4. El sistema presenta el detalle del programa seleccionado.

5. El usuario confirma la nueva elección.

6. El flujo continúa desde el paso 19.



### FA-08: Se pierde la conexión durante el registro



1. Antes de completar el paso 13, la aplicación pierde la conexión.

2. El sistema conserva localmente la información ingresada como borrador.

3. El sistema informa que el registro no pudo completarse y que los datos quedarán pendientes.

4. Cuando se recupera la conexión, el usuario puede reanudar el proceso.

5. El flujo continúa desde el último paso confirmado.



## Postcondiciones



### Postcondiciones de éxito



1. La cuenta del usuario queda creada.

2. El perfil queda configurado con la información proporcionada.

3. Los consentimientos y autorizaciones quedan registrados de manera trazable.

4. El usuario tiene un programa asignado y confirmado.

5. La primera rutina queda iniciada.

6. El sistema registra el tiempo transcurrido hasta el inicio del primer entrenamiento.



### Postcondiciones mínimas



1. Si el proceso no se completa, no se crea una cuenta activa de manera incorrecta.

2. Los datos ingresados y autorizados se conservan únicamente cuando corresponde.

3. Los consentimientos rechazados no se consideran otorgados.

4. El sistema no recomienda programas basados en datos que el usuario no autorizó a utilizar.



## Relaciones consideradas para el diagrama



El caso de uso principal incluye:



- Registrar usuario.

- Validar edad.

- Gestionar consentimientos.

- Configurar perfil.

- Generar recomendación.

- Confirmar programa.

- Iniciar primera rutina.



Los siguientes comportamientos extienden el caso principal:



- Informar molestia o limitación.

- Cambiar programa recomendado.

- Reanudar registro pendiente.



## Diagrama UML



![Diagrama UML del caso de uso CU-01](./diagramas/CU_01_CONFIGURAR_PERFIL.svg)



---



# CU-02: Realizar una rutina y registrar resultados



## Objetivo



Permitir que el usuario realice una rutina, consulte las instrucciones, utilice el temporizador, registre o corrija sus resultados y conserve la información aunque el dispositivo no tenga conexión.



## Actor principal



- Usuario.



## Actores secundarios



- Entrenador, cuando la rutina fue asignada o adaptada por un profesional.



## Precondiciones



1. El usuario debe tener una cuenta activa.

2. El usuario debe haber iniciado sesión.

3. El usuario debe tener un programa asignado o seleccionado.

4. La rutina debe encontrarse disponible en el dispositivo.

5. Los ejercicios necesarios deben estar descargados o disponibles para su consulta.

6. La base local SQLite debe encontrarse operativa.

7. Si la rutina fue asignada por un entrenador, el programa debe contar con una versión vigente.



## Flujo básico



1. El usuario accede al programa que tiene asignado.

2. El sistema presenta las rutinas disponibles.

3. El usuario selecciona la rutina que desea realizar.

4. El sistema recupera la rutina y sus ejercicios desde el almacenamiento local.

5. El sistema presenta:

&nbsp;  - Ejercicios incluidos.

&nbsp;  - Orden de realización.

&nbsp;  - Series.

&nbsp;  - Repeticiones o tiempo.

&nbsp;  - Descansos.

&nbsp;  - Instrucciones.

&nbsp;  - Material demostrativo disponible.

6. El usuario selecciona la opción de iniciar la rutina.

7. El sistema registra localmente la fecha y hora de inicio.

8. El sistema presenta el primer ejercicio.

9. El usuario consulta las instrucciones y realiza la serie indicada.

10. El usuario registra manualmente las repeticiones, el tiempo o el resultado alcanzado.

11. El sistema guarda el resultado en SQLite antes de informar que el registro fue exitoso.

12. El sistema genera un `operation_id` único, la versión, la fecha de creación y el estado de sincronización.

13. El sistema confirma al usuario que el resultado quedó guardado localmente.

14. El usuario inicia el temporizador de descanso.

15. El sistema informa la finalización del descanso.

16. El usuario continúa con la siguiente serie o ejercicio.

17. Los pasos 8 a 16 se repiten hasta completar todos los ejercicios.

18. El usuario selecciona la opción de finalizar la rutina.

19. El sistema registra localmente la fecha y hora de finalización.

20. El sistema presenta un resumen con los ejercicios, series, repeticiones, tiempos y resultados registrados.

21. El usuario revisa y confirma el resumen.

22. El sistema actualiza localmente el progreso, las sesiones completadas y los récords personales correspondientes.

23. Si existe conexión, el sistema envía las operaciones pendientes al servidor.

24. El servidor procesa cada operación de manera idempotente utilizando el `operation_id`.

25. El servidor confirma la recepción y el registro de los resultados.

26. El sistema actualiza el estado de cada operación como sincronizada.

27. El usuario puede consultar el resultado de la sesión y su progreso actualizado.



## Flujos alternativos



### FA-01: El dispositivo no tiene conexión



1. En el paso 23 del flujo básico, el sistema detecta que no existe conexión.

2. Los resultados permanecen almacenados en SQLite.

3. Las operaciones quedan identificadas con estado pendiente.

4. El sistema muestra el estado pendiente en cada registro y en un resumen general.

5. El usuario puede cerrar la aplicación sin perder la información.

6. Cuando se recupera la conexión, el sistema intenta sincronizar automáticamente las operaciones pendientes.

7. El flujo continúa desde el paso 24.



### FA-02: Error temporal durante la sincronización



1. En el paso 24 del flujo básico, se produce un error temporal.

2. El sistema conserva la operación pendiente.

3. El sistema realiza hasta tres reintentos automáticos utilizando una espera progresiva.

4. Si alguno de los reintentos finaliza correctamente, el flujo continúa desde el paso 25.

5. Si todos los reintentos fallan, se ejecuta el flujo alternativo FA-03.



### FA-03: La operación no puede sincronizarse



1. Los tres reintentos automáticos finalizan sin éxito.

2. El sistema marca la operación como fallida o pendiente de resolución.

3. El sistema muestra una explicación al usuario.

4. La operación no se elimina.

5. El usuario puede volver a intentar la sincronización o solicitar asistencia.

6. El registro permanece guardado localmente hasta su confirmación o resolución.



### FA-04: El servidor recibe una operación duplicada



1. En el paso 24 del flujo básico, el servidor recibe un `operation_id` que ya fue procesado.

2. El servidor identifica la operación como duplicada.

3. El servidor no crea un nuevo registro.

4. El servidor devuelve la confirmación correspondiente.

5. El flujo continúa desde el paso 26.



### FA-05: El usuario corrige un resultado



1. En el paso 21 o después de finalizar la rutina, el usuario detecta un resultado incorrecto.

2. El usuario selecciona la opción de corregir el registro.

3. El sistema presenta el valor registrado.

4. El usuario ingresa el valor correcto y confirma la modificación.

5. El sistema conserva el registro anterior y genera un cambio trazable o evento compensatorio.

6. El sistema guarda la corrección localmente con un nuevo `operation_id`.

7. La corrección se sincroniza siguiendo el mismo mecanismo que los demás resultados.



### FA-06: Se detecta un conflicto entre versiones



1. Durante la sincronización, el sistema detecta que el registro local y el registro del servidor poseen versiones incompatibles.

2. El sistema conserva ambas versiones.

3. El sistema informa que existe un conflicto pendiente.

4. Cuando el conflicto puede resolverse automáticamente, se aplica la política correspondiente.

5. Cuando el conflicto es relevante, el sistema solicita una resolución explícita.

6. Ninguna versión se elimina sin informar al usuario.



### FA-07: El usuario informa dolor o malestar



1. Durante el paso 9 del flujo básico, el usuario siente dolor, malestar o un síntoma inesperado.

2. El usuario pausa la rutina.

3. El sistema detiene el temporizador y conserva el progreso alcanzado.

4. El sistema recomienda detener la actividad y consultar a un profesional de la salud cuando corresponda.

5. Si existe autorización y un entrenador asignado, el sistema permite enviar un aviso privado.

6. El usuario puede finalizar la rutina o consultar una alternativa general previamente aprobada.

7. El sistema no realiza diagnósticos, no recomienda tratamientos ni garantiza que una alternativa sea segura.



### FA-08: El programa fue modificado por el entrenador



1. Al recuperar la conexión, el sistema detecta una versión más reciente del programa asignado.

2. Si la rutina todavía no comenzó, el sistema descarga la versión vigente del servidor.

3. Si la rutina ya comenzó, el sistema conserva la versión utilizada durante la sesión.

4. La nueva versión se aplicará a las próximas sesiones.

5. El sistema informa al usuario que su programa fue actualizado.



## Postcondiciones



### Postcondiciones de éxito



1. La rutina queda registrada como completada.

2. Los resultados quedan almacenados localmente.

3. Cada operación posee un identificador único y un estado de sincronización.

4. Los resultados quedan sincronizados con el servidor o visibles como pendientes.

5. Las correcciones quedan registradas de manera trazable.

6. El progreso básico del usuario queda actualizado.

7. No se generan registros duplicados.



### Postcondiciones mínimas



1. Si la sincronización falla, los resultados permanecen almacenados localmente.

2. Las operaciones pendientes o fallidas permanecen visibles.

3. Ningún registro se elimina sin informar al usuario.

4. Los conflictos conservan la información necesaria para su resolución.

5. La aplicación puede cerrarse o perder la conexión sin perder los resultados confirmados localmente.



## Relaciones consideradas para el diagrama



El caso de uso principal incluye:



- Consultar rutina.

- Consultar instrucciones.

- Utilizar temporizador.

- Registrar resultados.

- Guardar resultados localmente.

- Finalizar rutina.

- Consultar progreso.

- Sincronizar resultados.



Los siguientes comportamientos extienden el caso principal:



- Corregir resultado.

- Reintentar sincronización.

- Resolver conflicto.

- Informar dolor o malestar.

- Actualizar programa asignado.



## Diagrama UML



![Diagrama UML del caso de uso CU-02](./diagramas/CU_02_REALIZAR_RUTINA.svg)



---



# CU-03: Buscar un entrenador y reservar una sesión



## Objetivo



Permitir que un usuario encuentre un entrenador verificado, envíe una solicitud, reserve y pague una sesión, y reciba la asignación o adaptación de un programa básico.



## Actor principal



- Usuario.



## Actores secundarios



- Entrenador.

- Stripe, como proveedor externo de pagos y reembolsos.



## Precondiciones



1. El usuario debe tener una cuenta activa y haber iniciado sesión.

2. El usuario debe ser mayor de 18 años.

3. El usuario debe haber aceptado los términos y condiciones y la política de privacidad.

4. El usuario debe haber definido qué información autoriza a compartir con el entrenador.

5. El entrenador debe tener una cuenta activa.

6. La identidad y la documentación profesional del entrenador deben estar verificadas.

7. El perfil del entrenador debe estar publicado y habilitado para recibir solicitudes y cobros.

8. El entrenador debe tener disponibilidad registrada.

9. El servicio de pagos Stripe debe encontrarse disponible para procesar la operación.



## Flujo básico



1. El usuario accede al marketplace de entrenadores.

2. El sistema presenta los entrenadores disponibles.

3. El usuario aplica filtros por especialidad, tarifa, disponibilidad o modalidad de atención.

4. El sistema muestra los entrenadores que cumplen con los filtros.

5. El usuario selecciona un entrenador.

6. El sistema presenta el perfil del entrenador con:

&nbsp;  - Nombre o identificación pública.

&nbsp;  - Experiencia.

&nbsp;  - Especialidad.

&nbsp;  - Certificaciones.

&nbsp;  - Calificaciones.

&nbsp;  - Modalidad de atención.

&nbsp;  - Disponibilidad.

&nbsp;  - Tarifa.

&nbsp;  - Tiempo estimado de respuesta.

&nbsp;  - Información verificada e información declarada claramente diferenciadas.

7. El usuario consulta la información y selecciona la opción de enviar una solicitud.

8. El sistema solicita la confirmación de la información que el usuario autoriza a compartir.

9. El usuario confirma la autorización.

10. El sistema registra el consentimiento y envía la solicitud al entrenador.

11. El entrenador recibe la solicitud.

12. El entrenador consulta el objetivo, nivel, disponibilidad, duración, equipamiento, preferencias, registros básicos y limitaciones que el usuario autorizó a compartir.

13. El entrenador acepta la solicitud.

14. El sistema informa al usuario que la solicitud fue aceptada.

15. El usuario consulta el calendario del entrenador.

16. El sistema presenta los horarios disponibles.

17. El usuario selecciona una fecha y horario.

18. El sistema verifica nuevamente la disponibilidad y controla que no exista una reserva superpuesta.

19. El sistema presenta:

&nbsp;   - Fecha y horario.

&nbsp;   - Duración.

&nbsp;   - Tarifa de la sesión.

&nbsp;   - Comisión del 20% correspondiente a FitConnect.

&nbsp;   - Importe total.

&nbsp;   - Política de cancelación.

&nbsp;   - Condiciones de reprogramación.

&nbsp;   - Condiciones de reembolso.

20. El usuario acepta las condiciones y confirma que desea continuar.

21. El sistema envía la solicitud de pago a Stripe.

22. Stripe procesa el pago.

23. Stripe envía la confirmación mediante un webhook firmado.

24. El sistema valida la firma, el identificador y el estado del evento.

25. El sistema registra el pago de manera idempotente.

26. El sistema confirma la reserva.

27. El calendario actualiza el horario como ocupado.

28. El sistema notifica la reserva al usuario y al entrenador.

29. El entrenador selecciona una plantilla de programa.

30. El entrenador configura los ejercicios, orden, series, repeticiones o tiempo, descansos e instrucciones.

31. Si corresponde, el entrenador adapta el programa utilizando únicamente la información autorizada por el usuario.

32. El entrenador confirma la asignación del programa.

33. El sistema genera una versión del programa y registra autor, fecha, motivo y tipo de modificación.

34. El sistema informa al usuario que el programa fue asignado o actualizado.

35. El usuario consulta el programa recibido.



## Flujos alternativos



### FA-01: No se encuentran entrenadores con los filtros seleccionados



1. En el paso 4 del flujo básico, el sistema no encuentra entrenadores compatibles.

2. El sistema informa que no existen resultados.

3. El sistema permite quitar o modificar los filtros.

4. El usuario modifica los criterios de búsqueda.

5. El flujo continúa desde el paso 3.



### FA-02: El entrenador rechaza la solicitud



1. En el paso 13 del flujo básico, el entrenador rechaza la solicitud.

2. El sistema registra el rechazo.

3. El sistema informa al usuario.

4. El usuario puede regresar al marketplace y seleccionar otro entrenador.

5. El caso de uso finaliza sin crear una reserva.



### FA-03: La documentación del entrenador perdió vigencia



1. Antes de aceptar la solicitud o confirmar la reserva, el sistema detecta documentación vencida o una suspensión.

2. El sistema impide que el entrenador continúe recibiendo solicitudes o cobros.

3. El perfil deja de estar disponible para nuevas reservas.

4. El sistema informa al usuario que no puede continuar con ese entrenador.

5. El usuario puede regresar al marketplace.

6. El caso de uso finaliza sin procesar el pago.



### FA-04: El horario seleccionado ya no está disponible



1. En el paso 18 del flujo básico, el sistema detecta que el horario fue reservado o bloqueado.

2. El sistema no permite confirmar una doble reserva.

3. El sistema actualiza la disponibilidad.

4. El usuario selecciona otro horario.

5. El flujo continúa desde el paso 18.



### FA-05: El pago es rechazado



1. En el paso 22 del flujo básico, Stripe rechaza el pago.

2. El sistema registra el intento fallido.

3. La reserva no se confirma.

4. El horario no queda ocupado de forma definitiva.

5. El sistema informa al usuario el resultado.

6. El usuario puede utilizar otro medio de pago o cancelar la operación.

7. Si selecciona otro medio de pago, el flujo continúa desde el paso 21.



### FA-06: No se recibe confirmación del proveedor de pagos



1. Después del paso 21, el sistema no recibe una confirmación válida de Stripe.

2. La operación queda identificada como pendiente.

3. El sistema no informa el pago como exitoso.

4. El sistema reintenta o consulta el estado según la política definida.

5. La reserva no se confirma hasta recibir una respuesta válida.

6. El usuario puede consultar el estado de la operación.



### FA-07: Stripe envía el mismo evento más de una vez



1. En el paso 23 del flujo básico, Stripe envía un webhook cuyo identificador ya fue procesado.

2. El sistema reconoce el evento duplicado.

3. El sistema no genera un segundo pago ni una segunda reserva.

4. El sistema devuelve la confirmación técnica correspondiente.

5. El flujo continúa desde el estado previamente registrado.



### FA-08: El usuario cancela la sesión



1. El usuario accede a una reserva confirmada.

2. El usuario selecciona la opción de cancelar.

3. El sistema presenta la política aplicable.

4. El usuario confirma la cancelación.

5. El sistema actualiza el estado de la reserva.

6. El sistema libera el horario del entrenador.

7. Si corresponde, el sistema solicita a Stripe el reembolso definido por la política.

8. El sistema registra de manera trazable la cancelación y el resultado del reembolso.



### FA-09: El entrenador cancela la sesión



1. El entrenador selecciona una sesión confirmada.

2. El entrenador informa la cancelación.

3. El sistema registra el motivo y actualiza el estado.

4. El sistema notifica al usuario.

5. El sistema ofrece una reprogramación o el reembolso.

6. Si el usuario solicita el reembolso, el sistema procesa la operación mediante Stripe.

7. El sistema libera el horario correspondiente.



### FA-10: El usuario solicita una reprogramación



1. El usuario accede a una reserva confirmada.

2. El usuario selecciona la opción de reprogramar.

3. El sistema presenta los horarios disponibles.

4. El usuario selecciona una nueva fecha y horario.

5. El entrenador confirma el cambio cuando corresponda.

6. El sistema controla que no exista una reserva superpuesta.

7. El sistema actualiza la reserva y notifica a ambas partes.



### FA-11: El usuario informó una molestia o limitación



1. En el paso 31 del flujo básico, el entrenador consulta una molestia o limitación que el usuario autorizó a compartir.

2. El sistema muestra qué información declaró el usuario y cuándo lo hizo.

3. El entrenador puede:

&nbsp;  - Reducir la intensidad.

&nbsp;  - Reducir el volumen.

&nbsp;  - Modificar el rango de movimiento.

&nbsp;  - Reemplazar el ejercicio por otro previamente validado.

&nbsp;  - Pausar o excluir el ejercicio.

4. El entrenador registra la modificación y su motivo.

5. El sistema genera una nueva versión del programa.

6. El sistema aclara que FitConnect no realiza diagnósticos ni recomienda tratamientos.

7. Ante síntomas de alarma, se indica detener la actividad y consultar a un profesional de la salud.



### FA-12: El entrenador no puede asignar un programa adecuado



1. En el paso 31 del flujo básico, el entrenador determina que no puede realizar una adaptación adecuada con la información y herramientas disponibles.

2. El entrenador no asigna ejercicios que puedan representar un riesgo.

3. El entrenador solicita información adicional autorizada o recomienda consultar a un profesional de la salud.

4. El sistema registra la situación sin almacenar diagnósticos ni indicaciones médicas.

5. El programa permanece pendiente de asignación.



## Postcondiciones



### Postcondiciones de éxito



1. La solicitud queda aceptada.

2. El consentimiento para compartir información queda registrado.

3. El pago queda confirmado y registrado de manera idempotente.

4. La reserva queda confirmada sin superposición de horarios.

5. El usuario y el entrenador reciben la notificación correspondiente.

6. El programa queda asignado o adaptado.

7. La versión y las modificaciones del programa quedan registradas.

8. El historial conserva la solicitud, reserva, pago, consentimiento y asignación.



### Postcondiciones alternativas



1. Si la solicitud es rechazada, no se genera una reserva ni se procesa un pago.

2. Si el pago falla o permanece pendiente, la reserva no se confirma.

3. Si existe una cancelación, la reserva cambia de estado y el horario se libera.

4. Si corresponde un reembolso, la operación queda registrada y vinculada con el pago original.

5. Si el programa no puede asignarse, la situación queda registrada como pendiente.

6. Ningún entrenador con documentación vencida o suspendida puede recibir nuevas reservas o cobros.



## Relaciones consideradas para el diagrama



El caso de uso principal incluye:



- Buscar entrenador.

- Filtrar entrenadores.

- Consultar perfil.

- Verificar credenciales.

- Enviar solicitud.

- Autorizar información compartida.

- Aceptar o rechazar solicitud.

- Consultar disponibilidad.

- Seleccionar horario.

- Validar disponibilidad.

- Procesar pago.

- Confirmar reserva.

- Asignar o adaptar programa.

- Registrar versión del programa.

- Notificar resultado.



Los siguientes comportamientos extienden el caso principal:



- Modificar filtros.

- Cambiar medio de pago.

- Cancelar sesión.

- Reprogramar sesión.

- Procesar reembolso.

- Adaptar programa por una limitación.

- Reportar inconveniente o incidente.



## Diagrama UML



![Diagrama UML del caso de uso CU-03](./diagramas/CU_03_RESERVAR_ENTRENADOR.svg)



---



## Trazabilidad



Los tres casos de uso fueron seleccionados y validados por Gabriel (Product Manager) en la respuesta recibida el 30/09/2026.



Los flujos fueron definidos utilizando también la información relevada con:



- Enzo, como usuario activo.

- Ana, como Head de Entrenadores.

- Mara, como responsable de Legal, Riesgo y Privacidad.

- Diego, como CTO / DevOps.



El registro completo de las consultas y respuestas se encuentra disponible en [SEGUIMIENTO.md](../SEGUIMIENTO.md).



## Referencias



- Pressman, R. S. *Ingeniería del Software: Un Enfoque Práctico*. 7.ª edición. Capítulo 6.

- Kendall, K. E., & Kendall, J. E. *Análisis y Diseño de Sistemas*. 8.ª edición.

