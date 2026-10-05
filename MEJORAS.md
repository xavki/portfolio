# Mejoras del portfolio

Rama: `feat/portfolio-mejoras`. Se conserva el diseño base, incluida la paleta, tipografías, stickers y numeración. Un commit por bloque A–F, además de un commit inicial para guardar los cambios anteriores y este informe. No se ha hecho push.

## Resultado por punto

| Punto | Estado | Resultado o motivo |
|---|---|---|
| 1 | Hecho | GymFlow, Atlas, FocusFlow y X-O Agenda, en ese orden, con repositorios concretos. TravelBudgetPlanner no tenía URL pública proporcionada. |
| 2 | Hecho | IDs semánticos y todos los enlaces de habilidades actualizados; frontend, backend y bases de datos enlazan a FocusFlow. |
| 3 | Hecho | Añadidos Flutter, Next.js y Firebase. |
| 4 | Hecho | Dos columnas en escritorio, una en móvil y tarjeta final a ancho completo. |
| 5 | Hecho | Cuarto arte azul grisáceo y símbolo de calendario; estilos en content.css. |
| 6 | Hecho | Introducción actualizada a cuatro proyectos y sus áreas. |
| 7 | Hecho | Soporte para «Ver demo ↗» y «Google Play ↗»; botones ocultos mientras las URL estén vacías. Sin emoji de globo. |
| 8 | Saltado | No se proporcionaron capturas de proyectos. Se mantiene el arte abstracto y se admite image con src, alt, width y height. |
| 9 | Hecho | Tres detalles técnicos por proyecto y etiqueta «Proyecto en equipo · DAM» en X-O Agenda. |
| 10 | Hecho | Desarrollo, hardware y Domino’s, con el último puesto compacto y sin lista. |
| 11 | Saltado | No se proporcionaron empresa, tecnologías ni logros nuevos del puesto. Conservados los datos existentes del CV. |
| 12 | Hecho | Eliminados los br de row-between y ajustada su disposición con CSS. |
| 13 | Saltado | No se proporcionaron centro y fecha del curso de IA. Se conserva «En curso». |
| 14 | Hecho | Se mantiene el nivel confirmado del CV: B1, en progreso. Sin certificado ni objetivo inventados. |
| 15 | Hecho | Sobre mí queda en dos párrafos sobre cómo trabaja y qué equipo busca. |
| 16 | Hecho | GitHub y LinkedIn en hero y contacto, con SVG inline y etiquetas accesibles. |
| 17 | Hecho | WebP de 840 × 1000, JPG optimizado de respaldo y JPG social de 1200 × 630 sin recortar el rostro. |
| 18 | Hecho | CV español sin espacio en el nombre; enlace y README actualizados. |
| 19 | Hecho | Eliminados estilos antiguos, archivos de src y configuración Vite tras buscar referencias. README actualizado con el modelo de proyectos. |
| 20 | Hecho | Banderas española y británica como SVG locales. |
| 21 | Hecho | Canonical y og:url coinciden con https://xavki.github.io/portfolio/, comprobada con respuesta HTTP 200. |
| 22 | Hecho | JSON-LD Person con nombre, puesto, ubicación, perfiles y conocimientos. |
| 23 | Hecho | orbit-label oculta a 480 px o menos. |
| 24 | Hecho | Franja de disciplinas en cuadrícula 2 × 2 a 480 px o menos. |
| 25 | Hecho | Elementos de habilidades como chips con flex-wrap en móvil. |
| 26 | Hecho | Todas las ampliaciones de estilos están en css/content.css; css/redesign.css conserva exactamente el contenido inicial. |

## Verificación

El sitio se sirvió con `python -m http.server 5500` y se comprobó en Chrome mediante Playwright a 375 × 900 y 1366 × 900:

- Sin scroll horizontal: scrollWidth coincide con el ancho del viewport en ambos tamaños.
- Sin errores de consola, JavaScript, solicitudes fallidas o respuestas HTTP de error durante la carga.
- Todas las imágenes cargadas: retrato WebP y tres banderas locales.
- Cuatro IDs de proyecto correctos y ninguna ancla interna rota.
- Una columna de proyectos en móvil y dos en escritorio.
- Sobre mí antes de Proyectos.
- Menú móvil abre y se cierra al seleccionar una sección.
- Franja móvil con dos columnas y cuatro elementos visibles.
- JavaScript y JSON-LD válidos; git diff --check sin errores.

