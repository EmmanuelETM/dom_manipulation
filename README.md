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

Para dar un ejemplo de la estructura del DOM, miremos este codigo:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Mi Página</title>
  </head>
  <body>
    <h1 id="titulo">Hola Mundo</h1>
    <p class="parrafo">Este es un párrafo.</p>
    <a href="https://www.ejemplo.com">Visita Ejemplo</a>
  </body>
</html>
```
