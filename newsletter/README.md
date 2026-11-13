# Newsletter Singular Campers — implementación preparada (NO desplegada)

**Estado, 13/11/2026:** HTML/CSS de la sección preparado en este PR, sin modificar la web publicada. Falta conectar una cuenta de Brevo y generar su formulario real de suscripción, probarlo en borrador/staging y obtener aprobación de David antes de publicar.

## Diseño y ubicación
- Sistema de diseño oficial **Estudio** (marca.md): fondos lino/arena, tipografías Lato y Heebo, botones tinta rectangulares, sin verde de la paleta antigua.
- Home ID 263264 (URL /): insertar el contenido de `section-estudio.html` **antes del `</main>` que sigue al formulario de presupuesto**, manteniendo el CTA prioritario “Pide tu presupuesto a medida”. La Home es un bloque HTML de gran tamaño bajo `#sc-estudio`; usar borrador duplicado de la página, no sobreescribir el contenido entero de producción. No modificar la portada, H1, URLs ni los precios.
- Blog: reutilizar la misma sección en un GeneratePress Element de tipo Hook, ubicación posterior al contenido del artículo, condiciones de visualización solo para entradas del blog. No usar popups, no interferir con contenidos SEO existentes.
- Pie de página: versión compacta únicamente tras probar el módulo en Home y Blog; evitar colocar el mismo formulario varias veces en una sola vista.

## Pasos de integración pendientes
1. Crear o conectar **Brevo** (cuenta bajo control de Singular Campers). Usar dominio de envío autenticado y dirección corporativa. No pedir claves por el chat.
2. Crear lista **Newsletter Singular Campers** separada de los contactos de presupuestos y de los clientes: nadie entra automáticamente por solicitar información.
3. Configurar formulario incrustado real de Brevo con email obligatorio, consentimiento de marketing sin marcar por defecto, enlace a política de privacidad y **doble confirmación (double opt-in)**. Añadir protección contra spam.
4. Sustituir el comentario `SLOT BREVO` por el código oficial del formulario. Antes de publicar probar alta, confirmación, registro de consentimiento, correo de bienvenida, mensaje de error, desuscripción y entrega en móvil/escritorio.
5. Revisar la política de privacidad para informar correctamente del tratamiento, plataforma usada y derechos. No dar por válida la mera presencia del enlace.
6. Enviar solo **una edición al mes** al empezar. Se propone un resumen del blog y proyectos realizados, sin envíos sin consentimiento. Probar el primer correo antes de automatizar.

## Criterios de aceptación
- Suscripción funcional y verificada mediante doble opt-in; 0 contactos creados sin consentimiento.
- La Home mantiene el CTA de presupuestos como principal; el formulario nuevo es secundario y no bloquea navegación.
- Vista móvil accesible, sin ventanas emergentes y sin cambios relevantes de rendimiento.
- Política de privacidad revisada; el correo de bienvenida incluye baja y dirección de contacto.
- No publicar la sección si la cuenta Brevo y su formulario todavía no están conectados.
- No modificar producción sin la aprobación explícita de David tras comprobar el borrador.

El conector WPVibe agotó el límite diario en esta sesión; no hay cambios en WordPress por este PR. (ChatGPT)
