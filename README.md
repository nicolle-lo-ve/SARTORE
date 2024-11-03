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
  - **Sección principal (`<main>`)**:
    Presenta un título, una galería de imágenes y un párrafo descriptivo sobre las pizzas.
    ```
    <main class="main-section">
            <h2>¿Alguna vez vieron la perfección en persona?</h2>
            <div class="image-gallery">
                <div class="image-item image-item-1"></div>
                <div class="image-item image-item-2"></div>
                <div class="image-item image-item-3"></div>
            </div>
            <p>Cada una de nuestras pizzas es diferente pero increíble a su manera. La combinación de ingredientes es, sencillamente, perfecta.</p>
        </main>
  - **Pie de página (`<footer>`)**:
    Incluye derechos de autor.
    ```
    <footer class="footer">
            <p>© 2024 SARTORE. Todos los derechos reservados.</p>
    </footer>

## Estilos CSS

El CSS proporciona un diseño visual atractivo y funcional. A continuación, se describen algunas características clave:

- **Estilo del encabezado**:
  - El encabezado está fijo en la parte superior con un fondo de color `#e39c03`, asegurando que siempre sea visible mientras se navega por la página.
  - Utiliza flexbox para distribuir el espacio entre el logo y los elementos de navegación.
    ```
    header.main-header {
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 9999;
      background-color: #e39c03;
    }

    .wrap-logo-header {
      display: flex;              /* Utiliza Flexbox para centrar el contenido */
      justify-content: left;    /* Centra horizontalmente */
      width: 100%;               /* Asegura que ocupe el 100% del ancho del contenedor */
    }

    .logo-header {
      font-size: 4.5rem;         /* Aumenta el tamaño de la fuente */
      color: #fff;               /* Cambia el color del texto si es necesario */
      text-align: left;        /* Centra el texto dentro de su contenedor */
      margin: 0.2rem;                 /* Elimina el margen para mantener el logo centrado */
      display: inline-block;      /* Cambia a inline-block para centrarse correctamente */
    }

    .header-wrap {
      display: flex;
      justify-content: space-between;
      padding: 1rem;
      color: #fff;
    }
  
- **Menú de navegación**:
  - Los elementos del menú están dispuestos horizontalmente sin puntos de lista, con márgenes entre ellos para mejorar la legibilidad.
    ```
    .nav-header {
      padding: 1rem; /* Ajusta el padding según sea necesario */
      color: #fff; /* Cambia el color del texto si es necesario */
    }

    .main-menu {
      list-style: none; /* Elimina los puntos de la lista */
      padding: 0; /* Elimina el padding */
      display: flex; /* Usar flexbox para alinear los elementos */
    }

    .menu-item {
      margin-right: 20px; /* Espacio entre los elementos del menú */
    }

    .menu-item a {
      color: #fff; /* Color del texto */
      text-decoration: none; /* Sin subrayado */
      font-size: 2.2rem; /* Tamaño de la fuente */
    }
    
- **Cuerpo y fondo**:
  - Se establece una imagen de fondo que cubre todo el viewport, lo que le da un aspecto visual atractivo a la página.
  - La fuente utilizada es 'Amatic SC', lo que aporta un toque amigable y moderno.
    ```
    body {
      font-family: 'Amatic SC', sans-serif;
      background-image: url('SARTORE-IMAGEN-1.jpg'); /* Cambia por el nombre de tu imagen */
      background-size: cover; /* La imagen cubrirá todo el fondo */
      background-position: center; /* Centra la imagen */
      background-repeat: no-repeat; /* Evita que la imagen se repita */
      height: 100vh; /* Asegúrate de que el body tenga altura completa */
      margin: 0; /* Elimina el margen predeterminado del body */
    }  
  
- **Sección principal**:
  - La sección principal tiene un fondo blanco semitransparente, bordes redondeados y una sombra suave, lo que ayuda a destacar el contenido sobre el fondo.
  - Los textos están centrados, lo que mejora la presentación visual.
     ```
    .main-section {
      position: fixed;
      top: 150px;
      left: 130px;
      padding: 1rem;                /* Añade espacio alrededor del contenido */
      background-color: rgba(255, 255, 255, 0.89); /* Fondo blanco con opacidad */
      border-radius: 10px;         /* Bordes redondeados */
      max-width: 1000px;            /* Ancho máximo de la sección */
      margin: 1rem auto;           /* Centra la sección y añade márgenes superior e inferior */
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2); /* Sombra suave para darle profundidad */
    }

    .main-section h2 {
      font-size: 2.5rem;             /* Aumenta el tamaño de la fuente del encabezado */
      color: #333;                 /* Color oscuro para el texto */
      text-align: center;          /* Centra el texto */
      margin-bottom: 1rem;        /* Espacio debajo del encabezado */
    }

    .main-section p {
      font-size: 1.7rem;           /* Tamaño de fuente del párrafo */
      color: #000000;                 /* Color del texto del párrafo */
      line-height: 1.5;            /* Espaciado entre líneas */
      text-align: center;          /* Centra el texto del párrafo */
    }
     
- **Galería de imágenes**:
  - Las imágenes están organizadas en una galería flexible, cada una ocupando el 30% del ancho disponible, con bordes redondeados.
    ```
    .image-gallery {
      display: flex;                          /* Usar flexbox para alinear las imágenes */
      justify-content: center;                /* Centra las imágenes horizontalmente */
      margin: 2rem 0;                        /* Espacio arriba y abajo de la galería */
    }

    .image-item {
        width: 30%;                             /* Cada imagen ocupa el 30% del ancho */
        height: 200px;                          /* Altura fija para las imágenes */
        margin: 0 10px;                         /* Espacio entre las imágenes */
        border-radius: 10px;                    /* Bordes redondeados en las imágenes */
        background-size: cover;                 /* Cubrir el contenedor */
        background-position: center;            /* Centrar la imagen */
    }

    /* Aplicando las imágenes de fondo */
    .image-item-1 {
        background-image: url('preparacion-1.jpeg');
    }
    
    .image-item-2 {
        background-image: url('preparacion-2.jpeg');
    }
    
    .image-item-3 {
        background-image: url('preparacion-3.jpeg');
    }
    
- **Pie de página**:
  - Fijo en la parte inferior, asegurando que siempre esté visible. Utiliza texto blanco para contrastar con el fondo.
    ```
    .footer {
      position: fixed;                 /* Fija el footer en la parte inferior de la página */
      bottom: 0;                      /* Coloca el footer en la parte inferior */
      left: 2.5rem;                        /* Alinea el footer a la izquierda */
      width: 100%;                    /* Asegúrate de que el footer ocupe todo el ancho */
      color: white;                   /* Color del texto blanco */
      text-align: left;             /* Centra el texto dentro del footer */
      font-size: 1rem;                /* Tamaño de la fuente */
      z-index: 1000;                  /* Asegúrate de que el footer esté sobre otros elementos */
    }
    
## Conclusiones

La estructura es clara y organizada, facilitando tanto la lectura como el mantenimiento. El uso de flexbox en el diseño asegura que los elementos se ajusten adecuadamente en diferentes tamaños de pantalla. Además, la elección de colores y fuentes contribuye a una experiencia visual agradable para los usuarios.

Este enfoque no solo mejora la estética, sino que también es funcional, permitiendo a los visitantes navegar fácilmente por las diferentes secciones del sitio. En general, este código es un buen ejemplo de cómo construir una página web moderna y responsiva.

![image](https://github.com/user-attachments/assets/1bff7dc4-3159-4de0-9e19-134e7380c70d)

