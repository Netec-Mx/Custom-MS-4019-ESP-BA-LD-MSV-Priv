---
permalink: /Capitulo02/Practica01/
---

# Práctica 1. Uso del agente Analista

## Objetivo de la práctica:

Al finalizar la práctica, serás capaz de:

- Analizar respuestas cuantitativas y comentarios de una encuesta con el agente Analista de Microsoft 365 Copilot.
- Obtener tablas de resumen, cálculos, relaciones estadísticas y visualizaciones descargables.
- Elaborar los entregables de Word, Excel y PowerPoint solicitados para comunicar los hallazgos de Project Nexus.

## Duración aproximada:

- 33 minutos.

## Tabla de ayuda:

| Parámetro | Valor | Uso |
| --- | --- | --- |
| Aplicación | [Microsoft Copilot](https://m365.cloud.microsoft.com/) | Abrir el agente **Analista / Analyst**. |
| Archivo | [Encuesta_Project_Nexus.xlsx](./recursos/Encuesta_Project_Nexus.xlsx) | Datos de entrada de la práctica. |
| Hoja de datos | `Encuesta` | 120 respuestas individuales del escenario. |
| Hoja de referencia | `Diccionario` | Definiciones y escalas de la encuesta. |
| Categorías evaluadas | Comunicación, Coordinación, Herramientas y Satisfacción general | Promedios, porcentajes y gráficos. |
| Escala | De 1 a 5 | Una calificación favorable corresponde a 4 o 5. |
| Campo de texto | `Comentario abierto` | Clasificación de temas recurrentes, preocupaciones y sugerencias. |
| Campo complementario | `Horas de uso semanal` | Analizar asociación con satisfacción, sin afirmar causalidad. |
| Proyecto | Project Nexus | Contexto común para los reportes. |

## Instrucciones

El equipo de Project Nexus necesita interpretar los resultados de su encuesta de 120 respuestas y presentar hallazgos verificables a los responsables del programa. Utilizarás Analista para calcular indicadores, estudiar comentarios y preparar los informes y las visualizaciones solicitados.

### Tarea 1. Abrir Analista y cargar la encuesta (4 minutos)

**Paso 1.** Descargar el archivo [Encuesta_Project_Nexus.xlsx](./recursos/Encuesta_Project_Nexus.xlsx) y abrirlo en Excel para identificar las hojas `Encuesta` y `Diccionario`.

**Paso 2.** Abrir [Microsoft Copilot](https://m365.cloud.microsoft.com/) con la cuenta autorizada, ingresar en **Agentes** o **Todos los agentes** y seleccionar **Analista (Analyst)**. Si no aparece en el menú lateral, buscarlo en la Tienda de agentes según la configuración del tenant.

**Paso 3.** Iniciar una conversación y adjuntar el libro mediante **Agregar contenido (+)**, **Adjuntar archivo** o el control equivalente de la interfaz. Cuando se solicite, seleccionar el archivo descargado. Si el servicio exige un archivo en OneDrive, cargar allí el mismo libro y seleccionarlo como archivo de trabajo.

**Paso 4.** Enviar el siguiente prompt para verificar que el agente interpreta los encabezados y la escala.

**Prompt 1 — Reconocimiento de datos**

```text
Analiza únicamente el archivo Encuesta_Project_Nexus.xlsx que adjunté.
Verifica que puedas leer las hojas Encuesta y Diccionario.
Indica: total de respuestas, nombres exactos de las cuatro categorías
calificadas de 1 a 5, campos adicionales disponibles y cantidad de
valores vacíos por categoría. No calcules resultados inventados.
Si una columna no se puede leer, indícame cuál es y qué debo corregir.
```

**Paso 5.** Comprobar que el total es de **120 respuestas** y que aparecen las cuatro categorías del archivo. Si la cantidad no coincide, volver a adjuntar el libro correcto antes de continuar.

### Tarea 2. Calcular indicadores y organizar el análisis cuantitativo (12 minutos)

**Paso 1.** Solicitar el análisis de promedios, porcentajes y correlaciones utilizando el prompt completo.

**Prompt 2 — Cálculo de indicadores y archivo Excel**

```text
Trabaja solo con las 120 filas de la hoja Encuesta del archivo adjunto.
Calcula para Comunicación, Coordinación, Herramientas y Satisfacción general:
1) número de respuestas válidas;
2) promedio de las calificaciones en escala de 1 a 5;
3) porcentaje de calificaciones favorables (valores 4 o 5);
4) categorías mejor y peor evaluadas según el promedio;
5) correlación de Pearson entre Horas de uso semanal y Satisfacción general.

Comprueba el denominador utilizado en cada porcentaje e informa si hay
valores vacíos. No infieras relaciones causales y no presentes correlaciones
como hechos explicativos. Genera un libro Excel descargable denominado
Nexus_Analisis_Cuantitativo.xlsx con una hoja de resumen por categoría y
otra hoja con el cálculo de la correlación y su interpretación. Incluye las
fórmulas o el método de cálculo y un resumen que pueda verificarse.
```

**Paso 2.** Abrir la tabla de promedios que entrega Analista. Comparar que haya una fila por categoría y que el promedio quede entre **1 y 5**. Verificar que cada porcentaje favorable esté entre **0 % y 100 %**.

**Paso 3.** Descargar `Nexus_Analisis_Cuantitativo.xlsx` desde el enlace que proporcione el agente, si aparece. Si no ofrece descarga, pedir **«muéstrame el resumen en tabla copiable»**, trasladar las tablas a un libro de Excel y guardarlo con el nombre indicado. No atribuir al agente la creación del archivo cuando solo haya generado texto.

**Paso 4.** Solicitar el informe de tendencias para Word.

**Prompt 3 — Informe de tendencias**

```text
Con base exclusivamente en las cifras calculadas a partir de la encuesta,
prepara un informe breve para Word titulado "Tres tendencias de la encuesta
Project Nexus". Identifica exactamente tres tendencias cuantitativas.
En cada una, muestra la categoría, el promedio, el porcentaje favorable y
la interpretación prudente del hallazgo. Distingue datos observados de
recomendaciones. Si puedes generar un .docx descargable, hazlo con el nombre
Nexus_Tres_Tendencias.docx; de lo contrario entrega el texto completo con
encabezados para incorporarlo a Word sin añadir información no sustentada.
```

**Paso 5.** Descargar o guardar el informe en Word y contrastar sus tres tendencias con los datos del Excel. Corregir las discrepancias usando el archivo fuente.

### Tarea 3. Examinar comentarios y preparar los entregables ejecutivos (9 minutos)

**Paso 1.** Solicitar el procesamiento de los comentarios libres sin reemplazarlos por valoraciones genéricas.

**Prompt 4 — Comentarios e informe Word**

```text
Analiza solamente la columna Comentario abierto de la hoja Encuesta.
Agrupa por temas recurrentes y distingue expresamente:
- temas que se repiten;
- principales preocupaciones;
- sugerencias de mejora.
Para cada grupo indica una cantidad o frecuencia verificable y cita hasta
dos ejemplos breves extraídos del archivo (sin datos personales).
No confundas un comentario con un hecho probado ni inventes testimonios.
Genera, si está disponible, un archivo Word Nexus_Comentarios.docx.
Si no puedes crear el archivo, entrega una estructura completa para Word.
```

**Paso 2.** Abrir o guardar el documento `Nexus_Comentarios.docx`. Comprobar que los ejemplos citados realmente existan en la columna `Comentario abierto` y que los temas se clasifiquen de manera consistente.

**Paso 3.** Solicitar un esquema de presentación con fortalezas, oportunidades y recomendaciones, tomando como base los dos análisis.

**Prompt 5 — Presentación de resultados**

```text
Conserva el contexto del archivo Encuesta_Project_Nexus.xlsx y los
análisis cuantitativo y cualitativo de esta conversación. Prepara una
presentación ejecutiva de Project Nexus de 5 diapositivas:
1. Objetivo y alcance de la encuesta.
2. Principales fortalezas con métricas.
3. Oportunidades de mejora y comentarios asociados.
4. Comparación de las cuatro categorías.
5. Tres recomendaciones vinculadas a los hallazgos.
No agregues datos externos. Si es posible, genera un PowerPoint descargable
Nexus_Encuesta_Resumen.pptx. Si no es posible, entrega por diapositiva
título, contenidos, valores numéricos y notas para crearlo en PowerPoint.
```

**Paso 4.** Descargar el PowerPoint o crearlo en la aplicación PowerPoint a partir de la estructura suministrada por Copilot. Revisar que las métricas coincidan con las tablas verificadas; las recomendaciones deben estar identificadas como propuestas.

### Tarea 4. Generar visualizaciones y comprobar resultados (8 minutos)

**Paso 1.** Solicitar un gráfico de barras descargable de los cuatro promedios.

**Prompt 6 — Comparación de promedios**

```text
Genera un gráfico de barras con el promedio de Comunicación, Coordinación,
Herramientas y Satisfacción general calculado desde la encuesta.
Usa escala de 0 a 5, muestra el valor en cada barra, incluye título y
unidades, y proporciona una imagen PNG descargable llamada
Nexus_Promedios_Barras.png. No modifiques los datos para el gráfico.
```

**Paso 2.** Solicitar las otras visualizaciones estadísticas mencionadas en el temario. Mantener las variables correctas para cada una.

**Prompt 7 — Visualizaciones complementarias**

```text
Con los datos de Encuesta_Project_Nexus.xlsx, genera cuatro imágenes PNG:
1. Histograma de Satisfacción general (valores 1 a 5).
2. Gráfico circular de distribución porcentual por Área.
3. Dispersión de Horas de uso semanal frente a Satisfacción general.
4. Mapa de calor de correlaciones entre las cuatro calificaciones y
   Horas de uso semanal.
En cada gráfico agrega título, etiquetas, unidades o escala pertinente.
Calcula las cifras desde las filas originales. Si no es posible crear una
imagen, indica con precisión la limitación y entrega los datos tabulares
para generarla en Excel. No interpretes correlaciones como causalidad.
```

**Paso 3.** Descargar las imágenes que ofrezca el agente. Si alguna no es descargable, construirla en Excel a partir de los datos tabulares que entregue Analista y guardarla como imagen; no afirmar que la generó el agente.

**Paso 4.** Verificar que el gráfico de barras presenta exactamente cuatro promedios, que el gráfico circular suma **100 %**, que la dispersión utiliza pares de datos de la misma respuesta y que el mapa de calor contiene variables numéricas comparables.

### Resultado esperado

La práctica concluye cuando se cuenta con: un informe Word de tres tendencias, un Excel de promedios y análisis cuantitativo, un gráfico de barras en imagen, un Word de comentarios, una presentación ejecutiva PowerPoint y las visualizaciones estadísticas complementarias (histograma, circular, dispersión y mapa de calor). Los cálculos deben proceder de las **120 respuestas originales** y ser verificables; cuando una exportación nativa no esté disponible, los archivos se materializan con las aplicaciones Microsoft 365 a partir de resultados comprobados de Analista.

