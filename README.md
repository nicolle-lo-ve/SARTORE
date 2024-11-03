# Informe sobre el código HTML y CSS de "SARTORE"

A continuación, se analizarán las diferentes secciones del código, su estructura y estilo.

## Estructura del HTML

Aquí se describen sus componentes principales:

- **Declaración del Doctype**: 
  Se inicia con `<!DOCTYPE html>`, lo que indica que se trata de un documento HTML5.
- **Elemento `<html>`**:
  El atributo `lang="es"` especifica que el contenido está en español.
- **Elemento `<head>`**:
  - **Metaetiquetas**:
    Se incluyen metaetiquetas para la codificación de caracteres (UTF-8) y para la configuración del viewport, lo cual es esencial para la responsividad en dispositivos móviles.
  - **Título**:
    El título de la página se establece como "Mi Local - Inicio".
  - **Enlaces a estilos**:
    Se vincula a un archivo CSS externo (`styles.css`) y se incluyen enlaces para fuentes desde Google Fonts.
- **Elemento `<body>`**:
  - **Encabezado (`<header>`)**:
    Contiene el logo y la navegación principal. Utiliza un sistema de flexbox para organizar los elementos.
    ```
    <header class="main-header">
    <div class="header-wrap">
        <div class="wrap-logo-header">
            <a class="logo-header">
                SARTORE
            </a>
        </div>
        <div class="wrap-nav-header">
            <nav class="nav-header">
                <ul class="main-menu">
                    <li class="menu-item"><a href="index.html">Inicio</a></li>
                    <li class="menu-item"><a href="conocenos.html">Conócenos</a></li>
                    <li class="menu-item"><a href="tienda.html">Tienda</a></li>
                    <li id="nav-main-contact" class="menu-item"><a href="contacto.html">Contacto</a></li>
                </ul>
            </nav>
        </div>
    </div>
    </header> 
  ´´´
  - **Sección principal (`<main>`)**: Presenta un título, una galería de imágenes y un párrafo descriptivo sobre las pizzas.
  - **Pie de página (`<footer>`)**: Incluye derechos de autor.

## Estilos CSS

El CSS proporciona un diseño visual atractivo y funcional. A continuación, se describen algunas características clave:

- **Estilo del encabezado**:
  - El encabezado está fijo en la parte superior con un fondo de color `#e39c03`, asegurando que siempre sea visible mientras se navega por la página.
  - Utiliza flexbox para distribuir el espacio entre el logo y los elementos de navegación.
  
- **Menú de navegación**:
  - Los elementos del menú están dispuestos horizontalmente sin puntos de lista, con márgenes entre ellos para mejorar la legibilidad.
  
- **Cuerpo y fondo**:
  - Se establece una imagen de fondo que cubre todo el viewport, lo que le da un aspecto visual atractivo a la página.
  - La fuente utilizada es 'Amatic SC', lo que aporta un toque amigable y moderno.
  
- **Sección principal**:
  - La sección principal tiene un fondo blanco semitransparente, bordes redondeados y una sombra suave, lo que ayuda a destacar el contenido sobre el fondo.
  - Los textos están centrados, lo que mejora la presentación visual.
  
- **Galería de imágenes**:
  - Las imágenes están organizadas en una galería flexible, cada una ocupando el 30% del ancho disponible, con bordes redondeados.
  
- **Pie de página**:
  - Fijo en la parte inferior, asegurando que siempre esté visible. Utiliza texto blanco para contrastar con el fondo.

## Conclusiones

El código HTML y CSS proporcionado muestra una buena práctica en el desarrollo web. La estructura es clara y organizada, facilitando tanto la lectura como el mantenimiento. El uso de flexbox en el diseño asegura que los elementos se ajusten adecuadamente en diferentes tamaños de pantalla. Además, la elección de colores y fuentes contribuye a una experiencia visual agradable para los usuarios.

Este enfoque no solo mejora la estética, sino que también es funcional, permitiendo a los visitantes navegar fácilmente por las diferentes secciones del sitio. En general, este código es un buen ejemplo de cómo construir una página web moderna y responsiva.
