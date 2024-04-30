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
    <<< Notas del autor: Inicio del curso >>>
    Incluye botón de inicio, una nota sobre los minutos de Actions,
    y dile al aprendiz por qué debería tomar el curso.
-->

## Bienvenido

Los flujos de trabajo reutilizables ofrecen una forma simple y poderosa de evitar copiar y pegar flujos de trabajo en tus repositorios, y agregar una estrategia de matriz te permite usar variables en una definición de trabajo única para crear automáticamente múltiples ejecuciones de trabajo.

- **Para quién es esto**: Desarrolladores, ingenieros DevOps, estudiantes, gerentes, equipos, usuarios de GitHub.
- **Lo que aprenderás**: Cómo crear y usar flujos de trabajo reutilizables, crear una estrategia de matriz, desencadenar flujos de trabajo y encontrar registros de flujos de trabajo.
- **Qué construirás**: Un flujo de trabajo de Actions con una estrategia de matriz que llama a un flujo de trabajo reutilizable para generar múltiples versiones de node.
- **Prerrequisitos**: En este curso trabajarás con solicitudes de extracción y archivos de flujo de trabajo YAML. Te recomendamos que primero tomes el curso [Introducción a GitHub](https://github.com/skills/introduction-to-github) o estés familiarizado con los conceptos básicos de GitHub, y el curso [Hola GitHub Actions](https://github.com/skills/hello-github-actions) para una introducción a GitHub Actions y los archivos de flujo de trabajo.
- **Duración**: Este curso se puede completar en menos de una hora.
- **Atribución**: Este curso de Skills fue inspirado por un [video demostrativo](https://www.youtube.com/watch?v=MBpyouQtY_M) creado por Mickey Gousset ([@mickeygousset](https://github.com/mickeygousset)).

En este curso, aprenderás a:

1. Hacer un flujo de trabajo reutilizable
2. Agregar un trabajo
3. Agregar una estrategia de matriz
4. Fusionar tu solicitud de extracción
5. Desencadenar el flujo de trabajo


### Cómo comenzar este curso siendo stemdoer

Simplemente espera, esta vista cambiará. 
Haz click en la pestaña ``Actions`` y observa algo se está ejecutando.

### No eres stemdoer

Adelante haz click en el botón.


[![comenzar-curso](https://user-images.githubusercontent.com/1221423/235727646-4a590299-ffe5-480d-8cd5-8194ea184546.svg)](https://github.com/new?template_name=reusable-workflows&template_owner=stemdo-labs&visibility=public)

1. Haz clic derecho en **Comenzar curso** y abre el enlace en una nueva pestaña.
2. En la nueva pestaña, la mayoría de las opciones se completarán automáticamente.
   - Para el propietario, elige tu cuenta personal o una organización para alojar el repositorio.
   - Recomendamos crear un repositorio público, ya que los repositorios privados [utilizarán minutos de Actions](https://docs.github.com/billing/managing-billing-for-github-actions/about-billing-for-github-actions).
   - Desplázate hacia abajo y haz clic en el botón **Crear repositorio** en la parte inferior del formulario.
3. Después de que se cree tu nuevo repositorio, espera unos 20 segundos, luego actualiza la página. Sigue las instrucciones paso a paso en el README del nuevo repositorio.

<footer>

<!--
  <<< Notas del autor: Pie de página >>>
  Agrega un enlace para obtener soporte, página de estado de GitHub, código de conducta, enlace de licencia.
-->

---

Obtén ayuda: [Publica en nuestro foro de discusión](https://github.com/orgs/skills/discussions/categories/test-with-actions) &bull; [Revisa la página de estado de GitHub](https://www.githubstatus.com/)

&copy; 2023 GitHub &bull; [Código de Conducta](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [Licencia MIT](https://gh.io/mit)

</footer>
