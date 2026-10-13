# 6. Modelado de Base de Datos

Para el modelado de datos de FitConnect se tomó como referencia la base de datos central PostgreSQL confirmada para el MVP. El modelo se concentra en la información necesaria para configurar usuarios, administrar programas y ejercicios, asignar programas, registrar entrenamientos y gestionar reservas con entrenadores.

La base SQLite del dispositivo no se representa como un segundo modelo E-R completo, ya que almacena una copia local de determinados programas, ejercicios, sesiones incompletas, registros manuales y operaciones pendientes de sincronización. El modelo presentado a continuación describe las entidades principales del dominio que serán persistidas centralmente.

## A) Principales tablas de FitConnect

### 1. USUARIO

Almacena la identidad de la persona que utiliza FitConnect y los datos mínimos necesarios para configurar su perfil y recomendarle un programa.

| Campo | Tipo de dato | Clave o restricción | Descripción |
|---|---|---|---|
| `id_usuario` | `BIGSERIAL` | PK | Identificador único del usuario. |
| `email` | `VARCHAR(150)` | UNIQUE, NOT NULL | Correo utilizado para acceder a la cuenta. |
| `hash_contrasena` | `VARCHAR(255)` | NOT NULL | Contraseña almacenada de manera segura mediante un hash. |
| `nombre_o_alias` | `VARCHAR(100)` | NOT NULL | Nombre o alias visible en la plataforma. |
| `fecha_nacimiento` | `DATE` | NOT NULL | Permite comprobar que el usuario sea mayor de 18 años. |
| `objetivo` | `VARCHAR(100)` | NOT NULL | Objetivo principal de entrenamiento. |
| `nivel_experiencia` | `VARCHAR(30)` | NOT NULL | Nivel declarado por el usuario. |
| `dias_disponibles` | `SMALLINT` | NOT NULL | Cantidad de días semanales disponibles. |
| `duracion_sesion_min` | `SMALLINT` | NOT NULL | Duración disponible para cada sesión. |
| `equipamiento_principal` | `VARCHAR(120)` | NOT NULL | Equipamiento principal del que dispone. |
| `preferencia_entrenamiento` | `VARCHAR(120)` | NULL | Preferencia principal informada por el usuario. |
| `limitacion_declarada` | `TEXT` | NULL | Molestia o limitación informada voluntariamente. |
| `fecha_alta` | `TIMESTAMP` | NOT NULL | Fecha y hora de creación de la cuenta. |
| `activo` | `BOOLEAN` | NOT NULL | Indica si la cuenta se encuentra activa. |

**Clave primaria:** `id_usuario`.

---

### 2. ENTRENADOR

Almacena la información profesional de los entrenadores que ofrecen sus servicios dentro del marketplace.

| Campo | Tipo de dato | Clave o restricción | Descripción |
|---|---|---|---|
| `id_entrenador` | `BIGSERIAL` | PK | Identificador único del entrenador. |
| `especialidad` | `VARCHAR(100)` | NOT NULL | Especialidad profesional declarada. |
| `descripcion_profesional` | `TEXT` | NOT NULL | Presentación y experiencia profesional. |
| `anios_experiencia` | `SMALLINT` | NOT NULL | Años de experiencia declarados. |
| `modalidad_atencion` | `VARCHAR(30)` | NOT NULL | Modalidad en la que presta el servicio. |
| `tarifa_sesion` | `NUMERIC(10,2)` | NOT NULL | Precio de una sesión individual. |
| `estado_verificacion` | `VARCHAR(20)` | NOT NULL | Estado de la verificación de identidad y credenciales. |
| `fecha_publicacion` | `TIMESTAMP` | NULL | Momento desde el cual el perfil quedó publicado. |
| `activo_marketplace` | `BOOLEAN` | NOT NULL | Indica si el perfil puede aparecer en las búsquedas. |

**Clave primaria:** `id_entrenador`.

---

### 3. EJERCICIO

Almacena los ejercicios disponibles en la biblioteca de FitConnect.

