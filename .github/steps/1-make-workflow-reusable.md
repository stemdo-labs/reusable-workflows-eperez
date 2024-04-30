<!--
  <<< Notas del autor: Paso 1 >>>
  Elige 3-5 pasos para tu curso.
  ¡El primer paso siempre es el más difícil, así que elige algo fácil!
  Enlaza a docs.github.com para más explicaciones.
  ¡Anima a los usuarios a abrir nuevas pestañas para los pasos!
-->

## Paso 1: Hacer un flujo de trabajo reutilizable

_Bienvenido a "Flujos de trabajo reutilizables y estrategias de matriz"! :wave:_

¡Puedes hacer mucho con GitHub Actions! Puedes automatizar tareas repetitivas, construir tuberías de integración y despliegue continuo, y personalizar prácticamente cualquier parte de tu flujo de trabajo de desarrollo de software. No importa si estás aprendiendo sobre flujos de trabajo y GitHub Actions por primera vez o si tienes mucha experiencia con el proceso, pronto te encontrarás repitiendo trabajos y pasos de automatización dentro del mismo flujo de trabajo, e incluso usando el temido método de copiar y pegar para los flujos de trabajo en múltiples repositorios.

¿Existe una solución para reducir estas tareas repetitivas? ¡Sí, me alegra que lo hayas preguntado! :wink: Ingresa a los **flujos de trabajo reutilizables**, una forma simple y poderosa de evitar copiar y pegar flujos de trabajo en tus repositorios.

**¿Cuáles son los beneficios de usar flujos de trabajo reutilizables?**: Los flujos de trabajo reutilizables son ... reutilizables. Los flujos de trabajo reutilizables te permiten aplicar el principio DRY (don’t repeat yourself) a tus configuraciones de Actions, por lo que no necesitas copiar y pegar tus flujos de trabajo de un repositorio a otro.

- Por ejemplo: si tienes tres aplicaciones Node diferentes y las estás construyendo de la misma manera, puedes usar un flujo de trabajo reutilizable en lugar de copiar y pegar tus flujos de trabajo una y otra vez.

**Tengo un flujo de trabajo, ¿cómo lo hago reutilizable?**: Un flujo de trabajo reutilizable es igual que cualquier flujo de trabajo de GitHub Actions con una diferencia clave: incluye un disparador de evento `workflow_call`, similar a los disparadores de eventos como `push`, `issues`, y `workflow_dispatch`. Esto significa que todo lo que necesitas hacer para hacer un flujo de trabajo reutilizable es usar el disparador de evento de llamada de flujo de trabajo.

¡Comencemos con nuestro primer paso para ver cómo funcionaría esto!

### :keyboard: Actividad: Agregar un disparador `workflow_call` a un flujo de trabajo

1. Abre una nueva pestaña del navegador y navega a este mismo repositorio. Luego, trabaja en los pasos en tu segunda pestaña mientras lees las instrucciones en esta pestaña.
1. Ve a la pestaña **Code**.
1. Desde el menú desplegable de la rama **stemdo**, haz clic en la rama **reusable-workflow**.
1. Navega hasta la carpeta `.github/workflows/`, luego selecciona el archivo **reusable-workflow.yml**.
1. Reemplaza el disparador de evento `workflow_dispatch` con el disparador de evento `workflow_call`. Debería verse como sigue:


   ```yaml
   name: Reusable Workflow

   on:
     workflow_call:
       inputs:
         node:
           required: true
           type: string
   ```

1. Para confirmar tus cambios, haz clic en **Start commit**, y luego en **Commit changes**.
1. (opcional) Crea una solicitud de extracción para ver todos los cambios que realizarás a lo largo de este curso. Haz clic en la pestaña **Pull Requests**, luego en **New pull request**, establece `base: stemdo` y `compare: reusable-workflow`.
1. Espera unos 20 segundos para que se ejecuten las acciones, luego actualiza esta página (la que estás siguiendo para las instrucciones) y una acción cerrará automáticamente este paso y abrirá el siguiente.
