<header>

<!--
  <<< Notas del autor: Encabezado del curso >>>
  Lee <https://skills.github.com/quickstart> para obtener más información sobre cómo construir cursos usando esta plantilla.
  Incluye una imagen de 1280×640, el nombre del curso en minúsculas con una descripción concisa en énfasis.
  En la configuración de tu repositorio: habilita el repositorio de plantillas, agrega tu imagen social de 1280×640, elimina automáticamente las ramas principales.
  Junto a "Acerca de", agrega descripción y etiquetas; deshabilita las versiones, paquetes y entornos.
  Agrega tu licencia de código abierto, GitHub utiliza la licencia MIT.
-->

# Flujos de trabajo reutilizables y estrategias de matriz

_Haz que un flujo de trabajo sea reutilizable, llámalo en otro flujo de trabajo y usa una estrategia de matriz para ejecutar múltiples versiones._

</header>

<!--
  <<< Notas del autor: Paso 2 >>>
  Comienza este paso reconociendo el paso anterior.
  Define términos y enlaza a docs.github.com.
-->

## Paso 2: Agregar un trabajo para llamar al flujo de trabajo reutilizable

_¡Buen trabajo! :tada: ¡Hiciste un flujo de trabajo reutilizable!_

Ahora que tienes un flujo de trabajo reutilizable, puedes llamarlo en otro flujo de trabajo dentro de un trabajo nuevo o existente. Pero antes de hacer eso, tomémonos un minuto para entender qué está haciendo nuestro flujo de trabajo reutilizable al observar el contenido del archivo.

**Comprendiendo el contenido del archivo de tu flujo de trabajo reutilizable**


```yaml
name: Reusable Workflow

on:
  workflow_call:
    inputs:
      node:
        required: true
        type: string

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v3

      - name: Output the input value
        run: |
          echo "The node version to use is: ${{ inputs.node }}"
```


El flujo de trabajo reutilizable requiere una `input` de `node` para que el flujo de trabajo funcione. Debes asegurarte de que el otro flujo de trabajo que estás utilizando para llamar a este flujo de trabajo reutilizable produzca una versión de node. Si se detecta una entrada de node, el flujo de trabajo iniciará un trabajo llamado `build` que se ejecuta en ubuntu-latest.

El paso dentro del trabajo `build` utiliza una acción llamada `checkout@v3` para hacer checkout del código y luego un paso para producir el valor de entrada mediante la ejecución de un comando echo para imprimir en la consola de registro de Actions el siguiente mensaje, `The node version to use is: ${{ inputs.node }}`. La entrada de node aquí es el valor de node producido que necesitas tener en tu otro flujo de trabajo.

Bien, ahora que sabemos qué hace el flujo de trabajo reutilizable, agreguemos un nuevo trabajo a otro flujo de trabajo llamado **my-starter-workflow** para llamar a nuestro flujo de trabajo reutilizable. Podemos hacer esto utilizando el comando `uses:` y luego estableciendo la ruta al flujo de trabajo que queremos usar. También necesitamos asegurarnos de definir esa entrada de node o el flujo de trabajo reutilizable no funcionará.


### :keyboard: Actividad: Agregar un trabajo a tu flujo de trabajo para llamar al flujo de trabajo reutilizable

1. Ve a la carpeta `.github/workflows/` y abre el archivo `my-starter-workflow.yml`.
1. Agrega un nuevo trabajo al flujo de trabajo llamado `call-reusable-workflow`.
1. Agrega un comando `uses` y establece la ruta del comando en el archivo `reusable-workflow.yml`.
1. Agrega un comando `with` para pasar un parámetro `node` y establecer el valor en `14`.


   ```yaml
   call-reusable-workflow:
     uses: ./.github/workflows/reusable-workflow.yml
     with:
       node: 14
   ```

1. Para confirmar tus cambios, haz clic en **Start commit**, y luego en **Commit changes**.
1. Espera unos 20 segundos para que se ejecuten las acciones, luego actualiza esta página (la que estás siguiendo para las instrucciones) y una acción cerrará automáticamente este paso y abrirá el siguiente.

<footer>

<!--
  <<< Notas del autor: Pie de página >>>
  Agrega un enlace para obtener soporte, página de estado de GitHub, código de conducta, enlace de licencia.
-->

---

Obtén ayuda: [Publica en nuestro foro de discusión](https://github.com/orgs/skills/discussions/categories/test-with-actions) &bull; [Revisa la página de estado de GitHub](https://www.githubstatus.com/)

&copy; 2023 GitHub &bull; [Código de Conducta](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [Licencia MIT](https://gh.io/mit)

</footer>
