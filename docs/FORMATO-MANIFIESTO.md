# Formato del manifiesto de actualizaciones

La aplicación consultará el archivo `manifest.json` de este repositorio.

## Campos principales

- `appName`: nombre visible de la aplicación.
- `packageName`: identificador Android; debe coincidir exactamente con el APK instalado.
- `latestVersion` y `latestVersionCode`: última versión publicada y su código.
- `updateAvailable`: solo debe ser `true` cuando exista una APK pública, válida y verificada.
- `releaseStatus`: estado de publicación.
- `downloadUrl`: enlace HTTPS directo al APK publicado; permanece `null` mientras no haya descarga.
- `sha256`: hash SHA-256 del APK publicado; permanece `null` hasta calcularlo sobre el archivo final.
- `signingCertificateSha256`: huella SHA-256 del certificado de firma esperado.
- `minimumSupportedVersionCode`: versión mínima que el canal declara compatible.
- `plannedNextVersion`: información de planificación; no representa una versión publicada.

## Reglas

1. No activar una actualización antes de subir el APK definitivo.
2. Calcular SHA-256 después de generar el APK firmado.
3. Verificar el certificado de firma con herramientas Android.
4. Comprobar que el paquete sea `com.ministeriodiosconnosotros.beta`.
5. Confirmar que el versionCode sea mayor que el de la instalación anterior.
6. Mantener HTTPS y no incluir credenciales en el manifiesto.
7. La instalación final siempre queda sujeta a la confirmación del usuario en Android.
