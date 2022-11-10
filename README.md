# Detalles del proyecto
Se agregaron los archivos index.html, style.css e index.js, para fusionar algunos de los componentes de la vista principal.

Archivos y componentes fusionados:

- clase11.html (menu general)
- clase7.html (menu desktop)
- clase8.html (menu mobile)
- clase13.html (carrito de compras)
- clase6.html (lista de productos)
- clase12.html (detalle del producto)

Gracias a la fusión, los usuarios pueden utilizar el menú de navegación con todos sus componentes. Funciona en mobile, desktop, con el carrito de compras y los detalles de un producto; además de renderizar la lista de productos a partir de un array (hardcodeado). El contador de artículos funciona de manera interactiva, tanto para agregar como quitar productos de la lista de compra. En la lista de compra se pueden eliminar productos oprimiendo el botón rojo, y además, remueve precio del producto eliminado del total de la compra. Los detalles del producto cambia conforme se selecciona cada producto.

Todos los componentes se probaron individualmente y en conjunto, para que los usuarios tengan una buena experiencia. :)

**Quedan algunos issues con el botón de compra de los detalles del producto, se duplica al presionarse más de una vez y junta los botones de otros artículos ·-·.**

Demo en:  https://natsumychan.github.io/curso-frontend-javascript-practico/
<hr>

## Correcciones Javascript

### Botones que se repiten
Se verifica en el evento de la imagen (productImg) que no existan botones primarios en el estado de la tarjeta de detalles. Si existen se remueven.

### El botón principal de detalles no se elimina, se deshabilita
Se creó una clase en CSS para desactivar el botón. Pueden desactivarse los estilos en línea, pero es más ordenado hacerlo por medio de clases.
Asignamos la función del botón primario de detalles a una variable anónima, para nombrarla y poder remover el evento.
Removemos el evento y añadimos la clase creada dentro de esta función.

### Flecha del carrito no cierra el panel
Se creó una nueva constante para este elemento y se le añadió un evento al ser cliqueado. 

### No se cierra el panel de correo en Modo Desktop
Dada la lógica de la página al abrir el carrito debería cerrarse este panel.
En toggleAside se le añadió la clase "inactive" a desktopMenu.

## Posibles correcciones Javascript

* La lista de productos se podría leer de un archivo JSON, esto es más cercano a lo que se haría en la realidad, se puede guardar el JSON en un archivo y leerlo desde la URL del mismo.
* En las funciones se pueden poner todas las constantes al inicio y luego las acciones al final, siguiendo una lógica por ejemplo:  
  &nbsp;&nbsp;**Constantes $\rightarrow$ Cambio de atributos $\rightarrow$ Añadir o remover clases $\rightarrow$ Luego añadir nodos $\rightarrow$ Luego añadir eventos.**  
  Por ejemplo. Puede ser otro orden, pero mientras tenga coherencia se puede leer con más facilidad y depurar errores más fácilmente.
* Modularizar las funciones anónimas en funciones separadas, si están son muy largas (más de 5 líneas)
* Cambiar pointerDown por click, ya que pointerdown en escritorio también se activa con click derecho y click medio, lo cual no genera una buena experiencia.

## Ejercicio interesante Javascript

Darle funcionalidad al tab, para dar mayor accesibilidad por medio del teclado, dándole estilos al focus, con el atributo tabindex y con javascript.
