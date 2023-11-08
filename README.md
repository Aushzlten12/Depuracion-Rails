# Actividad

## Depuracion en Rails

Para realizar aquello, usaré la aplicación de Rails realizada en la Practica Calificada 2.

### Acciones
1. Muestra la descripción detallada de un objeto en una vista. Por ejemplo, pruebA a insertar `= debug(@movie)` o `= @movie.inspect` en cualquier vista (donde el signo `=` le dice a Haml que ejecute el código e inserta el resultado en la vista).
2. Deten la ejecución dentro de un método de un controlador lanzando una excepción cuyo mensaje sea una representación del valor que quieres inspeccionar, por ejemplo, `raise params.inspect`
3. Para ver el valor detallado de la hash `params` dentro del método de un controlador. Rails desplegará el mensaje de la excepción como la página web resultante de la petición.
4. Usa `logger.debug( mensaje)` para imprimir el mensaje al fichero de logging. `logger` está disponible en los modelos y en los controladores y puede registrar mensajes con
distintos niveles de importancia. Compara `config/environments/production.rb` con `development.rb` para ver cómo difieren los niveles logs por defecto entre
los entornos de producción y desarrollo.

### Segunda Forma

Instala la gema `debugger` a través de Gemfile, para usar el depurador en una aplicación Rails. 

Arranca el servidor de la aplicación usando  `rails server --debugger`, e inserta la sentencia `debugger` en un punto del código donde desees y detiene el programa. Cuando
llegas a esa sentencia, la ventana del terminal donde arrancó el servidor te dará el prompt del depurador. 