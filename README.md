# DOM
El DOM (Document Object Model) es una interfaz de programación para documentos HTML y XML. Representa la estructura de un documento como un árbol de nodos, donde cada nodo corresponde a una parte del documento, como un elemento, atributo, texto, etc.
El DOM permite a los lenguajes de programación, como JavaScript o Python, interactuar con el contenido, la estructura y el estilo de los documentos web de manera dinámica. Gracias al DOM, los desarrolladores pueden:

- Leer y modificar el contenido del documento, como el texto de un párrafo o el valor de un campo de formulario.
- Añadir, eliminar y reorganizar elementos en el documento.
- Alterar los estilos CSS aplicados a los elementos para cambiar su apariencia.
- Capturar eventos del usuario (como clics, movimientos del ratón o inputs) y reaccionar a ellos mediante scripts.

### Estructura del DOM

El DOM representa el documento como una estructura jerárquica de nodos, con el nodo raíz siendo el objeto document. Los nodos principales son:

1. Elementos (Element Nodes): Representan etiquetas HTML o XML, como `<div>`, `<p>`, `<a>`, etc.
2. Atributos (Attribute Nodes): Representan atributos de los elementos, como class, id, href, etc.
3. Texto (Text Nodes): Representan el contenido textual dentro de los elementos.
4. Comentarios (Comment Nodes): Representan los comentarios en el código HTML o XML.


##### Ejemplo de Estructura del DOM:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Estructura DOM</title>
  </head>
  <body>
    <h1 id="title">Hello Everyone</h1>
    <p class="text">Este es un párrafo.</p>
    <a href="https://www.ejemplo.com">Visita Ejemplo</a>
  </body>
</html>
```

Para este documento, la estructura del DOM es la siguiente:

```less
document
 ├── html
      ├── head
      │    └── title
      └── body
           ├── h1
           ├── p
           └── a
```


# Manipular el DOM desde la Consola

Para poder manipular el DOM desde la consola primero debemos saber los objetos que tiene, como el document, window, event, etc.


### Objetos Principales del DOM

#### Window

Representa la ventana del navegador. Es el objeto global en el contexto de un navegador web, lo que significa que todas las variables globales y funciones declaradas en el script se convierten en propiedades y métodos de window

###### Propiedades y Metodos Comunes

- window.document: Hace referencia al documento cargado en la ventana.
- window.alert(): Muestra una alerta con un mensaje.
- window.setTimeout(): Ejecuta una función después de un retraso especificado.
- window.setInterval(): Ejecuta una función repetidamente con un intervalo de tiempo especificado.

#### Document

Representa el documento HTML o XML cargado en la ventana. Proporciona métodos y propiedades para acceder y manipular el contenido y la estructura del documento.

###### Propiedades y Metodos Comunes

- document.getElementById(): Selecciona un elemento por su ID.
- document.getElementsByClassName(): Selecciona elementos por su clase.
- document.getElementsByTagName(): Selecciona elementos por su etiqueta.
- document.querySelector(): Selecciona el primer elemento que coincide con un selector CSS.
- document.querySelectorAll(): Selecciona todos los elementos que coinciden con un selector CSS.
- document.createElement(): Crea un nuevo elemento

#### Element

Representa un elemento en el documento HTML. Todos los nodos de elementos son instancias del tipo Element.

###### Propiedades y Metodos Comunes

- element.innerHTML: Obtiene o establece el HTML interno del elemento.
- element.textContent: Obtiene o establece el texto del elemento.
- element.setAttribute(): Establece un atributo en el elemento.
- element.getAttribute(): Obtiene el valor de un atributo del elemento.
- element.removeAttribute(): Elimina un atributo del elemento.
- element.classList: Proporciona métodos para manipular las clases del elemento (add, remove, toggle, contains).
- element.appendChild(): Añade un nodo como el último hijo de un nodo padre.
- element.removeChild(): Elimina un nodo hijo

#### Node

Es una interfaz base de la cual Element, Text, Comment y otros objetos heredan. Representa un solo nodo en el árbol DOM.

###### Propiedades y Metodos Comunes

- node.parentNode: Hace referencia al nodo padre.
- node.childNodes: Devuelve una colección de los nodos hijos.
- node.firstChild: Hace referencia al primer nodo hijo.
- node.lastChild: Hace referencia al último nodo hijo.
- node.nextSibling: Hace referencia al siguiente nodo hermano.
- node.previousSibling: Hace referencia al nodo hermano anterior.
- node.appendChild(): Añade un nodo al final de la lista de hijos.
- node.removeChild(): Elimina un nodo hijo.

#### Event

Representa cualquier evento que pueda ocurrir en la interfaz del navegador, como clics del ratón, pulsaciones de teclas o eventos de carga.

###### Propiedades y Metodos Comunes

- event.type: El tipo de evento (por ejemplo, click, keyup).
- event.target: El elemento que originó el evento.
- event.preventDefault(): Cancela el comportamiento predeterminado del evento.
- event.stopPropagation(): Evita que el evento se propague a los elementos padres.

### Ejemplos de manipular el DOM

##### Cambiar el contenido de un parrafo

```javascript
let parrafo = document.querySelector('p');
parrafo.textContent = 'Contenido actualizado desde la consola';
```

