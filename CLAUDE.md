# Claude Code — Singular Campers

Lee primero `AGENTS.md`. Sus restricciones también son obligatorias para Claude.

## Forma de trabajo
1. Antes de tocar nada, inspecciona los archivos disponibles y explica el alcance. Nunca des por hecho que este repositorio contiene el código WordPress de producción.
2. Trabaja en una rama `feature/*` o `fix/*`, no en `main`.
3. Haz cambios pequeños con una descripción y pruebas reproducibles.
4. Abre un pull request con capturas del antes/después cuando exista interfaz visual. Déjalo para revisión, sin fusionarlo automáticamente.
5. Solicita revisión de Codex en el pull request cuando esté instalada y habilitada su integración. Atiende los comentarios y vuelve a solicitar revisión.
6. La última aprobación para fusionar o desplegar corresponde a la persona responsable de Singular Campers.

## Orden de prioridades
1. Seguridad y privacidad, especialmente área de clientes.
2. No romper la web publicada.
3. Conversión y captación de clientes de camperizaciones e instalaciones.
4. Rendimiento, experiencia móvil, accesibilidad y SEO.
5. Consistencia visual con la marca.

## Entorno
- Sitio: https://singularcampers.com
- WordPress + GeneratePress + GenerateBlocks.
- No introducir Elementor ni otra capa visual pesada sin petición expresa.
- No instalar fuentes de pago ni dependencias premium sin autorización.
- No dar por terminadas las tareas que requieran acceso al administrador o a producción si solo se modificó GitHub.

## Antes de entregar un PR
Describe objetivo, cambios, pruebas, límites del resultado, riesgos SEO, seguridad, posibilidad de revertir y necesidad de publicación manual.
