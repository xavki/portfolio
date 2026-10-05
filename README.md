# Portfolio de Xavi Martínez

Portfolio estático con HTML, CSS y JavaScript, preparado para GitHub Pages. No necesita compilación ni dependencias de producción.

## Vista local

Desde esta carpeta ejecuta `python -m http.server 5500` y abre `http://localhost:5500`. El workflow de `.github/workflows/deploy.yml` publica el sitio estático en GitHub Pages al actualizar `main`.

## Estructura

- `index.html`: contenido, metadatos y JavaScript.
- `css/redesign.css`: diseño base; las mejoras se añaden en `css/content.css`.
- `public/foto_xavi.webp`: retrato principal, 840 × 1000; `foto_xavi.jpg` es el respaldo optimizado.
- `public/foto_xavi_social.jpg`: imagen de redes, 1200 × 630.
- `public/es.svg`, `gb.svg`, `catalan.svg`: banderas locales.
- `public/CV_FrancescXavier_Martinez_Batlle_ES.pdf` y `CV_FrancescXavier_Martinez_Batlle_EN.pdf`: currículums.

## Proyectos

Edita `FEATURED_PROJECTS` en el último script de `index.html`. Cada entrada admite:

```js
{
  id: 'project-gymflow', // Debe coincidir con los enlaces de Habilidades.
  name: 'GymFlow',
  area: 'Android',
  description: 'Descripción breve basada en el proyecto.',
  stack: ['Kotlin', 'Jetpack Compose'],
  highlights: ['Detalle técnico comprobado en el código.'],
  note: null, // Etiqueta opcional, por ejemplo: Proyecto en equipo · DAM.
  repo: 'https://github.com/xavki/App-de-gym',
  demo: null, // Añadir solo una URL pública verificada.
  store: null, // Solo GymFlow: URL pública de Google Play.
  image: null // O { src: 'public/projects/project-gymflow.webp', alt: 'Descripción de la captura', width: 1200, height: 750 }.
}
```

Los cuatro proyectos actuales son GymFlow, Atlas, AI Project Lab y FocusFlow. La demo de FocusFlow está en https://dayplan-murex.vercel.app (la web se publica con el nombre DayPlan). AI Project Lab aún no tiene repositorio público: con `"repo": null` la tarjeta muestra «Repositorio privado» en lugar del botón; cuando se publique, basta con poner su URL. Si se sustituye un proyecto, actualiza también los enlaces de Habilidades. Las capturas opcionales deben ser WebP de aproximadamente 1200 px y calidad 80; sin captura se mantiene el arte abstracto.

Las descripciones y detalles técnicos se revisaron contra los README y el código de los repositorios. GymFlow declara Room como dependencia, pero el guardado local revisado usa SharedPreferences y Gson; por eso los detalles de su tarjeta describen esa implementación.

## Accesibilidad y mantenimiento

La navegación incluye menú móvil, enlace para saltar al contenido y estados de foco visibles. El sitio respeta la preferencia de movimiento reducido. Las habilidades se agrupan por áreas, con enlaces a proyectos, sin porcentajes de dominio. Los proyectos y las imágenes locales no dependen de la API de GitHub.

La experiencia, formación, idiomas y habilidades coinciden con el CV v4 (`public/CV_*.pdf`): prácticas en Nextt, curso de Udia, SMX, 60 ECTS reconocidos en la UOC e inglés A2. Si cambia el CV, actualiza también estas secciones.
