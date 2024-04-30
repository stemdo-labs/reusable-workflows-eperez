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
