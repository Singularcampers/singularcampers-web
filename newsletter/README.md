# Newsletter Singular Campers — implementación preparada (NO desplegada)

**Estado, 13/11/2026:** Brevo creado por David y enlace de formulario facilitado. Integrado en el HTML/CSS con iframe responsive y enlace alternativo. Borrador WordPress creado: **ID 263792**, estado **draft**, plantilla `elementor_canvas`, título «Newsletter Singular Campers — Estudio (vista previa)». No se ha modificado ninguna página pública; continúa pendiente validación jurídica y funcional y aprobación final.

## Diseño y ubicación
- Sistema de diseño oficial **Estudio** (marca.md): fondos lino/arena, tipografías Lato y Heebo, botones tinta rectangulares, sin verde de la paleta antigua.
- Home ID 263264 (URL /): insertar el contenido de `section-estudio.html` **antes del `</main>` que sigue al formulario de presupuesto**, manteniendo el CTA prioritario “Pide tu presupuesto a medida”. La Home es un bloque HTML de gran tamaño bajo `#sc-estudio`; usar borrador duplicado de la página, no sobreescribir el contenido entero de producción. No modificar la portada, H1, URLs ni los precios.
- Blog: reutilizar la misma sección en un GeneratePress Element de tipo Hook, ubicación posterior al contenido del artículo, condiciones de visualización solo para entradas del blog. No usar popups, no interferir con contenidos SEO existentes.
- Pie de página: versión compacta únicamente tras probar el módulo en Home y Blog; evitar colocar el mismo formulario varias veces en una sola vista.

## Pasos de integración pendientes
1. Cuenta **Brevo** creada por David. **Pendiente** comprobar autenticación del dominio remitente, lista de suscriptores y dirección corporativa; no pedir claves por el chat.
2. Crear lista **Newsletter Singular Campers** separada de los contactos de presupuestos y de los clientes: nadie entra automáticamente por solicitar información.
3. Enlace de formulario Brevo recibido y verificado: el HTML actual muestra email y botón «SUSCRIBIRSE», pero **no muestra casilla separada de consentimiento ni enlace a privacidad**. El doble opt-in no es comprobable desde el HTML público. **Pendiente** informar a Brevo del tratamiento y revisar el consentimiento/registro y opt-in, incluyendo protección contra spam.
4. **Hecho:** sustitución del espacio de formulario por el enlace público de Brevo en un `<iframe>` responsive, con fallback. El diseño interior del iframe depende de Brevo y mantiene colores/estilos por defecto, así que **pendiente** cambiar su aspecto desde la cuenta Brevo a paleta Estudio. Antes de publicar probar alta, confirmación, registro de consentimiento, correo de bienvenida, mensaje de error, desuscripción y entrega en móvil/escritorio.
5. **Verificado:** la política de privacidad publicada (página ID 644) no contiene menciones a `Brevo`, `newsletter` ni «comunicaciones comerciales». **Pendiente** adecuarla para informar correctamente del tratamiento, plataforma usada, derechos, posibles transferencias y plazos de conservación. No dar por válida la mera presencia del enlace.
6. Enviar solo **una edición al mes** al empezar. Se propone un resumen del blog y proyectos realizados, sin envíos sin consentimiento. Probar el primer correo antes de automatizar.

## Criterios de aceptación
- Suscripción funcional y verificada mediante doble opt-in; 0 contactos creados sin consentimiento.
- La Home mantiene el CTA de presupuestos como principal; el formulario nuevo es secundario y no bloquea navegación.
- Vista móvil accesible, sin ventanas emergentes y sin cambios relevantes de rendimiento.
- Política de privacidad revisada; el correo de bienvenida incluye baja y dirección de contacto.
- No publicar la sección si la cuenta Brevo y su formulario todavía no están conectados.
- No modificar producción sin la aprobación explícita de David tras comprobar el borrador.

El conector WPVibe volvió a permitir operaciones y se creó un **borrador independiente de WordPress, ID 263792**. Se corrigió el `&` de una URL de tipografías a `&amp;` tras advertencia de validación Gutenberg. Se ha verificado con WP-CLI que el borrador contiene el iframe y mantiene `post_status=draft`. La vista previa requiere sesión de WordPress y no se ha podido validar la interacción de alta ni móvil. **La web pública no cambia.** (ChatGPT)
