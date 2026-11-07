# Singular Campers · web

Instrucciones para cualquier agente (Codex, Claude Code) que trabaje en este repositorio.

## Negocio
- Singular Campers: camperización de furgonetas a medida de gama alta e instalaciones sueltas (litio Victron, solar, calefacción estacionaria, agua, gas GLP, homologación ITV).
- Taller en Olesa de Montserrat (Barcelona), a 30 minutos de Barcelona.
- Web: https://singularcampers.com
- Objetivo SEO: posicionar en el top 3 para búsquedas de Barcelona y Cataluña («camperización de furgonetas Barcelona», «camperizar furgoneta Barcelona», «empresa camperización Barcelona»). La home NO debe posicionarse por «Olesa de Montserrat»: esa intención la cubre /donde-estamos/.

## Stack
- WordPress + GeneratePress + GenerateBlocks Pro, WP Rocket, Yoast SEO. Hosting Webempresa.
- La home (página ID 263264) usa la plantilla «Elementor Canvas» y su contenido son bloques `wp:html` y `generateblocks/*`. La migración de Elementor a GenerateBlocks está a medias.
- Este repositorio NO está conectado a WordPress: guarda copias del código. Los cambios se aplican en WordPress a mano o con autorización expresa.

## Reglas
- No publicar nada en producción sin autorización explícita de David.
- No cambiar URLs ni eliminar contenido indexado sin análisis previo.
- No cambiar la estructura tecnológica (WordPress / GeneratePress / GenerateBlocks).
- No editar reseñas de clientes.
- Una sola etiqueta H1 por página.
- Olesa de Montserrat solo en la dirección (NAP), la FAQ de ubicación y las indicaciones de cómo llegar. En titulares e introducciones, Barcelona.

## Estilo visual
- Verde salvia #6EBE8C, verde oscuro #2E5A40 / #4E9669, carbón #464A4F, fondo #FAF8F4, texto #15221B.
- Tipografías: Space Grotesk (titulares, mayúsculas), Instrument Serif cursiva (acentos), Plus Jakarta Sans (texto).
- Sin naranja. Fotos y vídeos propios con protagonismo.
- El kit de Elementor sigue cargando y pisa los estilos de h1/h2: usar selectores con especificidad suficiente (ej. `.sc-intro h1.sc-intro__h1`).

## Idioma
- Español en contenido y comunicación.

## Estructura
- `wordpress/home/` · bloques HTML de la página de inicio.
- `docs/` · registro de cambios SEO y prompts de trabajo.
