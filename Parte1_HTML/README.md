# Front End Js - Proyecto "Mundo Peregrino"

## Introducción

Este proyecto es una guía de turismo por el mundo, donde podrás explorar destinos populares, recomendaciones de viajes, y tener acceso a diversas herramientas interactivas como formularios de contacto. El objetivo es desarrollar una web completa y funcional con HTML en su primera etapa, a la cual se añadirán estilos y funcionalidades en etapas posteriores.

---

## Ruta A - Estructura HTML

### Clase N° 1 - Conceptos Básicos de HTML

#### Detalles

Crear una estructura HTML 5 básica que incluya etiquetas esenciales:

- `header`
- `main`
- `nav`
- `footer`

**Dentro del `header`,** deberás incluir una etiqueta `<h1>` con el nombre del proyecto.

### Clase N° 2 - Listas, Rutas, Multimedia y Tablas

#### Parte 1: Lista de navegación, etiquetas `nav`, `ul`, `li`, `a`

En esta parte, construiremos una barra de navegación. La barra debe ser una lista no ordenada con enlaces a las distintas secciones del sitio.

#### Ejemplo de la estructura

```html
<header>
  <nav>
    <ul>
      <li>
        <a href="/" aria-label="Volver al inicio">
          <img src="./assets/home.svg" height="20px" alt="Inicio" /> Inicio
        </a>
      </li>
      <li>
        <a href="/products" aria-label="Explorar productos">
          <img src="./assets/plane.svg" height="20px" alt="Productos" />
          Productos
        </a>
      </li>
      <li>
        <a href="/reviews" aria-label="Ver reseñas">
          <img src="./assets/feedback.svg" height="20px" alt="Reseñas" />
          Reseñas
        </a>
      </li>
      <li>
        <a href="/contact" aria-label="Contactar">
          <img src="./assets/envelope-dot.svg" height="20px" alt="Contacto" />
          Contacto
        </a>
      </li>
    </ul>
  </nav>
</header>
```

### Parte 3: Formularios y Subida al Servidor

#### Parte 1: Formularios y accesibilidad

Construiremos un **formulario** de contacto Dentro del `main`, utilizando las etiquetas `form`, `input` y `textarea`. Además, añadiremos validaciones básicas en HTML5 (`required`, `placeholder`) para mejorar la accesibilidad.

```html
<fieldset>
  <legend>Estamos para escucharte</legend>
  <form action="submit" method="post">
    <label for="name">Nombre: </label>
    <input
      type="text"
      id="name"
      name="name"
      placeholder="Juan Perez"
      required
    /><br /><br />

    <label for="email">Email: </label>
    <input
      type="email"
      id="email"
      name="email"
      placeholder="email@email.com"
      required
    /><br /><br />

    <label for="destination">Destino deseado: </label>
    <input
      type="text"
      id="destination"
      name="destination"
      placeholder="Ej: París"
      required
    /><br /><br />

    <label for="text">Comentario: </label>
    <textarea
      id="text"
      name="text"
      placeholder="Gracias por tu mensaje..."
      required
    ></textarea
    ><br /><br />

    <input type="submit" value="Enviar" />
  </form>
</fieldset>
```

#### Parte 2: Subida a GitHub Pages y Netlify

1. Crear una cuenta en `GitHub` y cargar el proyecto en un repositorio.
2. Configurar `GitHub Pages` para generar un enlace público y compartirlo.
3. Subir el proyecto a `Netlify`, enlazando la cuenta de `GitHub`.

### Extras: Optimización para SEO y accesibilidad

**Meta etiquetas SEO** ayudan a los motores de búsqueda a entender tu página. Estas son algunas que deberías incluir en el `<head>` de tu HTML:

```html
<!-- Descripción de la página que aparece en los motores de búsqueda -->
<meta
  name="description"
  content="Explora el mundo con Mundo Peregrino, tu guía de turismo."
/>

<!-- Palabras clave relacionadas con el contenido de la página para SEO -->
<meta
  name="keywords"
  content="turismo, viajes, destinos, vacaciones, guías de viaje"
/>

<!-- Autor del contenido de la página -->
<meta name="author" content="Mundo Peregrino" />

<!-- Título de la página para la vista previa en redes sociales (Open Graph) -->
<meta property="og:title" content="Mundo Peregrino - Turismo por el Mundo" />

<!-- Descripción de la página para la vista previa en redes sociales (Open Graph) -->
<meta
  property="og:description"
  content="Descubre los destinos más fascinantes y consejos de viaje."
/>

<!-- Imagen que se mostrará en la vista previa en redes sociales (Open Graph) -->
<meta property="og:image" content="./assets/banner.jpg" />

<!-- URL canónica de la página para compartir en redes sociales (Open Graph) -->
<meta property="og:url" content="https://tuweb.com" />

<!-- Tipo de tarjeta que se mostrará en Twitter al compartir el enlace -->
<meta name="twitter:card" content="summary_large_image" />
```

### Ejemplo completo de estructura HTML:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="Explora el mundo con Mundo Peregrino." />
    <meta name="keywords" content="turismo, viajes, destinos, vacaciones" />
    <meta name="author" content="Mundo Peregrino" />
    <title>Mundo Peregrino</title>
  </head>
  <body>
    <header>
      <div>
        <a href="/">
          <img
            src="./assets/undraw_traveling_yhxq.svg"
            height="100px"
            alt="Logo Mundo Peregrino"
          />
          <h1>Mundo Peregrino</h1>
        </a>
      </div>
      <nav>
        <ul>
          <li><a href="/">Inicio</a></li>
          <li><a href="/products">Productos</a></li>
          <li><a href="/reviews">Reseñas</a></li>
          <li><a href="/contact">Contacto</a></li>
        </ul>
      </nav>
    </header>

    <main>
      <section>
        <h2>Caminante son tus huellas el camino y nada más</h2>
        <img
          src="./assets/banner.jpg"
          height="1080px"
          width="1920px"
          alt="Banner Mundo Peregrino"
        />
        <h3>
          El invierno es fabuloso, no dejes de conocerlo en otras partes del
          mundo
        </h3>
        <iframe
          width="800"
          height="600"
          src="https://www.youtube.com/embed/SDzl9uB7j0s"
          title="Snowfall Winter"
          allowfullscreen
        ></iframe>
      </section>
      <aside>
        <h4>Promociones de temporada</h4>
        <ul>
          <li>Descuento 20% en vuelos a Europa</li>
          <li>Hoteles con tarifa especial en América Latina</li>
        </ul>
      </aside>

      <h4>Consultas y Sugerencias</h4>
      <fieldset>
        <legend>Estamos para escucharte</legend>
        <form action="submit" method="post">
          <label for="name">Nombre:</label>
          <input type="text" id="name" name="name" required /><br /><br />
          <label for="email">Email:</label>
          <input type="email" id="email" name="email" required /><br /><br />
          <label for="destination">Destino deseado:</label>
          <input
            type="text"
            id="destination"
            name="destination"
            required
          /><br /><br />
          <textarea
            id="text"
            name="text"
            placeholder="Gracias por tu mensaje..."
            required
          ></textarea
          ><br /><br />
          <input type="submit" value="Enviar" />
        </form>
      </fieldset>
    </main>

    <footer>
      <ul>
        <li><a href="/terms">Términos y condiciones</a></li>
        <li><a href="/about">Sobre nosotros</a></li>
      </ul>
    </footer>
  </body>
</html>
```

## Felicitaciones, llegaste al final de la Ruta A HTML!

### Con lo aprendido, estarás en condiciones de:

- Crear una estructura semántica completa.
- Añadir imágenes, videos y formularios.
- Optimizar el sitio para SEO básico.

## Próximos pasos:

#### Ahora que tienes el esqueleto funcional, es hora de comenzar con CSS para darle estilo y un diseño atractivo a tu página.

## Puedes ver el resultado final en cualquiera de estas 2 direcciones

- https://daroponce21.github.io/FrontEnd-Js-Curso/Parte1_HTML/index.html

- https://mundoperegrino.netlify.app/parte1_html/