| Campo | Tipo de dato | Clave o restricción | Descripción |
|---|---|---|---|
| `id_ejercicio` | `BIGSERIAL` | PK | Identificador único del ejercicio. |
| `nombre` | `VARCHAR(120)` | NOT NULL | Nombre del ejercicio. |
| `descripcion` | `TEXT` | NOT NULL | Explicación general de su ejecución. |
| `nivel` | `VARCHAR(30)` | NOT NULL | Nivel de dificultad. |
| `equipamiento_requerido` | `VARCHAR(120)` | NOT NULL | Equipamiento principal necesario. |
| `url_video` | `TEXT` | NULL | Referencia al video almacenado en el servicio de objetos. |
| `instrucciones_seguridad` | `TEXT` | NOT NULL | Advertencias e indicaciones de seguridad. |
| `activo` | `BOOLEAN` | NOT NULL | Indica si el ejercicio está disponible. |

**Clave primaria:** `id_ejercicio`.

---

### 4. PROGRAMA

Almacena los programas de entrenamiento y sus versiones. Cada modificación relevante genera una nueva fila, de modo que pueda conservarse la versión anterior.

| Campo | Tipo de dato | Clave o restricción | Descripción |
|---|---|---|---|
| `id_programa` | `BIGSERIAL` | PK | Identificador único de una versión del programa. |
| `codigo_programa` | `UUID` | NOT NULL | Identifica al mismo programa a través de sus distintas versiones. |
| `id_entrenador_creador` | `BIGINT` | FK, NULL | Entrenador que creó o adaptó el programa; es nulo si fue creado por FitConnect. |
| `id_version_anterior` | `BIGINT` | FK, NULL | Versión precedente del mismo programa. |
| `nombre` | `VARCHAR(120)` | NOT NULL | Nombre del programa. |
| `objetivo` | `VARCHAR(100)` | NOT NULL | Objetivo al que está orientado. |
| `nivel` | `VARCHAR(30)` | NOT NULL | Nivel de experiencia requerido. |
| `duracion_semanas` | `SMALLINT` | NOT NULL | Duración prevista del programa. |
| `tipo_acceso` | `VARCHAR(20)` | NOT NULL | Indica si es gratuito, premium o personalizado. |
| `numero_version` | `INTEGER` | NOT NULL | Número de versión. |
| `motivo_cambio` | `TEXT` | NULL | Motivo por el cual se generó la versión. |
| `fecha_creacion` | `TIMESTAMP` | NOT NULL | Fecha y hora de creación de la versión. |
| `estado` | `VARCHAR(20)` | NOT NULL | Estado del programa: borrador, publicado o archivado. |

**Clave primaria:** `id_programa`.

**Claves foráneas:**

- `id_entrenador_creador` referencia a `ENTRENADOR(id_entrenador)`.
- `id_version_anterior` referencia a `PROGRAMA(id_programa)`.

La combinación `codigo_programa` y `numero_version` deberá ser única.

---

### 5. PROGRAMA_EJERCICIO

Tabla asociativa que indica qué ejercicios integran cada programa y cómo deben realizarse.

| Campo | Tipo de dato | Clave o restricción | Descripción |
|---|---|---|---|
| `id_programa_ejercicio` | `BIGSERIAL` | PK | Identificador único del ejercicio dentro del programa. |
| `id_programa` | `BIGINT` | FK, NOT NULL | Programa al que pertenece la configuración. |
| `id_ejercicio` | `BIGINT` | FK, NOT NULL | Ejercicio incorporado al programa. |
| `numero_sesion` | `SMALLINT` | NOT NULL | Número de sesión dentro del programa. |
| `orden` | `SMALLINT` | NOT NULL | Posición del ejercicio dentro de la sesión. |
| `cantidad_series` | `SMALLINT` | NOT NULL | Cantidad de series previstas. |
| `repeticiones` | `SMALLINT` | NULL | Repeticiones previstas cuando corresponda. |
| `duracion_segundos` | `INTEGER` | NULL | Duración prevista para ejercicios medidos por tiempo. |
| `descanso_segundos` | `INTEGER` | NOT NULL | Tiempo de descanso indicado. |
| `instrucciones` | `TEXT` | NULL | Instrucciones particulares dentro del programa. |

