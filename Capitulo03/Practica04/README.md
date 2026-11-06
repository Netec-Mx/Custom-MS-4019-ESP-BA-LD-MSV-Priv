---
permalink: /Capitulo03/Practica04/
---

# Práctica 4. Creación de un agente de Microsoft 365 Copilot Chat

## Objetivo de la práctica:

Al finalizar la práctica, serás capaz de:

- Crear y guardar un agente personalizado de Microsoft 365 Copilot mediante Agent Builder.
- Configurar propósito, instrucciones, fuentes de conocimiento e indicaciones iniciales, y comprobar su comportamiento.
- Localizar el agente creado en Microsoft 365 Copilot y utilizarlo para generar un entregable relacionado con su función.

## Duración aproximada:

- 45 minutos.

## Tabla de ayuda:

| Parámetro | Valor | Uso |
| --- | --- | --- |
| Aplicación | [Microsoft Copilot](https://m365.cloud.microsoft.com/) → **Nuevo agente** | Abrir Agent Builder. |
| Nombre del agente | `Nexus Seguimiento` | Identificar el agente en los agentes propios. |
| Descripción | Asistente de consulta y seguimiento de Project Nexus basado en documentos del proyecto. | Propósito visible para el usuario. |
| Fuentes | [NXS-001](../../Capitulo02/Practica02/recursos/Nexus_01_Acta_inicio_2026-07-29.docx), [NXS-002](../../Capitulo02/Practica02/recursos/Nexus_02_Comite_2026-08-27.docx), [NXS-003](../../Capitulo02/Practica02/recursos/Nexus_03_Minuta_2026-09-24.docx), [NXS-004](../../Capitulo02/Practica02/recursos/Nexus_04_Estado_2026-10-23.docx), [plan de entregables](../../Capitulo02/Practica02/recursos/Nexus_05_Plan_entregables.xlsx) | Fundamentar las respuestas y los documentos producidos. |
| Campo de prueba | Entregable `D-03` y decisión `C-01` | Contrastar una respuesta con una decisión documentada. |
| Producto final | Un archivo Word, Excel, PowerPoint, correo o plan de acción | Seleccionar uno según las capacidades disponibles. |

## Instrucciones

El equipo de Project Nexus necesita consultar rápidamente acuerdos, responsables y estados documentados. Crearás en Agent Builder un agente de referencia con conocimientos específicos, indicaciones de inicio y pruebas de respuestas con y sin fundamento.

### Tarea 1. Definir el agente y preparar sus conocimientos (8 minutos)

**Paso 1.** Abrir [Microsoft Copilot](https://m365.cloud.microsoft.com/), ingresar a **Nuevo agente** y seleccionar **Omitir para configurar** o la opción que abre directamente **Configurar**. Esta práctica utiliza configuración explícita, no programación.

**Paso 2.** Introducir el nombre `Nexus Seguimiento` y la descripción de la Tabla de ayuda. Verificar que ambos campos describan una función de seguimiento y no prometan actualizar sistemas externos.

**Paso 3.** Descargar o recuperar de la práctica 2 los cinco archivos de Project Nexus. Si ya están en OneDrive o SharePoint, localizar las mismas fuentes en la biblioteca de trabajo autorizada.

**Paso 4.** Agregar en **Conocimiento** los archivos de Word y Excel desde **Examinar / Agregar contenido de trabajo**, **Adjuntar archivo** o las opciones equivalentes disponibles en Agent Builder. Seleccionar los documentos específicos y comprobar que aparecen en la lista de fuentes; no asumir que un enlace de carpeta incluye todos los archivos si no se muestran.

### Tarea 2. Configurar instrucciones e indicaciones iniciales (15 minutos)

**Paso 1.** Copiar el siguiente texto en el campo **Instrucciones** del agente.

**Instrucciones del agente — Texto completo**

```text
Eres Nexus Seguimiento, un agente de apoyo para consultar y resumir el
proyecto Project Nexus. Atiendes a usuarios autorizados que necesitan
información de entregables, decisiones, riesgos y próximas acciones.

FUENTES:
Usa primero los documentos de Project Nexus adjuntos como conocimiento.
Identifica siempre el documento que respalda un hecho, por su nombre o
identificador (NXS-001, NXS-002, NXS-003, NXS-004 o plan de entregables).
No supongas acceso a información que no esté en las fuentes.

COMPORTAMIENTO:
1. Para preguntas de estado, informa el corte temporal del documento,
   el identificador del entregable, su responsable, estado y fecha vigente.
2. Distingue fechas base de fechas aprobadas posteriormente.
3. Para decisiones, identifica ID, fecha, acuerdo y documento de origen.
4. Para acciones, informa responsable y fecha solo si figuran en las fuentes.
5. Si un dato es desconocido, escribe "No especificado en las fuentes".
6. No inventes reuniones, correos, cifras, documentos, aprobaciones ni
   enlaces. No utilices datos externos para completar la historia del
   proyecto cuando la consulta se refiera a sus registros internos.
7. Si hay información contradictoria, explica la diferencia y señala
   qué documento contiene cada versión.
8. No afirmes poder crear tareas, enviar mensajes o actualizar
   aplicaciones si no se ha habilitado expresamente esa capacidad.

FORMATO:
Responde en español, con encabezados claros y tablas breves cuando
faciliten comparar información. Separa hechos documentados de sugerencias.
Cuando te pidan un reporte, correo o tabla, ofrece un contenido completo
que pueda abrirse o copiarse a Word, Outlook o Excel, y proporciona un
archivo descargable únicamente si la interfaz realmente lo permite.
```

**Paso 2.** Configurar las siguientes indicaciones sugeridas en el campo **Indicaciones iniciales / Starter prompts** de Agent Builder, una por una.

| Título de indicación | Texto de la indicación |
| --- | --- |
| Estado de entregables | `Resume D-01 a D-05 indicando responsable, fecha vigente, estado y fuente.` |
| Decisiones | `¿Qué cambió con la decisión C-01 y en qué documento consta?` |
| Próximas acciones | `Enumera las acciones pendientes al 23/10/2026 con fecha y responsable confirmados.` |

**Paso 3.** Revisar en la pestaña de configuración que las fuentes sean correctas y que las indicaciones no prometan funcionalidades ajenas al temario. Comprobar que las instrucciones permanezcan dentro del límite admitido por la interfaz.

**Paso 4.** Abrir el área **Probar / Try it** del agente y seleccionar una de las indicaciones sugeridas. Confirmar que la respuesta mencione un documento de origen reconocible.

### Tarea 3. Probar, ajustar y crear el agente (15 minutos)

**Paso 1.** Enviar el siguiente prompt para probar el caso principal.

**Prompt 1 — Prueba de seguimiento**

```text
¿Cuál fue la fecha base de D-03, qué nueva fecha se aprobó, quién registró
el cambio y en qué documento se encuentra la decisión? Indica también
la fecha real de finalización y el estado al 23/10/2026.
```

**Paso 2.** Comparar la respuesta con la decisión `C-01` de `NXS-002` y el estado de `NXS-004`: fecha base **18/09/2026**, fecha revisada **25/09/2026** y cierre **09/10/2026**. Si el agente atribuye el cambio a otra persona o inventa una fecha, corregir las instrucciones o el origen de conocimiento y repetir la prueba.

**Paso 3.** Evaluar cómo trata una solicitud sobre datos ausentes.

**Prompt 2 — Dato que no está en las fuentes**

```text
¿Cuál fue el presupuesto aprobado y el costo final de Project Nexus?
Si no aparece en los documentos, indícalo de forma explícita.
```

**Paso 4.** Comprobar que el agente no inventa cifras presupuestales. Si responde con números no documentados, reforzar la instrucción de reconocer datos desconocidos y volver a probar.

**Paso 5.** Solicitar un producto compatible con el propósito del agente.

**Prompt 3 — Entregable de negocio**

```text
Con las fuentes disponibles de Project Nexus, prepara un informe de estado
para Word de una página al 23/10/2026, con resumen de entregables,
decisiones relevantes, bloqueos, responsables y próximas acciones.
Incluye referencias por documento y distingue hechos de recomendaciones.
Si puedes crear un archivo Word descargable, hazlo; de lo contrario entrega
el texto completo para guardarlo en Word.
```

**Paso 6.** Descargar el informe si existe la opción o copiar la respuesta a Word y guardarla como `Nexus_Estado_por_Agente.docx`. También es válido escoger otro producto contemplado por el temario (tabla de Excel, correo, PowerPoint, plan o propuesta), siempre que derive del propósito del agente y pueda comprobarse con las fuentes.

**Paso 7.** Seleccionar **Crear** o **Guardar/Crear agente** según la interfaz y confirmar que aparezca el mensaje de creación satisfactoria. Mantenerlo privado durante el ejercicio, salvo que se haya autorizado explícitamente compartirlo.

### Tarea 4. Localizar el agente y confirmar su funcionamiento (7 minutos)

**Paso 1.** Abrir el listado **Agentes**, **Mis agentes** o **Todos los agentes** de Microsoft 365 Copilot; localizar `Nexus Seguimiento` por nombre. Si la Tienda de agentes muestra la sección **Mis agentes**, buscarlo allí. Un agente privado no tiene por qué estar publicado para toda la organización.

**Paso 2.** Abrir una nueva conversación con el agente ya guardado y seleccionar la indicación **Estado de entregables**.

**Paso 3.** Verificar que el agente responde basándose en las fuentes configuradas y no solo en el contexto de la conversación de prueba anterior.

**Paso 4.** Recuperar el documento `Nexus_Estado_por_Agente.docx`, comprobar que es legible y que conserva referencias a los documentos de origen. No incluir datos que no aparezcan en las fuentes.

### Resultado esperado

Se dispone del agente `Nexus Seguimiento` creado y localizable desde Microsoft 365 Copilot, con nombre, propósito, instrucciones, cinco fuentes de conocimiento e indicaciones sugeridas. El agente responde a pruebas de datos presentes y ausentes sin inventarlos y produce al menos un entregable de negocio verificable, como el informe Word propuesto.

[Volver al listado de prácticas](../)
