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
  <<< Notas del autor: Paso 5 >>>
  Comienza este paso reconociendo el paso anterior.
  Define términos y enlaza a docs.github.com.
-->

## Paso 5: Dispara tu flujo de trabajo y ve los registros de acciones

_¡Ya casi terminas. ¡Último paso! :heart:_

Ahora que los cambios han sido fusionados en la rama `stemdo`, ¡disparemos el flujo de trabajo **My Starter Workflow** para ver todo en acción! Pero antes de hacerlo, recordemos qué deberíamos esperar ver antes de ejecutar el flujo de trabajo.

- Deberíamos esperar ver cinco trabajos ejecutándose desde nuestro \*My Starter Workflow\*\*. ¿Recuerdas cuáles son? Tenemos el trabajo `build` y luego el trabajo `call-reusable-workflow` que tiene la estrategia de matriz.
  ![Captura de pantalla 2022-09-08 a las 9.53.52 AM](https://user-images.githubusercontent.com/6351798/189220189-97361a5e-eecf-4666-a859-e0587354bafe.png)
- También deberíamos esperar ver el mensaje de eco impreso como una salida del flujo de trabajo reutilizable con la versión de nodo para cada uno de los trabajos de versión de matriz.
  ![Captura de pantalla 2022-09-08 a las 9.52.41 AM](https://user-images.githubusercontent.com/6351798/189220620-0576540a-366f-44e1-866c-2955af399cdb.png)


### :keyboard: Actividad: Ejecuta el flujo de trabajo My Starter y ve los registros de acciones

1. Navega a la pestaña **Actions** en tu repositorio.
1. Selecciona el flujo de trabajo **My Starter Workflow** en la izquierda, y elige el botón **Run workflow** para ejecutar el flujo de trabajo en la rama **stemdo**.
1. Espera unos segundos para que la ejecución del flujo de trabajo aparezca en la cola. Una vez que aparezca, selecciona el flujo de trabajo **My Starter Workflow** en la cola de ejecuciones de flujo de trabajo.

Observa la lista de trabajos de construcción a la izquierda. Uno para el trabajo `build` y cuatro para las diferentes versiones de nodo (14, 16, 18, 20) que estás ejecutando desde tu matriz. Cuando uno de los trabajos de versión de nodo se complete, puedes seleccionar ese trabajo y ver los registros de acciones para **Output the input value**. Esto imprimirá el mensaje del archivo de flujo de trabajo reutilizable.

Cuando hayas terminado de revisar los registros de acciones, ¡vuelve aquí y actualiza la página para terminar el curso! 🎉

<footer>

<!--
  <<< Notas del autor: Pie de página >>>
  Agrega un enlace para obtener soporte, página de estado de GitHub, código de conducta, enlace de licencia.
-->

---

Obtén ayuda: [Publica en nuestro foro de discusión](https://github.com/orgs/skills/discussions/categories/test-with-actions) &bull; [Revisa la página de estado de GitHub](https://www.githubstatus.com/)

&copy; 2023 GitHub &bull; [Código de Conducta](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [Licencia MIT](https://gh.io/mit)

</footer>
