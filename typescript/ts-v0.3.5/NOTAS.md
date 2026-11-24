# Footopia Care (TypeScript) · ts-v0.3.5 — candidata de prueba

Construido desde `Roylizzz/FootopiaCare-Typescript`, rama `feat/migracion-integral-original-ts-sqlite` (commit f94e793, último de la rama), el 24-nov-2026. Incluye todo lo de 0.3.2 más: puesta en marcha, horarios y permisos de Android simplificados; recuperación de cuenta, decisiones de atención, reservas rápidas y retiro de fotos; vinculación por QR, importación Excel y mejoras de uso.

APK con la misma firma que 0.3.0–0.3.2 (certificado SHA-256 `f9b72d35…42390692`, versionCode 305): se instala encima sin borrar datos.

## Verificado / pendiente
Verificado en la nube sobre f94e793: `npm ci`, compilación, 463 pruebas automáticas, réplica del troceado SQL del plugin Android (44 llamadas, arranque seguro), firma y paquete de la APK, sumas SHA-256. La prueba E2E `android-local` debe actualizarse a la importación Excel (busca el antiguo campo Word); hasta ese punto abre, crea la cuenta y configura el negocio. Pendiente: dispositivo físico (incluida la cámara para el QR) y Windows real.