**Clave primaria:** `id_programa_ejercicio`.

**Claves foráneas:**

- `id_programa` referencia a `PROGRAMA(id_programa)`.
- `id_ejercicio` referencia a `EJERCICIO(id_ejercicio)`.

La combinación `id_programa`, `numero_sesion` y `orden` deberá ser única para evitar dos ejercicios en la misma posición.

---

### 6. ASIGNACION_PROGRAMA

Registra qué versión de un programa fue recomendada, seleccionada o asignada a un usuario.

| Campo | Tipo de dato | Clave o restricción | Descripción |
|---|---|---|---|
| `id_asignacion` | `BIGSERIAL` | PK | Identificador único de la asignación. |
| `id_usuario` | `BIGINT` | FK, NOT NULL | Usuario que recibe el programa. |
| `id_programa` | `BIGINT` | FK, NOT NULL | Versión concreta del programa asignado. |
| `id_entrenador` | `BIGINT` | FK, NULL | Entrenador responsable, si la asignación fue realizada por uno. |
| `origen` | `VARCHAR(20)` | NOT NULL | Indica si fue automática, elegida por el usuario o asignada por un entrenador. |
| `motivo_recomendacion` | `TEXT` | NULL | Explicación de la recomendación automática. |
| `fecha_asignacion` | `TIMESTAMP` | NOT NULL | Momento de la asignación. |
| `fecha_inicio` | `DATE` | NULL | Fecha en la que el usuario comienza el programa. |
| `estado` | `VARCHAR(20)` | NOT NULL | Estado: pendiente, activa, finalizada o cancelada. |
| `confirmada_usuario` | `BOOLEAN` | NOT NULL | Indica si el usuario confirmó el programa recomendado. |

**Clave primaria:** `id_asignacion`.

**Claves foráneas:**

- `id_usuario` referencia a `USUARIO(id_usuario)`.
- `id_programa` referencia a `PROGRAMA(id_programa)`.
- `id_entrenador` referencia a `ENTRENADOR(id_entrenador)`.

---

### 7. SESION_ENTRENAMIENTO

Registra cada ejecución concreta de una rutina por parte del usuario. Constituye la cabecera del historial de entrenamientos.

| Campo | Tipo de dato | Clave o restricción | Descripción |
|---|---|---|---|
| `id_sesion` | `BIGSERIAL` | PK | Identificador único de la sesión realizada. |
| `id_asignacion` | `BIGINT` | FK, NOT NULL | Programa asignado que se estaba realizando. |
| `operation_id` | `UUID` | UNIQUE, NOT NULL | Identificador generado en el dispositivo para evitar duplicaciones. |
| `fecha_hora_inicio` | `TIMESTAMP` | NOT NULL | Inicio de la sesión. |
| `fecha_hora_fin` | `TIMESTAMP` | NULL | Finalización de la sesión. |
| `estado` | `VARCHAR(20)` | NOT NULL | Estado: iniciada, completada, pausada o abandonada. |
| `origen_registro` | `VARCHAR(20)` | NOT NULL | Indica si fue registrada online u offline. |
| `fecha_recepcion_servidor` | `TIMESTAMP` | NULL | Momento en que el servidor recibió la operación. |
| `observaciones` | `TEXT` | NULL | Comentario general del usuario sobre la sesión. |

**Clave primaria:** `id_sesion`.

**Clave foránea:** `id_asignacion` referencia a `ASIGNACION_PROGRAMA(id_asignacion)`.

---

### 8. RESULTADO_EJERCICIO

Almacena el resultado obtenido en cada serie realizada dentro de una sesión. También permite conservar las correcciones sin eliminar el dato anterior.