Las seis capturas y verificacion.json se guardaron fuera del sitio, en la carpeta de artefactos de este chat, bajo portfolio-mejoras. Son capturas de secciones: se ocultó la cabecera fija únicamente durante su captura para evitar que se superpusiera al contenido. No se cambió esa cabecera en el sitio.

## Peso de las imágenes

| Archivo | Bytes | Tamaño aproximado |
|---|---:|---:|
| Foto original | 2.547.639 | 2,55 MB |
| Retrato WebP | 78.920 | 79 KB |
| JPG de respaldo | 119.013 | 119 KB |
| JPG para redes | 50.786 | 51 KB |

La imagen principal pesa un 96,9 % menos. Se corrigió la orientación EXIF y se ajustó el retrato antes de exportar.

## Fuentes y diferencias detectadas

Se consultaron con curl los README, árboles y archivos de los repositorios en api.github.com y raw.githubusercontent.com:

- [GymFlow: dependencias](https://github.com/xavki/App-de-gym/blob/master/app/build.gradle), [mapa muscular](https://github.com/xavki/App-de-gym/blob/master/app/src/main/java/com/gymflow/MuscleMapScreen.kt), [progreso](https://github.com/xavki/App-de-gym/blob/master/app/src/main/java/com/gymflow/ExerciseProgressScreen.kt) y [guardado local](https://github.com/xavki/App-de-gym/blob/master/app/src/main/java/com/gymflow/DataManager.kt).
- [Atlas: README](https://github.com/xavki/Atlas/blob/main/README.md), con estructura de canales, memoria y proveedores de modelos de lenguaje.
- [FocusFlow: README](https://github.com/xavki/focusflow/blob/main/README.md), [dependencias web](https://github.com/xavki/focusflow/blob/main/web/package.json), [dependencias móviles](https://github.com/xavki/focusflow/blob/main/mobile/pubspec.yaml), [Supabase](https://github.com/xavki/focusflow/blob/main/web/src/lib/supabase.ts) y [planificación con IA](https://github.com/xavki/focusflow/blob/main/web/src/app/api/plan/route.ts).
- [X-O Agenda: README](https://github.com/xavki/X-O-Agenda/blob/main/README.md), [dependencias](https://github.com/xavki/X-O-Agenda/blob/main/app/build.gradle) y [recordatorios](https://github.com/xavki/X-O-Agenda/blob/main/app/src/main/java/com/institutmarianao/xo_agenda/ReminderReceiver.kt). GitHub identifica el repositorio como fork de joam6/X-O-Agenda.

El README de FocusFlow menciona OpenAI y Claude, pero la ruta revisada usa Claude y package.json declara el SDK de Anthropic. Se muestra Claude API en la tarjeta; falta confirmar una implementación de OpenAI.

GymFlow declara Room como dependencia, pero DataManager guarda rutinas con SharedPreferences y Gson. La tarjeta describe el guardado comprobado y no atribuye a Room una arquitectura offline-first que no se ha verificado. La habilidad Room, suministrada por el usuario, se mantiene; conviene precisar en qué proyecto o módulo se usa.

## Pendiente por parte del propietario

- Nombre de empresa o confirmación de Prácticas FCT, tecnologías y 1–2 logros concretos del puesto de desarrollo.
- Centro y fecha de inicio del curso de IA.
- Certificado u objetivo de inglés, si procede; el nivel actual permanece en B1.
- Hacer público TravelBudgetPlanner y facilitar su URL para sustituir X-O Agenda.
- URL de Google Play de GymFlow, demo de FocusFlow y vídeo de Atlas, si existen.
- Capturas reales de las aplicaciones. Las seis capturas del portfolio ya están realizadas.
- Crear un README para App-de-gym con instalación, funciones, arquitectura y capturas.
- Ajustar el README de FocusFlow a la implementación de proveedores de IA y documentar mejor la parte móvil.
- Precisar el uso de Room y la implementación offline-first.
- Fijar en el perfil de GitHub GymFlow, Atlas, FocusFlow y el portfolio; TravelBudgetPlanner cuando sea público.

La carpeta .claude ya estaba presente y no se ha modificado ni incluido en los commits.
