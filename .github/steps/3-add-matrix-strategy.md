<!--
  <<< Notas del autor: Paso 3 >>>
  Comienza este paso reconociendo el paso anterior.
  Define términos y enlaza a docs.github.com.
-->

## Paso 3: Agregar una estrategia de matriz a tu flujo de trabajo

_¡Bien hecho! :sparkles:_

Tu **My Starter Workflow** ahora tiene un trabajo que produce la versión de node 14 y llama al flujo de trabajo reutilizable llamado **Flujo de trabajo reutilizable**. Luego, imprime un mensaje en los registros de Actions de la versión de node para la compilación. Aún no hemos revisado los registros de Actions en este punto para ver el mensaje, pero no te preocupes, llegaremos allí después de este próximo paso. Mejoremos un poco más nuestro **My Starter Workflow** agregando una estrategia de matriz.

**¿Qué es una estrategia de matriz?**: Una estrategia de matriz te permite utilizar variables en una definición de trabajo única para crear automáticamente múltiples ejecuciones de trabajo que se basan en las combinaciones de las variables. Por ejemplo, puedes usar una estrategia de matriz para probar tu código en múltiples versiones de un lenguaje o en múltiples sistemas operativos. A continuación se muestra un ejemplo:


```yaml
jobs:
  example_matrix:
    strategy:
      matrix:
        version: [10, 12, 14]
        os: [ubuntu-latest, windows-latest]
```

Para definir una estrategia de matriz dentro de un trabajo, primero necesitas definir la matriz con la palabra clave `strategy`, seguida de la palabra clave anidada `matrix`. Luego puedes definir variables para la matriz. En el ejemplo anterior, las variables son `version` con los valores `10, 12 y 14`, y otra variable llamada `os` con los valores `ubuntu-latest y windows latest`.

El trabajo `example_matrix` se ejecutará para cada combinación posible de las variables. Entonces, en el ejemplo anterior, el flujo de trabajo ejecutará seis trabajos, uno para cada combinación de las variables os y version. Si deseas ejecutar un trabajo para múltiples versiones, utilizar una estrategia de matriz es una solución excelente en lugar de escribir 6 trabajos diferentes.

Agreguemos una estrategia de matriz al **My Starter Workflow** para que podamos ejecutar nuestro trabajo en diferentes versiones de node en lugar de la única versión codificada de 14.

### :keyboard: Actividad: Usa una estrategia de matriz para ejecutar múltiples versiones

1. En el mismo archivo `my-starter-workflow.yml`, agrega una palabra clave `strategy` debajo del trabajo `call-reusable-workflow`.
1. Bajo `strategy`, agrega una palabra clave `matrix`.
1. Define la variable `nodeversion` para ejecutar sobre las siguientes versiones de node `[14, 16, 18, 20]`.
1. Reemplaza el parámetro `node` codificado en duro de 14 utilizado en el comando `with`, y llama a `nodeversion` en la matriz usando la siguiente sintaxis `${{ matrix.nodeversion }}`. A continuación, se muestra cómo debería lucir tu trabajo:


   ```yaml
   call-reusable-workflow:
     strategy:
       matrix:
         nodeversion: [14, 16, 18, 20]
     uses: ./.github/workflows/reusable-workflow.yml
     with:
       node: ${{ matrix.nodeversion }}
   ```

1. Para confirmar tus cambios, haz clic en **Comenzar confirmación** y luego en **Confirmar cambios**.
1. Espera unos 20 segundos para que se ejecuten las acciones, luego actualiza esta página (la que estás siguiendo las instrucciones) y una acción cerrará automáticamente este paso y abrirá el siguiente.

