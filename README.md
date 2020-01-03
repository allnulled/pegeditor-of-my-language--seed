# quiero-mi-lenguaje

Con `quiero-mi-lenguaje` puedes construir rápidamente:
 - un lenguaje de programación
 - una gramática de editor
 - un editor personalizado
 - una línea de comandos
 - una API para `javascript` (`node` y `browser`).

# comandos

Los siguientes comandos `npm` están disponibles en los proyectos `quiero-mi-lenguaje`:
 - `npm run serve-and-open`: inicia el servidor y abre la aplicación con el navegador.
 - `npm run serve`: inicia el servidor.
 - `npm run build`: empaqueta la aplicación.
 - `npm run develop`: inicia el modo desarollo (compilación automática del lenguaje).
 - `npm run test`: ejecuta los tests.
 - `npm run open`: abre la aplicación con el navegador.
 - `npm run document`: genera toda la documentación del lenguaje.
 - `npm run git-create`: crea un proyecto git nuevo. Requiere `git` instalado.
 - `npm run git-push-application`: sube la aplicación. Requiere `git` instalado.
 - `npm run git-push-language`: sube el lenguaje. Requiere `git` instalado.
 - `npm run push`: sube la aplicación y el lenguaje. Requiere `git` instalado.

# carpetas y ficheros

Las siguientes carpetas y ficheros están presentes en un proyecto así:
 - **/bin**: carpeta de binarios, ficheros destinados a ser ejecutados mediante línea de comandos.
 - **/dist**: carpeta de distribución, ficheros y la aplicación final.
 - **/doc**: carpeta de documentación, ficheros de documentación del proyecto.
 - **/src**: carpeta de ficheros fuente, ficheros de la aplicación y lenguaje.
 - **/test**: carpeta de ficheros de test, ficheros destinados a ser ejecutados como pruebas.

# flujo de trabajo

Los flujos de trabajo son pasos a seguir con los que se realiza cierto trabajo.

1. `npm run git-init`: inicia el repositorio en git o inicializa git.
2. `npm run serve`: iniciamos el servidor de la aplicación.
3. `npm run develop`: iniciamos el estado de desarrollo.
4. abrimos un navegador por `http://127.0.0.1:8080/index.html`
  - deberíamos ver un editor con dos paneles.
5. editamos el fichero del lenguaje:
  - **src/lib/mylanguage.parser.pegjs**: lenguaje.
    - automáticamente, la consola se ocupará de recompilar el lenguaje.
6. la edición de estos ficheros no necesita compilación (modo `develop`):
  - **src/lib/codemirror.mode-mylanguage.js**: gramática del lenguaje en el editor.
  - **src/lib/codemirror.mode-mylanguage.css**: estilos de la gramática del lenguaje en el editor.
  - **src/lib/index.js**: lógica del editor.
  - **src/lib/index.css**: estilos del editor.
  - **src/index.html**: vista del editor.
7. refrescamos la página para observar los cambios.
8. `npm run git-push-language`: subimos los cambios al repositorio del lenguaje.
9. `npm run git-push-gh`: subimos los cambios al repositorio de la aplicación.

