# Instrucciones para agentes de IA — Singular Campers

## Objetivo
Mantener y mejorar el código **propio** de singularcampers.com (WordPress). Priorizar captación de solicitudes cualificadas, SEO local, legibilidad, rendimiento, accesibilidad y experiencia móvil.

## Contexto
- Sitio público: https://singularcampers.com
- WordPress con GeneratePress + GenerateBlocks. Comprobar versiones y configuración reales antes de modificar código.
- Identidad visual: verde grisáceo RAL 7033, fotografía real como protagonista, diseño sobrio.
- Evitar cambios visuales innecesarios, dependencias comerciales o tipografías de pago.
- El repositorio **no** es una copia verificada de producción. No asumir que un cambio en GitHub se publique en WordPress.

## Restricciones obligatorias
- No publicar, desplegar ni modificar la web en producción sin una autorización explícita y pruebas previas.
- No subir a Git: credenciales, claves API, `.env`, `wp-config.php`, backups, bases de datos, datos de clientes o archivos subidos por usuarios.
- No instalar un segundo plugin SEO principal ni reemplazar herramientas existentes sin analizar compatibilidad y migración.
- No introducir afirmaciones comerciales sin verificar (reseñas, certificaciones, homologaciones o servicios).
- No eliminar estilos o funcionalidades existentes salvo que sea necesario para el cambio solicitado.
- Preferir código acotado, reversible, documentado y compatible con WordPress.

## Criterios de aceptación
- Probar escritorio y móvil, especialmente contraste, CTA, navegación, galerías, servicios y formularios.
- Preservar URLs, títulos SEO, metadatos, enlazado interno, canonical, schema y redirecciones salvo cambio expresamente aprobado.
- Documentar archivos afectados, comportamiento anterior/nuevo y pasos para revertir.
- Si hay un área privada de clientes, verificar aislamiento por usuario, permisos, autenticación y protección de datos personales.

## Code Review Rules

### Privacidad y seguridad de WordPress
- Marcar como hallazgo importante cualquier exposición de datos de clientes, credenciales o controles de acceso incorrectos.
- Comprobar capacidades, nonces cuando correspondan y sanitización/escape correctos en entradas y salidas de WordPress.
- No permitir que un cliente consulte documentos, presupuestos, fotografías o expedientes de otro cliente.

### Compatibilidad y regresiones
- Marcar cambios que rompan GeneratePress, GenerateBlocks, estructura de plantillas, formularios o funcionalidades que ya funcionan.
- Marcar regresiones en responsive móvil, contraste de títulos, menús y CTA cuando exista evidencia en el diff.

### SEO y contenidos
- Marcar noindex accidental, pérdida de canonicals, enlaces rotos introducidos por el cambio o duplicación de marcado SEO.
- No confundir puntuaciones de plugins con una mejora demostrada del posicionamiento.

### Producción
- Marcar cualquier workflow o código que publique automáticamente en producción sin un control humano explícito.