| Campo | Tipo de dato | Clave o restricción | Descripción |
|---|---|---|---|
| `id_resultado` | `BIGSERIAL` | PK | Identificador único del resultado. |
| `id_sesion` | `BIGINT` | FK, NOT NULL | Sesión en la que se registró. |
| `id_programa_ejercicio` | `BIGINT` | FK, NOT NULL | Ejercicio y configuración previstos por el programa. |
| `id_resultado_anterior` | `BIGINT` | FK, NULL | Resultado anterior al que corrige esta fila. |
| `operation_id` | `UUID` | UNIQUE, NOT NULL | Identificador de la operación para sincronización idempotente. |
| `numero_serie` | `SMALLINT` | NOT NULL | Número de la serie realizada. |
| `repeticiones_realizadas` | `SMALLINT` | NULL | Repeticiones registradas. |
| `duracion_real_segundos` | `INTEGER` | NULL | Duración registrada cuando el ejercicio se mide por tiempo. |
| `resultado_alcanzado` | `VARCHAR(100)` | NULL | Marca, distancia u otro resultado relevante. |
| `fecha_registro` | `TIMESTAMP` | NOT NULL | Fecha y hora originales del registro. |
| `vigente` | `BOOLEAN` | NOT NULL | Indica si es la versión vigente del resultado. |

**Clave primaria:** `id_resultado`.

**Claves foráneas:**

- `id_sesion` referencia a `SESION_ENTRENAMIENTO(id_sesion)`.
- `id_programa_ejercicio` referencia a `PROGRAMA_EJERCICIO(id_programa_ejercicio)`.
- `id_resultado_anterior` referencia a `RESULTADO_EJERCICIO(id_resultado)`.

---

### 9. RESERVA

Registra las solicitudes y reservas de sesiones individuales entre usuarios y entrenadores.

| Campo | Tipo de dato | Clave o restricción | Descripción |
|---|---|---|---|
| `id_reserva` | `BIGSERIAL` | PK | Identificador único de la reserva. |
| `id_usuario` | `BIGINT` | FK, NOT NULL | Usuario que solicita la sesión. |
| `id_entrenador` | `BIGINT` | FK, NOT NULL | Entrenador solicitado. |
| `fecha_hora_inicio` | `TIMESTAMP` | NOT NULL | Fecha y hora de inicio reservadas. |
| `fecha_hora_fin` | `TIMESTAMP` | NOT NULL | Fecha y hora de finalización previstas. |
| `estado` | `VARCHAR(20)` | NOT NULL | Estado: solicitada, aceptada, confirmada, realizada, cancelada o reprogramada. |
| `modalidad` | `VARCHAR(20)` | NOT NULL | Modalidad de la sesión, por ejemplo videollamada. |
| `importe_total` | `NUMERIC(10,2)` | NOT NULL | Importe informado al usuario. |
| `porcentaje_comision` | `NUMERIC(5,2)` | NOT NULL | Comisión de FitConnect, inicialmente del 20 %. |
| `referencia_pago_externa` | `VARCHAR(100)` | NULL | Identificador de la operación procesada mediante Stripe. |
| `fecha_creacion` | `TIMESTAMP` | NOT NULL | Fecha y hora de creación de la solicitud. |
| `motivo_cancelacion` | `TEXT` | NULL | Motivo de cancelación cuando corresponda. |

**Clave primaria:** `id_reserva`.

**Claves foráneas:**

- `id_usuario` referencia a `USUARIO(id_usuario)`.
- `id_entrenador` referencia a `ENTRENADOR(id_entrenador)`.

Además de las claves, deberá existir una regla que impida confirmar dos reservas superpuestas para un mismo entrenador.

## B) Modelo Entidad-Relación

El diagrama E-R representa las nueve entidades identificadas, sus relaciones y las cardinalidades correspondientes. Para mantener legible el modelo conceptual, los campos no se repiten dentro de las entidades. Las claves foráneas necesarias se detallan debajo del diagrama.

[Abrir el diagrama E-R editable](./DER_FITCONNECT.drawio)

### Relaciones y cardinalidades

