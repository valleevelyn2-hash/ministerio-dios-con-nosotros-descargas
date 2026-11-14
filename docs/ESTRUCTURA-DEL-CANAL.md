# Estructura del canal público

Este repositorio es el canal de distribución, no el proyecto Android.

## Archivos actuales

- `README.md`: presentación y estado general.
- `manifest.json`: datos de consulta de actualizaciones.
- `history.json`: historial estructurado acumulativo.
- `CHANGELOG.md`: resumen legible de cambios.
- `docs/`: documentación de formato, publicación y seguridad.

## Archivos previstos cuando haya una versión aprobada

- APK final firmada, alojada en una ubicación pública HTTPS estable.
- Hash SHA-256 calculado sobre esa APK.
- Entrada de versión en `manifest.json`, `history.json` y `CHANGELOG.md`.

## Qué no se copia aquí

No se copia el proyecto fuente completo, archivos de firma, secretos, tokens, bases de datos privadas ni información de miembros. Esos elementos deben permanecer protegidos en el repositorio privado y en respaldos seguros.
