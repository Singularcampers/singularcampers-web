# Prompt de auditoría SEO para Claude Code

Pégalo en Claude Code (o Codex) con este repositorio abierto. El contexto del negocio y las reglas están en `AGENTS.md`; el registro de cambios en `docs/cambios-seo-2026-11.md`.

```
Eres mi consultor SEO técnico. Audita singularcampers.com y valida los cambios de docs/cambios-seo-2026-11.md. Sigue las reglas de AGENTS.md. Responde en español, claro y conciso.

## Herramientas (por prioridad)
1. Skill Claude SEO: auditoría completa (técnico, on-page, schema, SEO local, Core Web Vitals, GEO).
2. Windsor.ai, si está conectado: datos reales de Search Console, Google Analytics 4 y Google Business Profile.
3. Semrush o Ahrefs, si está conectado: volúmenes locales, SERP, competidores en Barcelona, backlinks, keyword gap y visibilidad en IA.
4. Ubersuggest: solo si no hay Semrush ni Ahrefs (plan gratuito: 3 informes al día).
5. Skill site-audit: nota rápida de SEO, accesibilidad y GEO con informe PDF.
6. Skill impeccable o design-taste-frontend: revisión de diseño antes de publicar cualquier página nueva.
7. Skill deep-research: competencia y contenidos.
Al empezar, dime qué herramientas tienes. Si falta alguna, avisa de qué datos no podrás obtener. No inventes cifras: indica la fuente de cada dato.

## Lo que necesito
1. Auditoría completa de la home y de la web: técnico, on-page, schema, SEO local, Core Web Vitals, GEO / búsqueda con IA (llms.txt, rastreadores IA).
2. Verifica que los 9 cambios publicados están bien en producción (H1 único, schema válido, canonical, móvil).
3. Con Search Console: línea base de impresiones, clics y posición media de la home para consultas con "barcelona", "camperización" y "camperizar".
4. Canibalización: home vs /soluciones-camper/ vs /donde-estamos/ vs páginas de proyecto con "barcelona" en la URL. Keyword principal de cada página.
5. Keywords y SERP para Barcelona: volúmenes, top 10 actual y keyword gap frente a Tinkervan, Cultura Camper y Kangaroo Campers.
6. Google Business Profile: categorías, zona de servicio, reseñas y fotos.
7. Plan para quitar Elementor de la home cambiando la plantilla «Elementor Canvas» sin romper el diseño. Solo el plan.
8. Valorar: página propia para la «Guía interactiva de chasis», menos tarjetas de proyectos en la home y sustituir el iframe de Google Maps.
9. Redactar las páginas «Homologar camper en Barcelona» y «Cuánto cuesta camperizar una furgoneta en Barcelona» (sin precios cerrados), guardándolas en wordpress/paginas/.
10. Revisar el aviso de 3 vulnerabilidades de alto riesgo de WordPress.

## Entregable
- Lista priorizada (impacto/esfuerzo) con el texto o código exacto de cada cambio y la fuente de cada dato.
- Plan SEO de 90 días para ser referencia en camperización en Barcelona y Cataluña, con KPIs medibles en Search Console.
- Antes de aplicar cualquier cambio en la web, enséñamelo y espera mi OK.
```