| Entidades relacionadas | Cardinalidad | Interpretación |
|---|---|---|
| `USUARIO` - `RESERVA` | 1:N | Un usuario puede realizar muchas reservas; cada reserva pertenece a un único usuario. |
| `ENTRENADOR` - `RESERVA` | 1:N | Un entrenador puede recibir muchas reservas; cada reserva corresponde a un único entrenador. |
| `ENTRENADOR` - `PROGRAMA` | 1:N opcional | Un entrenador puede crear diferentes programas. Un programa puede ser creado por un entrenador o automáticamente por FitConnect. |
| `PROGRAMA` - `EJERCICIO` | N:M | Un programa contiene muchos ejercicios y un ejercicio puede utilizarse en muchos programas. Se resuelve mediante `PROGRAMA_EJERCICIO`. |
| `USUARIO` - `PROGRAMA` | N:M | Un usuario puede recibir distintos programas y un programa puede asignarse a muchos usuarios. Se resuelve mediante `ASIGNACION_PROGRAMA`. |
| `ENTRENADOR` - `ASIGNACION_PROGRAMA` | 1:N opcional | Un entrenador puede realizar muchas asignaciones; una asignación puede ser automática y no tener entrenador. |
| `ASIGNACION_PROGRAMA` - `SESION_ENTRENAMIENTO` | 1:N | Una asignación puede originar muchas sesiones; cada sesión corresponde a una asignación. |
| `SESION_ENTRENAMIENTO` - `RESULTADO_EJERCICIO` | 1:N | Una sesión contiene muchos resultados; cada resultado pertenece a una sola sesión. |
| `PROGRAMA_EJERCICIO` - `RESULTADO_EJERCICIO` | 1:N | Una configuración de ejercicio puede aparecer en los resultados de muchas sesiones. |
| `PROGRAMA` - `PROGRAMA` | 1:1 opcional | Una versión puede señalar a su versión anterior para conservar el historial de modificaciones. |
| `RESULTADO_EJERCICIO` - `RESULTADO_EJERCICIO` | 1:1 opcional | Una corrección puede referenciar al resultado anterior sin sobrescribirlo. |

### Claves foráneas identificadas

- `PROGRAMA.id_entrenador_creador` → `ENTRENADOR.id_entrenador`.
- `PROGRAMA.id_version_anterior` → `PROGRAMA.id_programa`.
- `PROGRAMA_EJERCICIO.id_programa` → `PROGRAMA.id_programa`.
- `PROGRAMA_EJERCICIO.id_ejercicio` → `EJERCICIO.id_ejercicio`.
- `ASIGNACION_PROGRAMA.id_usuario` → `USUARIO.id_usuario`.
- `ASIGNACION_PROGRAMA.id_programa` → `PROGRAMA.id_programa`.
- `ASIGNACION_PROGRAMA.id_entrenador` → `ENTRENADOR.id_entrenador`.
- `SESION_ENTRENAMIENTO.id_asignacion` → `ASIGNACION_PROGRAMA.id_asignacion`.
- `RESULTADO_EJERCICIO.id_sesion` → `SESION_ENTRENAMIENTO.id_sesion`.
- `RESULTADO_EJERCICIO.id_programa_ejercicio` → `PROGRAMA_EJERCICIO.id_programa_ejercicio`.
- `RESULTADO_EJERCICIO.id_resultado_anterior` → `RESULTADO_EJERCICIO.id_resultado`.
- `RESERVA.id_usuario` → `USUARIO.id_usuario`.
- `RESERVA.id_entrenador` → `ENTRENADOR.id_entrenador`.

## C) Decisiones del modelo

### ¿Qué consideraciones de normalización se tuvieron en cuenta?

El modelo fue organizado hasta la tercera forma normal como criterio general:

1. **Primera forma normal (1FN):** cada tabla posee una clave primaria y cada campo almacena un único valor. No se incluyeron grupos repetidos de ejercicios, sesiones o resultados dentro de una misma fila.
2. **Segunda forma normal (2FN):** los atributos dependen de la totalidad de la identificación lógica del registro. Por ejemplo, las series, repeticiones, duración y descansos de `PROGRAMA_EJERCICIO` describen la incorporación de un ejercicio en una sesión concreta del programa, no solamente al programa o al ejercicio por separado.
3. **Tercera forma normal (3FN):** se evitó repetir información que corresponde a otra entidad. Una reserva conserva los identificadores del usuario y del entrenador, pero no duplica sus nombres, correos o especialidades. De igual manera, un resultado referencia al ejercicio configurado en el programa, en lugar de volver a guardar toda su descripción.

