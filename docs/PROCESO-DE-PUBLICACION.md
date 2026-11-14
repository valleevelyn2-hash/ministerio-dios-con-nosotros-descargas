# Proceso seguro de publicación

Este canal público distribuye únicamente archivos destinados a los usuarios finales. El código fuente y los secretos de compilación permanecen en el repositorio privado.

## Antes de publicar una versión

- [ ] Compilar desde el repositorio privado y registrar el commit de origen.
- [ ] Confirmar nombre de paquete: `com.ministeriodiosconnosotros.beta`.
- [ ] Confirmar versionName y versionCode crecientes.
- [ ] Verificar que la APK esté firmada con el certificado autorizado.
- [ ] Calcular SHA-256 del APK final.
- [ ] Instalar y probar la APK en un dispositivo de prueba.
- [ ] Revisar que las funciones anunciadas realmente funcionen.
- [ ] Publicar el APK en una ubicación HTTPS estable.
- [ ] Actualizar `manifest.json` con el enlace y el hash reales.
- [ ] Agregar una entrada nueva a `history.json` y `CHANGELOG.md`, sin eliminar entradas anteriores.
- [ ] Verificar desde una sesión sin iniciar sesión que los archivos públicos se puedan consultar.

## Nunca publicar

- Contraseñas, tokens, claves privadas o archivos de firma.
- Archivos `.jks`, `.keystore` o sus copias cifradas.
- Secretos de GitHub Actions.
- Datos privados de miembros de la congregación.
- APK que no haya sido probada y verificada.

## Instalación Android

El canal puede facilitar la descarga y abrir el instalador del sistema. Android puede pedir autorización y confirmación al usuario. No se promete ni se intenta una instalación silenciosa.
