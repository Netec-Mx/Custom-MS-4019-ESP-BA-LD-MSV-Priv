
# Práctica 3. Uso de un agente precompilado de tu elección

## Objetivo de la práctica:

Al finalizar la práctica, serás capaz de:

- Seleccionar y utilizar un agente precompilado de Microsoft 365 Copilot adecuado para una necesidad concreta de trabajo.
- Producir y revisar el entregable correspondiente a la función del agente elegido.
- Identificar las limitaciones del resultado antes de utilizarlo en un contexto empresarial.

## Duración aproximada:

- 19 minutos.

## Tabla de ayuda:

| Agente | Uso previsto | Entregable previsto |
| --- | --- | --- |
| Asistente de solicitudes / Prompt Coach | Optimizar una indicación de trabajo. | Prompt mejorado e incorporación a la biblioteca de indicaciones cuando esté disponible. |
| Entrenador de ideas / Idea Coach | Proponer enfoques para un desafío. | Presentación, infografía o plan de implementación. |
| Asistente de escritura / Writing Coach | Revisar y adaptar una comunicación. | Dos versiones para públicos distintos, en Word, Outlook o Página de Copilot. |
| Agente de aprendizaje / Learning Coach | Desarrollar una habilidad y un plan de aprendizaje. | Síntesis de aprendizaje y plan con criterios de seguimiento; infografía o calendario Excel. |

## Instrucciones

Un colaborador debe seleccionar el agente precompilado más adecuado para una necesidad concreta: mejorar una indicación, proponer ideas, revisar una comunicación o apoyar su aprendizaje. Elegirás una ruta, ejecutarás la interacción y revisarás su resultado.

### Tarea 1. Elegir el agente precompilado (3 minutos)

