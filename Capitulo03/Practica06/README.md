---
permalink: /Capitulo03/Practica06/
---

# Práctica 6. Crear tres agentes guiados con Agent Builder

## Objetivo de la práctica:

Al finalizar la práctica, serás capaz de:

- Crear tres agentes independientes desde Microsoft 365 Copilot para consultar procedimientos, redactar comunicaciones y analizar solicitudes.
- Configurar las instrucciones, los archivos de conocimiento y las indicaciones sugeridas que necesita cada agente.
- Comprobar respuestas, límites de actuación y resultados usando los recursos proporcionados.

## Duración aproximada:

- 65 minutos.

## Tabla de ayuda:

| Parámetro | Valor | Uso |
| --- | --- | --- |
| Herramienta | [Microsoft 365 Copilot](https://m365.cloud.microsoft.com/) → **Nuevo agente / Agent Builder** | Crear y probar los tres agentes. |
| Escenario | Unidad de Servicios Nova | Hilo conductor de los tres agentes. |
| Agente 1 | `Nova Procedimientos` | Consultar etapas, prioridades y escalamiento. |
| Agente 2 | `Nova Comunicaciones` | Preparar correos y mensajes ajustados a una guía. |
| Agente 3 | `Nova Seguimiento` | Consultar estados, responsables y prioridades del registro. |
| Fuente del agente 1 | [Manual_Atencion_Nova.docx](recursos/Manual_Atencion_Nova.docx) | Documento de procedimientos. |
| Fuente del agente 2 | [Guia_Comunicaciones_Nova.docx](recursos/Guia_Comunicaciones_Nova.docx) | Criterios y plantillas de comunicación. |
| Fuente del agente 3 | [Solicitudes_Nova.xlsx](recursos/Solicitudes_Nova.xlsx) | Registro de 36 solicitudes con tres hojas. |
| Almacenamiento del Excel | OneDrive del participante | Permitir comprobar permisos de conocimiento en la práctica 7. |

> **Importante:** Estos agentes son **agentes de consulta y generación de contenido**. No aprueban solicitudes, no escriben en el registro, no envían correos y no ejecutan acciones sobre sistemas operativos. La creación se realiza en **Agent Builder de Microsoft 365 Copilot**, no en otro producto.

## Instrucciones

La Unidad de Servicios Nova necesita atender consultas frecuentes sobre procesos internos, mantener comunicaciones coherentes y revisar un registro de solicitudes sin reconstruir manualmente la información. Crearás tres agentes para resolver estas necesidades. Cada agente tendrá su propio propósito y un origen de conocimiento delimitado.

### Tarea 1. Preparar los tres archivos y abrir Agent Builder (7 minutos)

**Paso 1.** Descargar el [manual de atención](recursos/Manual_Atencion_Nova.docx), la [guía de comunicaciones](recursos/Guia_Comunicaciones_Nova.docx) y el [registro de solicitudes](recursos/Solicitudes_Nova.xlsx). Abrir los tres archivos para comprobar que contienen las secciones y los datos descritos en la Tabla de ayuda.

**Paso 2.** Comprobar en `Solicitudes_Nova.xlsx` que la hoja `Solicitudes` contiene 36 registros identificados con códigos `SOL-2026-1001` a `SOL-2026-1036`, además de las hojas `Diccionario` y `Reglas`.

**Paso 3.** Entrar en OneDrive con la cuenta de Microsoft 365 del curso. Cargar `Solicitudes_Nova.xlsx` en una carpeta de trabajo propia, sin compartir el archivo todavía. Abrirlo desde OneDrive para comprobar que está disponible. Se utilizará como fuente de nube del agente 3 y para probar permisos en la práctica 7.

**Paso 4.** Abrir [Microsoft 365 Copilot](https://m365.cloud.microsoft.com/), seleccionar **Nuevo agente**, y elegir **Omitir para configurar / Skip to configure** si aparece. Identificar los controles de **Nombre**, **Descripción**, **Instrucciones**, **Conocimiento**, **Indicaciones sugeridas** y **Probar / Try it**.

### Tarea 2. Crear el agente Nova Procedimientos (16 minutos)

**Paso 1.** Introducir los siguientes valores en la configuración de un agente nuevo:

| Campo | Valor |
| --- | --- |
| Nombre | `Nova Procedimientos` |
| Descripción | `Ayuda a consultar el flujo de atención de solicitudes, prioridades y criterios de escalamiento de la Unidad de Servicios Nova.` |
| Conocimiento | Cargar desde el dispositivo `Manual_Atencion_Nova.docx`. |

**Paso 2.** Agregar el documento mediante **Conocimiento → Cargar** y esperar hasta que se muestre disponible. No agregar el libro Excel ni la guía de comunicaciones a este agente.

**Paso 3.** Copiar las siguientes instrucciones completas en **Instrucciones**:

**Instrucciones de Nova Procedimientos**

```text
Eres Nova Procedimientos, un asistente de consulta de la Unidad de Servicios Nova.
Tu fuente de referencia es Manual_Atencion_Nova.docx.

Ayuda a los colaboradores a identificar la etapa de una solicitud,
clasificarla según las reglas del manual y conocer cuándo escalarla.
Al explicar un procedimiento, devuelve pasos ordenados e identifica
la sección del manual que respalda la respuesta.

No solicites contraseñas, códigos de verificación, datos bancarios ni
identificadores personales completos. No prometas resoluciones ni
apruebes modificaciones. Si un paso o plazo no está documentado,
indica que no está especificado en el manual.

Si la solicitud es ambigua, pide únicamente los datos necesarios
para identificar el tipo de solicitud y el problema.
Responde en español con lenguaje claro y breve.
```

**Paso 4.** Configurar las indicaciones sugeridas:

| Título | Pregunta inicial |
| --- | --- |
| Clasificar solicitud | `¿Cómo clasificar una solicitud de acceso y qué datos mínimos necesito?` |
| Escalar incidente | `¿Cuándo se debe escalar un incidente con prioridad alta?` |
| Información insuficiente | `¿Qué hacer cuando faltan datos para atender una solicitud?` |

**Paso 5.** Abrir **Probar / Try it** y enviar el siguiente prompt:

**Prompt 1 — Consulta de procedimiento**

```text
Debo atender una solicitud por falla en el visor de informes,
que impide continuar un proceso prioritario. Según el manual,
¿qué prioridad y pasos corresponden? Indica las secciones utilizadas.
```

**Paso 6.** Verificar que la respuesta use el criterio de incidente con prioridad **Alta**, mencione el escalamiento a Coordinación de Servicio y no asegure la ejecución de cambios. Realizar una segunda consulta: `¿Puedo autorizar desde este agente la modificación de un permiso?` Comprobar que el agente no se atribuya facultades de aprobación.

**Paso 7.** Seleccionar **Crear / Create** y confirmar que `Nova Procedimientos` aparece entre los agentes propios.

### Tarea 3. Crear el agente Nova Comunicaciones (15 minutos)

**Paso 1.** Seleccionar **Nuevo agente** y completar estos valores:

| Campo | Valor |
| --- | --- |
| Nombre | `Nova Comunicaciones` |
| Descripción | `Ayuda a redactar borradores de comunicación de recepción, seguimiento, aclaración y cierre de solicitudes.` |
| Conocimiento | Cargar `Guia_Comunicaciones_Nova.docx` desde el dispositivo. |

**Paso 2.** Agregar como instrucciones del agente:

**Instrucciones de Nova Comunicaciones**

```text
Eres Nova Comunicaciones. Tu tarea es preparar borradores de
comunicación según Guia_Comunicaciones_Nova.docx.

Cuando el usuario solicite un mensaje, identifica su destinatario,
propósito, código de solicitud SOL, estado confirmado y siguiente paso.
Usa la plantilla pertinente y adapta el tono a la audiencia.

Entrega el asunto y el cuerpo del mensaje por separado. No inventes
fechas de aprobación, cumplimiento, responsables ni acciones ejecutadas.
Si falta un dato indispensable, solicita ese dato o deja una marca
[PENDIENTE DE CONFIRMAR] en el borrador.

No incluyas contraseñas ni datos bancarios y no afirmes que enviaste
un correo. Tu función es redactar para revisión del colaborador.
Responde en español con estilo claro, respetuoso y operativo.
```

**Paso 3.** Agregar las indicaciones sugeridas:

| Título | Pregunta inicial |
| --- | --- |
| Acuse de recibo | `Prepara un acuse de recibo para una solicitud.` |
| Solicitar datos | `Redacta una solicitud breve de información faltante.` |
| Actualización de estado | `Redacta un seguimiento para coordinación con asunto y cuerpo.` |

**Paso 4.** Abrir **Probar** y enviar:

**Prompt 2 — Borrador de seguimiento**

```text
Redacta un correo de seguimiento para el colaborador que reportó
SOL-2026-1003. Estado confirmado: Pendiente de información.
La acción requerida es precisar el mensaje de error y el servicio
impactado. No tenemos fecha confirmada de resolución.
Usa la guía de comunicaciones y entrega asunto y cuerpo.
```

**Paso 5.** Comprobar que el asunto contiene `SOL-2026-1003`, que se solicita solo la información indicada, que no se promete una fecha y que el agente no afirma haber enviado un mensaje.

**Paso 6.** Enviar una segunda consulta sin información suficiente:

**Prompt 3 — Información incompleta**

```text
Prepara un correo de cierre de una solicitud, pero no tengo el
código ni la fecha en que fue resuelta.
```

**Paso 7.** Verificar que el agente pida los datos faltantes o utilice la marca `[PENDIENTE DE CONFIRMAR]` sin inventarlos. Seleccionar **Crear** y confirmar que `Nova Comunicaciones` quedó guardado.

### Tarea 4. Crear el agente Nova Seguimiento (19 minutos)

**Paso 1.** Seleccionar **Nuevo agente** y asignar:

| Campo | Valor |
| --- | --- |
| Nombre | `Nova Seguimiento` |
| Descripción | `Consulta el registro de solicitudes de la Unidad de Servicios Nova para identificar estados, prioridades, responsables y acciones siguientes.` |
| Conocimiento | Libro `Solicitudes_Nova.xlsx` almacenado en OneDrive. |

**Paso 2.** Seleccionar en **Conocimiento** **Examinar / Browse / Adjuntar archivos de nube** y localizar el libro cargado a OneDrive en la Tarea 1. Seleccionar esa **fuente de nube**, no la opción de carga local o archivo incorporado. Este detalle permitirá probar el acceso al archivo en la práctica 7.

**Paso 3.** Abrir la configuración de la fuente y comprobar que se muestre el nombre correcto. Si indica **Preparando / Preparing**, esperar a que esté disponible antes de atribuir al agente fallos de análisis.

**Paso 4.** Introducir las siguientes instrucciones:

**Instrucciones de Nova Seguimiento**

```text
Eres Nova Seguimiento, asistente de consulta del registro de solicitudes.
Utiliza como fuente Solicitudes_Nova.xlsx, especialmente la hoja
Solicitudes y las definiciones de Diccionario y Reglas.

Cuando el usuario consulte un código SOL, indica tipo, prioridad,
estado, responsable, fecha objetivo y acción siguiente, sin inventar
campos. Para resúmenes, cuenta registros reales y muestra el total
usado como denominador antes de calcular porcentajes.

Distingue las fechas objetivo de las fechas de cierre. No afirmes
que una solicitud está vencida sin verificar los días hábiles.
No edites el archivo ni afirmes cerrar, crear o actualizar solicitudes.
No utilices otros expedientes para completar valores ausentes.
Cuando la fuente no esté disponible o falte un dato, indícalo.
Responde en español y presenta tablas breves cuando sean útiles.
```

**Paso 5.** Añadir estas indicaciones sugeridas:

| Título | Pregunta inicial |
| --- | --- |
| Estado de caso | `Consulta el estado y la próxima acción de SOL-2026-1003.` |
| Resumen por estado | `Cuenta los casos por estado e indica el total de registros.` |
| Pendientes de alta prioridad | `Enumera los incidentes de prioridad Alta que no están resueltos.` |

**Paso 6.** Abrir **Probar** y enviar:

**Prompt 4 — Consulta verificable**

```text
Revisa Solicitudes_Nova.xlsx y dime cuántos registros hay en
la hoja Solicitudes. Resume sus estados en una tabla con cantidad
y porcentaje del total. Incluye la fórmula del porcentaje y
comprueba que las cantidades suman el total.
```

**Paso 7.** Contrastar el total con las **36 filas de datos** del Excel y comprobar que los porcentajes suman aproximadamente el **100 %** (pueden existir diferencias por redondeo).

**Paso 8.** Enviar una consulta puntual:

**Prompt 5 — Verificación de registro**

```text
¿Qué estado, prioridad, responsable, fecha objetivo y acción
siguiente aparecen para SOL-2026-1003? Si falta un campo en el
registro, indícalo y no lo completes por suposición.
```

**Paso 9.** Comparar los valores con la fila exacta de `SOL-2026-1003` en Excel. Seleccionar **Crear** para guardar el tercer agente.

### Tarea 5. Verificar la autonomía de los tres agentes (8 minutos)

**Paso 1.** Abrir **Agentes propios / Mis agentes** o el listado equivalente en Copilot y localizar `Nova Procedimientos`, `Nova Comunicaciones` y `Nova Seguimiento`.

**Paso 2.** Abrir una conversación nueva con cada uno, sin reutilizar la sesión de configuración, y repetir una de sus preguntas sugeridas. Verificar que cada agente responda según su conocimiento y propósito específicos.

**Paso 3.** Preguntar a `Nova Seguimiento` por el código `SOL-2026-9999`. Comprobar que no inventa un caso inexistente.

**Paso 4.** Revisar que `Nova Comunicaciones` no tenga el registro Excel como fuente y que `Nova Procedimientos` no tenga la guía de comunicaciones. Comprobar que `Nova Seguimiento` conserva el archivo de **OneDrive** como fuente.

**Paso 5.** Conservar los tres agentes en el espacio propio de Microsoft 365 Copilot para utilizarlos en la práctica 7; no habilitar uso compartido de toda la organización.

### Resultado esperado

Se han creado y guardado **tres agentes independientes** en Microsoft 365 Copilot: `Nova Procedimientos` responde consultas fundamentadas en el manual de atención; `Nova Comunicaciones` redacta mensajes en formatos de recepción, seguimiento, aclaración o cierre sin inventar datos ni enviar correos; y `Nova Seguimiento` consulta las **36 solicitudes** de un libro Excel almacenado en OneDrive, cuenta estados y verifica registros por identificador. Cada agente conserva instrucciones, conocimiento e indicaciones sugeridas. No debe existir ninguna conexión que edite registros ni ejecute acciones de negocio.

[Volver al capítulo 3](../)
