---
permalink: /Capitulo03/Practica07/
---

# Práctica 7. Compartir agentes y comprobar roles y permisos

## Objetivo de la práctica:

Al finalizar la práctica, serás capaz de:

- Compartir un agente creado con Agent Builder mediante Microsoft 365 Copilot y distribuir su vínculo por Teams.
- Comprobar la diferencia entre **Puede chatear** y **Puede editar** mediante cuentas distintas.
- Verificar que el permiso para abrir un agente no otorga automáticamente acceso a todos los documentos que utiliza como conocimiento.
- Modificar y revocar el acceso al agente y comprobar el resultado.

## Duración aproximada:

- 30 minutos.

## Tabla de ayuda:

| Elemento | Valor | Uso |
| --- | --- | --- |
| Aplicación | [Microsoft 365 Copilot](https://m365.cloud.microsoft.com/) | Compartir y administrar el acceso al agente. |
| Canal para el vínculo | Microsoft Teams | Distribuir el enlace en un chat con usuarios autorizados. |
| Agente de roles | `Nova Procedimientos` o agente propio de la práctica 5 | Comprobar permisos de conversación y edición. |
| Agente para fuentes | `Nova Seguimiento` | Comprobar lectura de una fuente en OneDrive. |
| Archivo origen | [Solicitudes_Nova.xlsx](../Practica06/recursos/Solicitudes_Nova.xlsx) | Fuente del agente de seguimiento. |
| Cuenta A | Creador del agente | Propietario inicial. |
| Cuenta B | Colaborador del mismo tenant | Usuario de chat; acceso al Excel inicialmente no otorgado. |
| Cuenta C | Colaborador del mismo tenant | Copropietario con acceso de edición. |
| Cuenta D | Colaborador no agregado al agente (cuando esté disponible) | Comprobación de acceso denegado. |

> **Importante:** Se requieren identidades reales y distintas del **mismo tenant** para comprobar permisos. No es válido cambiar únicamente de ventana de navegador conservando la misma cuenta. Los controles y la posibilidad de compartir están sujetos a las políticas del administrador y a la licencia de los destinatarios.

## Instrucciones

El equipo de la Unidad de Servicios Nova necesita distribuir sus agentes sin dar a todos facultades de modificación ni exponer fuentes que cada colaborador no tiene autorizado consultar. Utilizarás dos agentes del ejercicio anterior y comprobarás las consecuencias de compartirlos desde Copilot y de enviar sus vínculos por Teams.

### Tarea 1. Preparar cuentas y comprobar la configuración inicial (4 minutos)

**Paso 1.** Organizarse con el instructor o con compañeros para disponer de las cuentas **A**, **B** y **C**, y de la cuenta **D** cuando el entorno lo permita. Confirmar que los participantes tienen acceso a Microsoft 365 Copilot según las licencias habilitadas.

**Paso 2.** Iniciar sesión como **A**, abrir **Mis agentes / Agentes propios**, localizar `Nova Procedimientos` y comprobar que se puede utilizar y editar desde esa cuenta.

**Paso 3.** Abrir el menú **Compartir / Share** del agente y revisar la lista de usuarios autorizados. Confirmar que no está activado el acceso a toda la organización, si el control está disponible. Si ya hay destinatarios agregados por otra actividad, utilizar otro agente propio con un alcance controlado.

**Paso 4.** Acordar qué comprobará cada cuenta: **A** administra; **B** puede chatear sin editar; **C** puede editar; **D** no recibe permisos. No introducir información interna de clientes en las pruebas.

### Tarea 2. Compartir desde Copilot y contrastar los roles (8 minutos)

**Paso 1.** Seleccionar desde la cuenta **A** **Compartir** en `Nova Procedimientos`, buscar a **B** por su nombre o dirección de la organización y elegir el rol **Puede chatear / Can chat**. Seleccionar **Agregar** y comprobar que figura en el listado.

**Paso 2.** Agregar a **C** mediante la misma ventana, pero con el rol **Puede editar / Can edit**. Confirmar que **C** aparece como persona con permiso de administración o copropietario. No seleccionar un grupo de seguridad para el rol de propietario: Microsoft solo permite asignarlo a personas individuales.

**Paso 3.** Solicitar a **B** que abra el agente desde el vínculo de chat o la notificación, y enviar este prompt:

**Prompt 1 — Prueba del usuario de chat**

```text
Consulta el manual y dime qué pasos se siguen para registrar una
solicitud y cuándo corresponde escalar un incidente de prioridad Alta.
```

**Paso 4.** Confirmar que **B** puede conversar con el agente pero no puede modificar sus instrucciones, conocimiento ni destinatarios autorizados. Si solo se muestra un botón de uso del agente y no aparece edición, ese comportamiento es el esperado.

**Paso 5.** Solicitar a **C** que abra el agente, ingrese en **Editar** y compruebe que aparecen sus instrucciones e indicaciones. Para no interrumpir el ejercicio, evitar cambios destructivos; agregar temporalmente una indicación sugerida si se requiere verificar la facultad de edición y retirarla después.

**Paso 6.** Solicitar a **D**, si existe, abrir el mismo vínculo sin haber sido agregado. Comprobar que no puede utilizar el agente o que se exige solicitar autorización. Si no se cuenta con **D**, no declarar ejecutada la comprobación de acceso denegado.

### Tarea 3. Compartir el vínculo por Teams sin modificar permisos (7 minutos)

**Paso 1.** Volver desde la cuenta **A** a **Compartir** y seleccionar **Copiar vínculo de chat / Copy chat link** del agente `Nova Procedimientos`.

**Paso 2.** Abrir Microsoft Teams y entrar en un chat individual o de grupo autorizado con **B** y **C**. Enviar el vínculo acompañado de este mensaje de contexto:

```text
Agente Nova Procedimientos: consulta el manual de atención de
solicitudes y los criterios de escalamiento.
Abre el enlace con tu cuenta corporativa y comprueba qué permisos
tienes sobre el agente.
```

**Paso 3.** Solicitar a **B** que abra el vínculo recibido en Teams, complete una pregunta del agente y compruebe que **no** dispone de edición. Solicitar a **C** comprobar que puede abrir el agente y continuar administrándolo.

**Paso 4.** Comprobar que el envío del vínculo a un chat no agregó nuevos permisos. Si **D** recibe el mismo mensaje reenviado, su situación de acceso debe seguir dependiendo de los permisos otorgados en Copilot, no de la posesión del enlace.

> **Importante:** En esta práctica, **compartir por Teams significa enviar el enlace** para abrir el agente. Los agentes creados con Agent Builder no se convierten automáticamente en un bot que responda como miembro de un chat individual o de grupo de Teams. Esa publicación multicanal no forma parte del curso.

### Tarea 4. Comprobar los permisos de la fuente de OneDrive (8 minutos)

**Paso 1.** Abrir desde la cuenta **A** `Nova Seguimiento` y verificar que su conocimiento procede del archivo **`Solicitudes_Nova.xlsx` guardado en OneDrive**, no de un archivo incorporado desde el equipo.

**Paso 2.** Compartir el agente `Nova Seguimiento` con **B** como **Puede chatear** desde Copilot. No compartir aún el archivo de OneDrive.

**Paso 3.** Solicitar a **B** abrir el agente y preguntar:

**Prompt 2 — Comprobación de acceso a la fuente**

```text
Según el archivo Solicitudes_Nova.xlsx, ¿cuál es el estado exacto
y la acción siguiente de SOL-2026-1003? Indica si puedes consultar
el registro o si no tienes acceso a la fuente.
```

**Paso 4.** Comprobar que **B** no puede fundamentar la respuesta en el registro si no tiene permiso sobre el archivo. Si responde con datos que no puede verificar, no considerarlos evidencia de acceso válido. Revisar que **B** no haya recibido permisos al Excel por otra vía.

**Paso 5.** Seleccionar desde OneDrive con la cuenta **A** `Solicitudes_Nova.xlsx` → **Compartir**, agregar a **B** con permiso **Puede ver / Can view** y sin conceder edición. Confirmar que **B** puede abrir el Excel desde su cuenta.

**Paso 6.** Solicitar a **B** repetir la consulta del Prompt 2. Comparar los datos con la fila del registro y verificar que el agente ahora pueda fundamentar la respuesta cuando la fuente esté disponible. Si se acaba de agregar el archivo, actualizar la fuente o permitir el tiempo de indexación correspondiente.

**Paso 7.** Retirar después el acceso de **B** al archivo si así lo requiere el instructor. Explicar a partir de las pruebas que **el acceso al agente** y **el acceso al documento de OneDrive** son controles independientes.

> **Precaución:** Los documentos **incorporados directamente al agente** tienen un comportamiento de acceso distinto: su contenido puede quedar disponible para quien tenga acceso al agente. Por eso esta prueba de permisos utiliza una **fuente de OneDrive**.

### Tarea 5. Modificar y revocar permisos y comprobar el resultado (3 minutos)

**Paso 1.** Abrir desde la cuenta **A** **Compartir** en `Nova Procedimientos` y cambiar temporalmente el rol de **B** de **Puede chatear** a **Puede editar**, si la política del tenant permite el cambio. Solicitar a **B** confirmar que aparece la edición; devolverlo a **Puede chatear**.

**Paso 2.** Retirar el acceso de **B** al agente o utilizar la opción **Quitar / Remove**. Solicitar que vuelva a abrir el vínculo. Comprobar el acceso efectivamente observado; si persiste una sesión previa, renovar la sesión y considerar la propagación de permisos antes de concluir el resultado.

**Paso 3.** Mantener un único conjunto final de destinatarios autorizados y revisar el estado de uso compartido. Conservar los agentes para uso de la formación sin activar el acceso general del tenant.

### Resultado esperado

El agente `Nova Procedimientos` se compartió desde Microsoft 365 Copilot y su vínculo se transmitió en Teams. Se verificó con usuarios diferenciados que **Puede chatear** permite consultar, mientras **Puede editar** otorga facultades de administración. Se comprobó, cuando existió una cuenta sin permisos, que el enlace por sí solo no concede acceso. Para `Nova Seguimiento` se contrastó el comportamiento con y sin permiso de lectura del libro en OneDrive. Finalmente, se probó la modificación o revocación del acceso conforme a las opciones disponibles en el tenant, sin tratar a Teams como un canal de publicación del agente.

[Volver al capítulo 3](../)
