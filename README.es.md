# Proyecto Educativo: Página Web de Disney

**Este sitio web se ha construido únicamente con fines educativos y académicos**, para compartir y evaluar los conocimientos de mis estudiantes en un contexto cercano al profesional. Es una práctica que refuerza las habilidades de HTML y CSS mientras simula flujos de trabajo reales de desarrollo web.

---

## 1. Resumen de la estructura HTML

```html
<!DOCTYPE html>
<html lang="es">
<head>…</head>
<body>
  <nav class="navbar">…</nav>
  <section class="banner">…</section>
  <main>
    <section id="shop">…</section>
    <section id="disney-plus">…</section>
    <section id="movies">…</section>
    <section id="parks-and-travel">…</section>
    <section id="more">…</section>
  </main>
  <footer>…</footer>
</body>
</html>
```

### Etiquetas semánticas clave

- `<!DOCTYPE html>`: Declara HTML5 para un renderizado consistente entre navegadores.
- `<html lang="es">`: Ayuda a los lectores de pantalla y a los motores de búsqueda a identificar el idioma del contenido.
- `<head>`: Contiene los metadatos (codificación de caracteres, configuración del viewport, título de la página, enlaces a hojas de estilo e íconos).
- `<nav>`: Define la sección de navegación principal.
- `<section>`: Organiza agrupaciones temáticas de contenido (banner, tienda, Disney+, películas, parques, ofertas).
- `<article>`: Representa bloques de contenido independientes y reutilizables (tarjetas de la tienda, destacados).
- `<main>`: Indica el área de contenido principal; es única por página.
- `<footer>`: Contiene la navegación secundaria y los avisos legales.

---

## 2. Propiedades CSS esenciales

```css
/* Reset global */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
```

- **`box-sizing: border-box`**: Incluye el padding y el borde dentro del ancho y alto definidos del elemento, lo que simplifica los cálculos del layout.
- **`display: flex`** / **`justify-content`** / **`align-items`**: Crean layouts flexibles de una dimensión (usados en la barra de navegación, el banner y los contenedores de tarjetas).
- **`background-size: cover`**, **`background-position: center`**, **`background-repeat: no-repeat`**: Hacen que las imágenes de fondo cubran por completo su contenedor manteniendo el punto focal.
- **`flex-direction: column`**: Apila los elementos hijos verticalmente.
- **`gap`**, **`margin`**, **`padding`**: Gestionan el espaciado consistente entre elementos y dentro de ellos.
- **Unidades relativas (`%`, `rem`, `vh`)**: Permiten diseños fluidos y escalables en diferentes tamaños de pantalla.

---

## 3. Buenas prácticas y consejos profesionales

1. **Marcado semántico**: Usa siempre las etiquetas HTML apropiadas para mejorar la accesibilidad y el SEO.
2. **Mobile-first y unidades responsivas**: Empieza con los estilos base y ve agregando capas con media queries. Usa `rem` y `%` para espaciados y tipografía escalables.
3. **Arquitectura CSS modular**: Organiza los estilos en archivos lógicos (settings, tools, base, layout, components, utilities). Adopta la convención de nombres BEM (`bloque__elemento--modificador`).
4. **Imágenes optimizadas**: Usa `<picture>` con `srcset` para imágenes responsivas, combinado con `loading="lazy"` para mejorar el rendimiento.
5. **Mejoras de rendimiento**: Minifica los recursos, aprovecha el cache busting y precarga los recursos críticos (por ejemplo, las imágenes del hero).
6. **Accesibilidad (a11y)**: Escribe atributos `alt` descriptivos, asegura estados de foco visibles para el teclado y mantén un contraste de color suficiente.

---

*Este README busca guiar a docentes y estudiantes a través de la estructura y las decisiones de estilo centrales del proyecto, fomentando una comprensión cercana a la profesional del desarrollo web moderno.*

---

## 4. Sugerencias para mejorar profesionalmente tu HTML y CSS

Para refinar tu proyecto usando **solo HTML y CSS**, considera las siguientes buenas prácticas y técnicas modernas:

- **Preprocesadores CSS (Sass/SCSS):** Organiza tus estilos con variables, anidamiento, parciales y mixins para eliminar repetición y mejorar el mantenimiento.
- **Convenciones de nombres:** Adopta una metodología como **BEM** o **SMACSS** para mantener nombres de clases claros, modulares y sin colisiones.
- **CSS Reset o Normalize:** Incluye un reset pequeño (o Normalize.css) al inicio de tu hoja de estilos para asegurar estilos por defecto consistentes entre navegadores.
- **Propiedades personalizadas de CSS:** Usa `--variable` para colores, espaciados y escalas tipográficas. Por ejemplo:
  ```css
  :root {
    --color-primary: #db5243;
    --space-md: 2rem;
  }
  ```
- **Tipografía fluida:** Usa `clamp()` para tamaños de fuente escalables y responsivos:
  ```css
  h1 {
    font-size: clamp(1.5rem, 4vw, 3rem);
  }
  ```
- **Layouts responsivos con Grid y Flexbox:**
  - Usa **CSS Grid** para layouts bidimensionales (por ejemplo, cuadrículas de tarjetas complejas, composiciones de banner).
  - Usa **Flexbox** para flujos unidimensionales (por ejemplo, la barra de navegación, grupos de botones).
  - Combínalos en layouts híbridos: Grid para la estructura principal y Flexbox dentro de los elementos de la cuadrícula.
- **Container Queries (donde sean compatibles):** Limita las media queries al contenedor padre en lugar del viewport para crear componentes verdaderamente modulares y responsivos.
- **Funciones CSS avanzadas:** Explora `min()`, `max()` y `env()` para dimensionamiento dinámico y ajustes de áreas seguras (útil en dispositivos con notch).
- **Transiciones y transformaciones:** Agrega microinteracciones con CSS:
  ```css
  .btn:hover {
    transform: translateY(-2px);
    transition: transform 0.2s ease;
  }
  ```
- **HTML semántico y accesibilidad:** Asegura estilos de foco (`:focus-visible`), texto `alt` significativo y el uso correcto de landmarks (`<header>`, `<main>`, `<footer>`) para mejorar la navegación por teclado y el soporte de lectores de pantalla.
- **Optimización de imágenes en HTML/CSS:**
  - Usa `<picture>` con `srcset` para imágenes adaptativas.
  - Carga diferida de imágenes no críticas: `<img loading="lazy" src="...">`.
  - Aprovecha `background-size: cover` y `background-position: center` para fondos CSS.

<<<<<<< HEAD
Al aplicar estas mejoras centradas en **HTML y 
=======
Al aplicar estas mejoras centradas en **HTML y CSS**, mantendrás un flujo de trabajo ágil, con pocas dependencias, y entregarás un código altamente mantenible y preparado para el futuro.
>>>>>>> a1ce45b47e08c69f1fcd5251a1503932a84baac4
