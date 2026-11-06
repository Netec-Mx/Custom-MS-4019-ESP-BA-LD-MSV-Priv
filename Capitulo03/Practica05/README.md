---
permalink: /Capitulo03/Practica05/
---

# Práctica 5. Creación de un agente propio con Agent Builder

## Objetivo de la práctica:

Al finalizar la práctica, serás capaz de:

- Delimitar una necesidad cotidiana del participante y convertirla en el propósito de un agente de Microsoft 365 Copilot.
- Crear un agente con Agent Builder, asignar instrucciones y conocimientos pertinentes y comprobar sus respuestas.
- Guardar un agente personalizado que pueda utilizarse en las tareas del día a día dentro de las funcionalidades autorizadas.

## Duración aproximada:

- 50 minutos.

## Tabla de ayuda:

| Parámetro | Valor | Uso |
| --- | --- | --- |
| Herramienta | [Microsoft Copilot](https://m365.cloud.microsoft.com/) → **Nuevo agente** | Crear un agente mediante Agent Builder. |
| Caso prioritario | Necesidad real elegida por el participante o caso de uso facilitado por el cliente | Determinar el objetivo de la práctica. |
| Caso operativo de respaldo | Consulta de decisiones y compromisos de Project Nexus | Permitir una ejecución completa cuando todavía no exista un caso personalizado aprobado. |
| Nombre para el caso de respaldo | `Nexus Acuerdos` | Identificar el agente sin confundirlo con el de la práctica 4. |
| Fuentes de respaldo | [Comité NXS-002](../../Capitulo02/Practica02/recursos/Nexus_02_Comite_2026-08-27.docx), [minuta NXS-003](../../Capitulo02/Practica02/recursos/Nexus_03_Minuta_2026-09-24.docx), [plan de entregables](../../Capitulo02/Practica02/recursos/Nexus_05_Plan_entregables.xlsx) | Dar soporte a consultas de acuerdos y fechas. |

> **Importante:** El temario indica que el cliente proporcionará casos de uso particulares. Hasta contar con ellos, el participante puede seleccionar una necesidad propia autorizada o utilizar el caso operativo de respaldo. Este ejemplo no debe interpretarse como un caso aprobado por el cliente.

## Instrucciones

Cada participante elegirá una necesidad de su trabajo para crear su propio agente con Agent Builder. Durante el ejercicio desarrollará el agente, probará respuestas y resolverá con apoyo del instructor las dudas de configuración que surjan durante su construcción.

### Tarea 1. Seleccionar y delimitar el caso de uso (8 minutos)

**Paso 1.** Elegir una tarea frecuente que actualmente requiera revisar información o producir una respuesta repetible. Si se ha recibido un caso aprobado del cliente, usarlo; de lo contrario, seleccionar una necesidad propia que no implique datos personales ni información sensible.

**Paso 2.** Definir mentalmente o en una breve nota de trabajo: quién preguntará al agente, qué problema resolverá, qué documentos puede consultar y qué respuesta concreta se espera. No incluir funciones que dependan de permisos o integraciones no habilitados.

**Paso 3.** Utilizar el siguiente caso completo si no se dispone de un caso real y fuentes autorizadas: *«Necesito consultar acuerdos, responsables y compromisos de Project Nexus sin revisar manualmente los documentos del comité»*. Para este caso utilizar el nombre `Nexus Acuerdos` y las tres fuentes de la Tabla de ayuda.

**Paso 4.** Establecer el criterio de finalización: el agente deberá responder preguntas sobre acuerdos y compromisos, citar las fuentes y rechazar afirmaciones que no estén documentadas.

### Tarea 2. Crear y configurar el agente (17 minutos)

**Paso 1.** Iniciar sesión en [Microsoft Copilot](https://m365.cloud.microsoft.com/), seleccionar **Nuevo agente** y abrir **Configurar** mediante **Omitir para configurar**, si aparece. No utilizar Copilot Studio en este ejercicio.

**Paso 2.** Escribir un nombre que identifique el caso elegido y una descripción que especifique quién lo utilizará y con qué propósito. Para el caso de respaldo, usar:

- **Nombre:** `Nexus Acuerdos`.
- **Descripción:** `Ayuda al equipo de Project Nexus a consultar decisiones, responsables y compromisos registrados en actas, minutas y el plan de seguimiento.`

**Paso 3.** Seleccionar en **Conocimiento** los documentos reales autorizados del caso. Para el respaldo, agregar `NXS-002`, `NXS-003` y `Nexus_05_Plan_entregables.xlsx`. Si algún archivo no está disponible, cargarlo en OneDrive y volver a seleccionarlo; no inventar enlaces.

**Paso 4.** Incorporar en el campo **Instrucciones** el texto correspondiente al caso seleccionado. El siguiente ejemplo está completo para `Nexus Acuerdos`; cuando se use un caso particular, sustituir su propósito, fuentes y criterios por los de esa necesidad, manteniendo las reglas de comprobación.

**Instrucciones del agente de respaldo — Texto completo**

```text
Eres Nexus Acuerdos, un agente que ayuda al equipo del proyecto a localizar
y explicar acuerdos, compromisos y decisiones documentadas.

Utiliza como conocimiento exclusivamente el comité del 27/08/2026
(NXS-002), la minuta del 24/09/2026 (NXS-003) y el plan de entregables.

Cuando te pregunten por una decisión:
- proporciona su identificador, fecha, descripción, responsable y fuente;
- distingue decisiones aprobadas de acciones pendientes;
- indica qué entregable o actividad resulta afectado;
- diferencia fechas iniciales de fechas vigentes cuando exista un cambio.

Cuando te pregunten por compromisos:
- responde en una tabla con ID, acción, responsable, fecha y estado;
- señala el corte temporal de los documentos utilizados;
- identifica explícitamente los campos ausentes.

No inventes acuerdos, reuniones, responsables, plazos ni aprobaciones.
Si un dato no está documentado, responde "No especificado en las fuentes".
Si las fuentes muestran fechas diferentes, explica el cambio e identifica
el documento que contiene cada una. No prometas actualizar calendarios,
mandar correos o modificar el plan; tu función es consultar y sintetizar.

Responde en español, con estructura breve, referencias de origen y
separación clara entre información confirmada y recomendaciones.
```

**Paso 5.** Agregar al menos dos indicaciones iniciales pertinentes. Para `Nexus Acuerdos`, utilizar:

| Título | Indicación |
| --- | --- |
| Decisiones adoptadas | `Enumera las decisiones C-01, C-01A, C-02 y C-03 con sus fechas y fuentes.` |
| Compromisos pendientes | `¿Qué compromisos siguen abiertos al corte del estado disponible y quién es responsable de cada uno?` |
| Cambio de plazo | `Explica por qué cambió la fecha de D-03 y quién registró la decisión.` |

**Paso 6.** Revisar en **Configurar** que las fuentes, instrucciones e indicaciones respondan a la necesidad elegida y no contengan obligaciones imposibles para un agente de consulta.

### Tarea 3. Probar y ajustar el agente para el uso cotidiano (12 minutos)

**Paso 1.** Abrir **Probar / Try it** y realizar una consulta habitual de la actividad elegida. Para el caso de respaldo, utilizar:

**Prompt 1 — Consulta normal**

```text
¿Qué decisiones se tomaron en las reuniones del 27/08/2026 y el
24/09/2026 que afectaron los entregables o la muestra del piloto?
Separa cada decisión, incluye ID, fecha, impacto y fuente.
```

**Paso 2.** Comprobar en los documentos que el agente identifique `C-01`, `C-01A`, `C-02` y `C-03`, sin atribuirlas a un comité incorrecto. Para un caso diferente, contrastar la respuesta con el documento propio que respalda los hechos.

**Paso 3.** Introducir una solicitud incompleta, equivalente a «¿Qué falta por hacer?», y verificar que el agente pida contexto suficiente o delimite el periodo antes de responder. En el caso de respaldo, utilizar:

**Prompt 2 — Pregunta incompleta**

```text
¿Qué tareas faltan? Dime cuáles están pendientes según tus fuentes,
indica la fecha de corte de la información y separa lo confirmado de
lo que no puede determinarse.
```

**Paso 4.** Introducir una pregunta que no deba contestarse sin fuente. En el caso de respaldo, utilizar:

**Prompt 3 — Comprobación de límites**

```text
¿Quién autorizó un presupuesto adicional de 250000 para Project Nexus
y en qué reunión se aprobó? Si no aparece en tus fuentes, dilo.
```

**Paso 5.** Verificar que el agente indique que no hay aprobación documentada de ese importe. Si inventa una respuesta, reforzar las instrucciones y repetir la consulta. Para un caso elegido por el participante, usar una pregunta equivalente sobre un dato no incluido en sus fuentes.

**Paso 6.** Solicitar una salida lista para uso cotidiano.

**Prompt 4 — Producto aplicado**

```text
Prepara una tabla de acuerdos y compromisos de Project Nexus que pueda
copiar a Excel. Incluye ID, fecha de decisión o compromiso, descripción,
responsable, estado y fuente exacta. No agregues registros no sustentados.
```

**Paso 7.** Examinar la tabla en la vista de prueba. Corregir cualquier fecha, ID o fuente que no coincida; guardar el resultado en Excel si se desea utilizar como salida de trabajo.

### Tarea 4. Guardar y localizar el agente propio (5 minutos)

**Paso 1.** Seleccionar **Crear** para guardar el agente. Dejarlo privado salvo que exista autorización para compartirlo.

**Paso 2.** Abrir el listado de agentes propios de Microsoft Copilot y localizarlo por el nombre configurado. Iniciar una conversación nueva desde su entrada guardada.

**Paso 3.** Repetir la consulta principal y comprobar que las respuestas siguen basadas en las fuentes agregadas, sin necesitar la conversación de prueba anterior.

**Paso 4.** Registrar únicamente para uso personal el enlace del agente, si la interfaz permite copiarlo. No distribuir el agente ni sus fuentes fuera de los usuarios autorizados.

### Tarea 5. Resolver inquietudes de construcción y permisos (8 minutos)

**Paso 1.** Formular al instructor la dificultad concreta que impide cumplir la función del agente: creación, acceso a conocimiento, comportamiento de respuesta, indicaciones iniciales, permisos o localización después de guardar. Probar nuevamente después de cada corrección.

**Paso 2.** Comprobar con el instructor la primera condición aplicable: disponibilidad de **Nuevo agente**, archivo realmente agregado en **Conocimiento**, estado de preparación de la fuente, permisos del usuario sobre ella y correspondencia entre instrucciones y respuesta esperada. Si la interfaz no permite realizar una acción, registrar la limitación del tenant como un impedimento real, sin simular su ejecución.

**Paso 3.** Refinar la instrucción que originó respuestas insuficientes. Por ejemplo, cuando la respuesta mezcle hechos y sugerencias, agregar: `Separa siempre los hechos documentados de las recomendaciones; incluye la fuente de cada hecho y reconoce expresamente los datos ausentes.` Volver a ejecutar una consulta de prueba.

**Paso 4.** Confirmar que el agente sigue disponible en el área de agentes propios, conserva instrucciones y conocimientos y contesta una consulta real del escenario escogido. Conservar su acceso para la práctica de compartir agentes.

### Resultado esperado

Existe un agente propio creado en Agent Builder, centrado en una necesidad concreta, con propósito, instrucciones, fuentes y preguntas sugeridas. Se ha comprobado una respuesta habitual, una consulta incompleta y una pregunta sin sustento, y el agente está guardado y accesible para su uso cotidiano. El agente conserva los ajustes aplicados durante la resolución de inquietudes y está disponible para compartirlo posteriormente, cuando corresponda.

[Volver al listado de prácticas](../)
