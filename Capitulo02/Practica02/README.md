---
permalink: /Capitulo02/Practica02/
---

# Práctica 2. Uso del agente Investigador

## Objetivo de la práctica:

Al finalizar la práctica, serás capaz de:

- Investigar los avances, decisiones y desafíos de Project Nexus durante un periodo de 90 días utilizando fuentes documentales identificables.
- Organizar acciones, acuerdos, entregables, preguntas abiertas y el inventario documental en hojas de cálculo.
- Preparar un informe, una presentación, una minuta, un correo y documentos de apoyo a reuniones, comprobando sus referencias.

## Duración aproximada:

- 36 minutos.

## Tabla de ayuda:

| Parámetro | Valor | Uso |
| --- | --- | --- |
| Agente | **Investigador / Researcher**, en [Microsoft Copilot](https://m365.cloud.microsoft.com/) | Investigación documental con referencias. |
| Proyecto | Project Nexus | Caso de seguimiento empresarial. |
| Periodo | **29/07/2026 a 26/10/2026**, ambos días incluidos | Ventana de 90 días del escenario de laboratorio. |
| [Acta de inicio](./recursos/Nexus_01_Acta_inicio_2026-07-29.docx) | `NXS-001` | Objetivos, responsables y fechas iniciales. |
| [Comité de seguimiento](./recursos/Nexus_02_Comite_2026-08-27.docx) | `NXS-002` | Cambio aprobado de fecha y compromisos. |
| [Minuta de reunión](./recursos/Nexus_03_Minuta_2026-09-24.docx) | `NXS-003` | Acuerdos y acciones de una reunión concreta. |
| [Estado ejecutivo](./recursos/Nexus_04_Estado_2026-10-23.docx) | `NXS-004` | Avances, bloqueos y próximos pasos. |
| [Plan de entregables](./recursos/Nexus_05_Plan_entregables.xlsx) | Hojas `Entregables`, `Acciones`, `Decisiones` | Fechas, estados e identificadores para contrastar. |

## Instrucciones

Los responsables de Project Nexus solicitan una visión consolidada de decisiones, avances y compromisos de sus documentos de seguimiento. Utilizarás Investigador para reconstruir la información con fuentes identificables y preparar productos de consulta y comunicación.

### Tarea 1. Reunir las fuentes y abrir Investigador (6 minutos)

**Paso 1.** Descargar los cinco archivos de la **Tabla de ayuda** y comprobar que se abren correctamente en Word y Excel.

**Paso 2.** Abrir OneDrive o SharePoint desde Microsoft 365, crear una carpeta de trabajo denominada `Project_Nexus_Investigacion` en un espacio autorizado y cargar allí los cinco archivos sin cambiar sus nombres. Copiar el enlace de la carpeta o de cada archivo según permita la plataforma.

**Paso 3.** Abrir [Microsoft Copilot](https://m365.cloud.microsoft.com/), acceder al agente **Investigador (Researcher)** desde **Agentes** o **Todos los agentes** y comenzar una nueva consulta. Utilizar la opción de agregar contenido o de hacer referencia a archivos de trabajo para incluir las cinco fuentes. Cuando el agente no pueda acceder a la carpeta, seleccionarlas individualmente.

**Paso 4.** Verificar que la cuenta tenga permiso de lectura en todos los documentos. Pedir al agente identificar los nombres o enlaces de las fuentes disponibles antes de utilizar sus resultados. No utilizar información del web para rellenar lagunas del proyecto.

### Tarea 2. Reconstruir el periodo y generar el informe consolidado (10 minutos)

**Paso 1.** Ejecutar una única investigación que agrupe los resultados que se utilizarán en el resto de los documentos.

**Prompt 1 — Investigación con fuentes**

```text
Investiga Project Nexus usando exclusivamente estos cinco documentos de
trabajo que te he proporcionado: NXS-001, NXS-002, NXS-003, NXS-004 y
Nexus_05_Plan_entregables.xlsx. El periodo del análisis es del 29 de julio
al 26 de octubre de 2026, ambos días inclusive (90 días del escenario).

Elabora un informe consolidado con:
1. contexto, propósito y alcance;
2. cronología de hitos y principales avances;
3. decisiones con identificador, fecha y aprobador;
4. estado de los cinco entregables;
5. obstáculos y riesgos abiertos;
6. próximos pasos con responsables y fechas;
7. conclusiones ejecutivas y preguntas todavía sin respuesta.

Para cada hecho incluye referencia al nombre del archivo y, cuando el
sistema permita vínculos, enlaza la fuente original. Distingue fechas
iniciales y fechas aprobadas posteriormente; no sustituyas la última fecha
vigente por la primera. Si las fuentes discrepan, identifícalo. No inventes
reuniones, acuerdos, resultados ni responsables. Organiza la respuesta con
encabezados que puedan copiarse a Word.
```

**Paso 2.** Revisar que el resumen indique **cinco entregables**, que el cambio de fecha de **D-03** corresponda a la decisión **C-01** y que los hitos citados tengan referencias a `NXS-001` a `NXS-004` o al plan.

**Paso 3.** Solicitar el texto final para Word sin repetir toda la investigación.

**Prompt 2 — Informe Word con referencias**

```text
Convierte el informe consolidado que acabas de elaborar en un documento
para Word denominado Nexus_Informe_90_Dias.docx. Incluye título, periodo,
resumen ejecutivo, hitos, tabla de entregables, decisiones, desafíos,
acciones pendientes y una sección final de fuentes consultadas con sus
vínculos cuando estén disponibles. Mantén la distinción entre hechos y
recomendaciones. Si no puedes adjuntar un .docx, entrega el documento
completo con estructura y tablas que pueda pegar en Word.
```

**Paso 4.** Guardar el informe en Word. Confirmar que las citas correspondan a documentos cargados y conservar los enlaces de origen; nunca reemplazarlos por URLs inventadas.

### Tarea 3. Obtener matrices y comunicación a partir del análisis (12 minutos)

**Paso 1.** Solicitar de manera agrupada las cinco tablas de Excel que exige el temario.

**Prompt 3 — Tablas estructuradas para Excel**

```text
A partir de la investigación ya realizada y de las cinco fuentes adjuntas,
produce cinco tablas independientes, listas para Excel, con una fila por
registro y sin mezclar tipos de información:
A. Nexus_Acciones.xlsx: ID, actividad, responsable, fecha compromiso,
   estado, documento de origen.
B. Nexus_Decisiones.xlsx: ID de decisión, fecha, participantes o
   aprobador identificado, descripción, impacto, documento de origen.
C. Nexus_Entregables.xlsx: ID, entregable, responsable, fecha vigente,
   fecha real cuando exista, estado y colaboradores confirmados.
D. Nexus_Preguntas_Abiertas.xlsx: pregunta o acción incompleta,
   responsable conocido, siguiente paso, fecha y fuente.
E. Nexus_Inventario_Documental.xlsx: nombre exacto de los cinco archivos,
   fecha del documento, contenido relevante y vínculo al archivo si el
   servicio permite recuperarlo.

Si un campo no aparece en la fuente, escribe "No especificado"; no lo
inventes. Conserva el vínculo o nombre de la fuente para cada registro.
Cuando sea posible, entrega los cinco archivos Excel descargables. En caso
contrario, muestra cada tabla por separado para copiarla a Excel.
```

**Paso 2.** Descargar los Excel generados, cuando estén disponibles. Si el agente solo produce tablas, abrir Excel, copiar cada tabla en un archivo distinto y guardarlo con el nombre solicitado. Al copiar datos, verificar que cada identificador quede en su propia fila.

**Paso 3.** Comparar las decisiones `C-01`, `C-01A`, `C-02` y `C-03` con la hoja `Decisiones` del plan. Verificar que no se atribuya a la reunión de septiembre una decisión adoptada en agosto. Revisar que el inventario indique exactamente cinco archivos fuente.

**Paso 4.** Preparar el correo que solicita el temario mediante el siguiente prompt.

**Prompt 4 — Correo de Outlook**

```text
Redacta un correo para Outlook dirigido a los participantes del proyecto
Project Nexus (sin inventar direcciones de correo). Asunto: "Project Nexus:
avances y próximos pasos". Resume la participación de las funciones
del equipo, tres avances confirmados al 23/10/2026, los bloqueos vigentes
y las acciones pendientes con responsables y fechas. Usa tono profesional,
conciso y verificable, sin afirmar que se hayan enviado mensajes.
```

**Paso 5.** Abrir Outlook, crear un mensaje nuevo, copiar el asunto y contenido, revisar los datos con `NXS-004` y guardar el mensaje como borrador. No enviarlo durante el ejercicio.

### Tarea 4. Preparar minuta, reunión, estado ejecutivo y presentación (8 minutos)

**Paso 1.** Solicitar tres documentos de Word en una única petición, manteniendo el hecho de que provienen de fuentes diferentes.

**Prompt 5 — Documentos Word para seguimiento**

```text
Usa exclusivamente los documentos de Project Nexus y el análisis previo.
Prepara tres entregables diferentes, cada uno con un nombre y estructura
independiente:
1. Nexus_Minuta_24Sep.docx: minuta de la reunión del 24/09/2026 con
   participantes, temas, acuerdos C-02 y C-03 y acciones de esa reunión.
2. Nexus_Preparacion_Reunion.docx: antecedentes, decisiones previas,
   estado vigente, puntos por decidir y preguntas para el próximo comité.
3. Nexus_Estado_Una_Pagina.docx: reporte ejecutivo de una página al
   23/10/2026 con avances, bloqueos y próximos pasos.

No combines hechos de fechas distintas como si fueran de una sola reunión.
Incluye fuentes identificables. Si no puedes generar archivos .docx,
proporciona el contenido completo de cada uno por separado para guardarlo
en Word.
```

**Paso 2.** Descargar o guardar cada documento en Word. Comprobar que los asistentes de la minuta coincidan con `NXS-003` y que el estado de una página use el corte de `NXS-004`.

**Paso 3.** Solicitar la presentación ejecutiva del proyecto.

**Prompt 6 — Presentación ejecutiva**

```text
Usa únicamente el informe y las fuentes de Project Nexus. Prepara una
presentación ejecutiva de seis diapositivas: 1) propósito y periodo,
2) cronología de avances, 3) estado de los cinco entregables,
4) decisiones y su impacto, 5) riesgos y bloqueos, 6) prioridades
siguientes. Para cada diapositiva entrega título, contenido breve, hechos
y referencia de origen. No introduzcas números adicionales. Indica cómo
trasladar el contenido a PowerPoint; no afirmes haber creado un PPTX si
no puedes generar el archivo directamente.
```

**Paso 4.** Crear `Nexus_Presentacion_Ejecutiva.pptx` en PowerPoint utilizando el esquema generado. El agente Investigador no ofrece de forma garantizada exportación nativa a PowerPoint: la preparación de diapositivas se completa en PowerPoint con la información aportada por el agente.

### Resultado esperado

Quedan preparados los **11 entregables** solicitados: informe consolidado en Word; presentación ejecutiva en PowerPoint; matrices Excel de acciones, decisiones, entregables, preguntas abiertas e inventario de documentos; minuta Word; correo como borrador de Outlook; documento Word para preparar reuniones; y reporte de una página en Word. Todos se construyen con las cinco fuentes de Project Nexus; las decisiones, fechas y responsables citados deben ser trazables. La creación de archivos de Office no se atribuye exclusivamente a Investigador cuando se realiza desde Word, Excel o PowerPoint.

[Volver al listado de prácticas](../)
