# Flujo de colaboración: Claude Code + Codex

Este repositorio es el punto compartido del **código**. No fusiona las memorias de los modelos ni los hace colaborar por el simple hecho de conectarlos a GitHub.

## Flujo propuesto

1. Una mejora se define con objetivo, alcance, criterios de aceptación y páginas afectadas.
2. Claude Code prepara el cambio en una rama separada y crea un pull request.
3. Las pruebas automáticas disponibles se ejecutan antes de revisar.
4. Codex revisa el PR con el contexto de `AGENTS.md` (automáticamente **solo si está habilitada la opción de revisión**).
5. Claude Code corrige los hallazgos relevantes, actualiza el PR y solicita nueva revisión si procede.
6. El propietario revisa el resultado visual/funcional y aprueba la fusión.
7. El despliegue al WordPress de pruebas y después a producción se realiza **solo tras autorización**, con copia de seguridad y plan de reversión.

## Activación pendiente en las cuentas

### Claude Code
- Dar a Claude Code acceso explícito a este repositorio en la conexión de GitHub.
- Para responder a menciones/comentarios de PR mediante GitHub Actions, la integración oficial se configura desde Claude Code con `/install-github-app`, siguiendo sus pasos de permisos y secretos.
- Requiere la autorización pertinente y puede generar costes de API. No almacenar claves en archivos del repositorio.

### Codex
- Conectar este repositorio a Codex desde su configuración.
- Habilitar Code Review y, si está disponible, las revisiones automáticas.
- Comprobación inicial: comentar `@codex review` en un PR después de confirmar que la integración está activa.
- `AGENTS.md` proporciona las reglas de revisión.

## Importante: repositorio vs. sitio web

GitHub almacena y revisa código. Los cambios hechos en el editor de WordPress no se sincronizan aquí de forma automática.
Antes de programar, definir qué componentes propios se versionan: tema hijo, plugin específico o estilos/scripts personalizados.
No versionar por defecto toda la instalación, la base de datos ni los archivos subidos por clientes.

## Seguridad
- El repositorio debe mantenerse **privado** antes de incorporar código propio o documentación interna.
- Nunca introducir contraseñas, tokens, claves ni datos de clientes en prompts, issues o PR.
- Revisión humana obligatoria antes de cualquier despliegue a producción.