También se tuvieron en cuenta las siguientes decisiones:

- Los ejercicios fueron separados de los programas para poder reutilizarlos.
- La información profesional de los entrenadores se almacena en `ENTRENADOR`.
- Las asignaciones se separaron de los programas para que una misma versión pueda ser utilizada por varios usuarios.
- Las sesiones y sus resultados se separaron en una estructura de cabecera y detalle.
- El progreso no se duplicó como un valor fijo, ya que puede calcularse a partir del historial.
- Los videos y documentos no se almacenan como archivos binarios dentro de PostgreSQL; se conserva únicamente su referencia al almacenamiento de objetos.
- Los campos sensibles deberán estar protegidos mediante controles de acceso, cifrado y auditoría, aunque puedan residir inicialmente en la misma base física.

### ¿Se identificó alguna tabla asociativa para resolver relaciones N:M?

Sí. La principal tabla asociativa es `PROGRAMA_EJERCICIO`, que resuelve la relación N:M entre `PROGRAMA` y `EJERCICIO`.

Esta tabla no solamente relaciona ambas entidades, sino que también conserva atributos propios de la relación, como el número de sesión, el orden, las series, las repeticiones, la duración y el descanso.

También existen dos entidades que resuelven relaciones N:M a lo largo del tiempo y poseen significado propio dentro del dominio:

- `ASIGNACION_PROGRAMA` relaciona usuarios con programas y registra quién realizó la asignación, cuándo se efectuó, su origen y su estado.
- `RESERVA` relaciona usuarios con entrenadores y conserva el horario, el estado, la modalidad y la información económica de la sesión.

### ¿Cómo se manejaría el historial de entrenamientos y progreso del usuario?

El historial se conservará mediante `SESION_ENTRENAMIENTO` y `RESULTADO_EJERCICIO`:

1. Cada vez que un usuario inicia una rutina se crea una fila en `SESION_ENTRENAMIENTO`.
2. Cada serie realizada se registra como una fila en `RESULTADO_EJERCICIO`, incluyendo repeticiones, duración o resultado alcanzado.
3. Los registros poseen fecha y hora para poder reconstruir la evolución cronológica.
4. Una corrección no sobrescribe silenciosamente el dato anterior. Se crea un nuevo resultado que referencia a `id_resultado_anterior`, y se identifica cuál es la versión vigente.
5. Cada operación creada en el dispositivo utiliza un `operation_id` único. El servidor aplica idempotencia para que un reintento de sincronización no genere registros duplicados.
6. Los registros realizados sin conexión conservan su fecha y hora original y se sincronizan cuando se recupera la conectividad.
7. Las sesiones completadas, el volumen de entrenamiento, la continuidad y los récords personales se calculan a partir de estos registros. Por ese motivo no se crea una tabla de progreso con valores duplicados.
8. Los programas también mantienen versiones, permitiendo conocer con qué versión entrenó el usuario y evitando que una modificación posterior altere el historial.

Este enfoque permite reconstruir qué entrenamiento realizó el usuario, cuándo lo realizó, qué resultados obtuvo, qué correcciones efectuó y cuál fue la versión del programa utilizada.

## Referencias

- Kendall, K. E. y Kendall, J. E. (2011). *Análisis y Diseño de Sistemas*. 8.ª ed. Pearson. Capítulos 7 y 13.
- Pressman, R. S. (2010). *Ingeniería del Software: Un Enfoque Práctico*. 7.ª ed. McGraw-Hill. Capítulos 5, 6 y 8.

## Fuente de la información relevada

- [SEGUIMIENTO.md](./SEGUIMIENTO.md), especialmente las definiciones proporcionadas por Diego el 25/09/2026 y el 30/09/2026.