**Paso 1.** Abrir [Microsoft Copilot](https://m365.cloud.microsoft.com/) con la cuenta autorizada, seleccionar **Agentes** o **Todos los agentes** y buscar los cuatro agentes de la tabla. Si alguno no aparece, abrir la Tienda de agentes y verificar si la organización permite agregarlo.

**Paso 2.** Elegir una de las rutas A, B, C o D de la siguiente tarea, de acuerdo con el resultado que se necesite. Los agentes son opciones alternativas dentro del **mismo ejercicio**; no es necesario crear cuatro prácticas ni ejecutar todas las rutas.

**Paso 3.** Abrir el agente seleccionado. Si la etiqueta de la organización está en inglés, identificarlo por el nombre inglés de la tabla. Comenzar una nueva conversación.

### Tarea 2. Realizar la actividad del agente elegido (12 minutos)

**Paso 1.** Seleccionar una de las cuatro rutas y realizar únicamente las acciones correspondientes a ese agente. Los pasos internos de cada ruta se identifican como **Acción** para distinguirlos de los pasos generales de la tarea.

#### Ruta A. Asistente de solicitudes (Prompt Coach)

**Acción 1.** Introducir una solicitud inicial relacionada con un reto de seguimiento del proyecto.

**Prompt A1 — Mejorar la instrucción**

```text
Necesito mejorar este prompt para Microsoft 365 Copilot:
"Haz un resumen del estado de mi proyecto".

Mi contexto es Project Nexus, donde debo revisar avances, bloqueos,
responsables y próximos compromisos. Ayúdame a convertirlo en una
instrucción clara que incluya objetivo, contexto, fuentes, formato de
salida y criterios de calidad. No inventes datos del proyecto.
Explica brevemente los cambios que realizaste.
```

**Acción 2.** Revisar que la versión mejorada incluya las fuentes, el periodo, el formato, la obligación de citar y la regla de no inventar datos. Solicitar un único ajuste cuando falte alguno.

**Acción 3.** Copiar el prompt mejorado y guardarlo en la **biblioteca o galería de indicaciones de Copilot**, si la opción está disponible en el tenant. Si la política no habilita guardar indicaciones, conservar el texto en la conversación, identificando la limitación sin afirmar que se añadió a la biblioteca.

#### Ruta B. Entrenador de ideas (Idea Coach)

**Acción 1.** Introducir un desafío del proyecto y pedir varias ideas contrastables.

**Prompt B1 — Generar y comparar soluciones**

```text
Ayúdame a generar ideas para que los participantes de Project Nexus
localicen más rápido las instrucciones vigentes de atención. Propón cuatro
alternativas distintas que puedan aplicarse con herramientas habituales
de Microsoft 365. Para cada alternativa indica: beneficio esperado,
esfuerzo relativo, principal dificultad y una forma de verificar su utilidad.
Evita suponer que hay una integración o automatización ya aprobada.
```

**Acción 2.** Comparar las cuatro ideas y seleccionar una que pueda explicarse con evidencia. Pedir al agente que justifique la elección sin presentar una estimación como ahorro comprobado.

**Prompt B2 — Convertir una idea en entregable**

```text
A partir de las cuatro propuestas, elige una alternativa y prepara el
contenido de un plan de implementación de una página en Word que incluya:
problema, solución elegida, actividades principales, responsables por
función, riesgos, indicador de éxito y criterio de aprobación.
Distingue responsables propuestos de responsables confirmados.
```

**Acción 3.** Guardar el plan en Word. Si se prefiere otra salida autorizada por el temario, solicitar una presentación PowerPoint o una infografía con la misma propuesta y revisar su contenido.

#### Ruta C. Asistente de escritura (Writing Coach)

**Acción 1.** Utilizar el borrador proporcionado en el siguiente prompt, sin introducir datos personales.

**Prompt C1 — Dos comunicaciones para audiencias diferentes**

```text
Revisa este borrador sobre Project Nexus:
"Buen día. El piloto avanza, pero faltan permisos para dos personas y
el protocolo todavía está pendiente de aprobación. Necesitamos confirmar
quién resuelve los accesos y cuándo estará el documento final."

Corrige claridad, gramática y tono. Después genera dos versiones:
A) correo breve para el equipo operativo, con tareas y fechas por confirmar;
B) comunicación ejecutiva para la dirección, con situación, impacto y
próximo paso. No inventes fechas ni afirmes que el problema ya se resolvió.
Explica las diferencias principales entre ambas versiones.
```

**Acción 2.** Comparar las dos versiones y comprobar que la información esencial no cambió. Solicitar corrección si alguna añade fechas o decisiones no confirmadas.

**Acción 3.** Guardar las versiones en Word, en dos borradores de Outlook o en una Página de Copilot según las opciones habilitadas. No enviar comunicaciones como parte del ejercicio.

#### Ruta D. Agente de aprendizaje (Learning Coach)

**Acción 1.** Plantear un escenario de desarrollo rápido de habilidades para un colaborador de Banco Agrícola.

**Prompt D1 — Aprender una habilidad y comprobarla**

```text
Simula que trabajo en un equipo operativo de Banco Agrícola y necesito
aprender rápidamente a identificar riesgos operativos habituales antes de
escalar una incidencia. Tengo conocimientos generales del proceso, pero
no formación especializada en gestión de riesgos.

Prepara una microexperiencia de aprendizaje de 10 minutos: conceptos
básicos, tres ejemplos situacionales y cuatro preguntas de comprobación.
Hazme una pregunta a la vez y espera mis respuestas. Al final, explícame
qué he comprendido, qué debo repasar y dos acciones concretas para aplicar
lo aprendido en el trabajo. No presentes la actividad como formación
normativa oficial del banco.
```

**Acción 2.** Responder las preguntas del agente y obtener una síntesis de conceptos, resultados del ejercicio de comprobación y dos acciones de aplicación laboral.

**Acción 3.** Abrir una nueva petición al mismo agente para elaborar el plan de desarrollo personalizado.

**Prompt D2 — Plan de aprendizaje**

```text
Supón que soy un colaborador de un banco que quiere asumir funciones de
coordinación de procesos. Mi punto de partida es conocimiento básico de
Microsoft 365, experiencia operativa y disponibilidad para estudiar dos
horas por semana durante cuatro semanas.

Elabora un plan de aprendizaje personalizado con: meta profesional,
tres competencias prioritarias, actividades por semana, criterios
observables de progreso y un mecanismo breve de autoevaluación.
Revisa el plan para que sea compatible con dos horas semanales.
Entrega también una tabla de calendario que pueda trasladarse a Excel
o a una infografía. No inventes cursos corporativos ni certificaciones.
```

**Acción 4.** Guardar la síntesis y el plan; pasar la tabla de cuatro semanas a Excel si no existe descarga directa. Comprobar que cada semana incluya una actividad y un criterio verificable de progreso.

**Paso 2.** Comprobar que se obtuvo el producto indicado para la ruta seleccionada antes de pasar a la Tarea 3.

### Tarea 3. Revisar y conservar el entregable seleccionado (4 minutos)

**Paso 1.** Comparar la respuesta del agente con la solicitud original de la ruta elegida. Identificar, según el caso, una indicación mejorada, una propuesta elegida, dos textos diferenciados o una síntesis y plan de aprendizaje.

**Paso 2.** Corregir la información no sustentada mediante una indicación al agente. Si el resultado se requiere en Word, PowerPoint o Excel, abrir la aplicación correspondiente y guardar el contenido, sin presuponer disponibilidad de exportación automática.

**Paso 3.** Comprobar que el resultado conserva el contexto de la actividad y que no hace afirmaciones no verificadas. Mantener el archivo o la indicación como producto de la práctica.

### Resultado esperado

Se ha utilizado al menos **un agente precompilado** y obtenido su producto verificable: un prompt optimizado, una propuesta transformada en artefacto, dos versiones de comunicación o una síntesis y un plan de aprendizaje personalizado. Las rutas constituyen alternativas para una sola práctica de 19 minutos.

