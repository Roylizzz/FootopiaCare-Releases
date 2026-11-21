# Footopia Care (TypeScript) · ts-v0.3.1 — candidata de prueba

Construido desde `Roylizzz/FootopiaCare-Typescript`, rama `feat/migracion-integral-original-ts-sqlite` (commit e529cc0), el 21-nov-2026.

> **Candidata de prueba, no versión estable.** La actualización sobre 0.3.0 y la conservación de datos se verificaron con pruebas automáticas (SQLite real y el troceado SQL original del plugin), **no** en un teléfono ni en Windows reales. No uses información real de pacientes hasta completar la aceptación.

> **0.3.0 queda retirada para Android:** su APK muestra «No se pudo abrir el almacenamiento local». No la instales; instala 0.3.1 encima (no desinstales ni borres datos: 0.3.1 actualiza la misma app y conserva lo guardado).

| Archivo | Uso |
|---|---|
| `FootopiaCare-Servidor-Setup-0.3.1.exe` | Instalador Windows x64 (servidor + monitor). Actualiza una instalación anterior conservando los datos (migración 018 incremental). |
| `FootopiaCare-Servidor-0.3.1-win-x64.zip` | Mismo contenido, portable. |
| `FootopiaCare-Monitor-0.3.1-win-x64.zip` | Solo el monitor de escritorio. |
| `FootopiaCare-Android-0.3.1-debug.apk` | App Android de desarrollo (`com.footopiacare.client.dev`, versionCode 301). Misma firma de depuración que 0.3.0 (SHA-256 del certificado `f9b72d35…42390692`): se instala **encima** de 0.3.0. |
| `SHA256SUMS.txt` | Hashes SHA-256. |

## Correcciones
- **Android no abría (0.3.0):** el plugin SQLite nativo trocea el SQL por `;` + salto de línea; los dos disparadores nuevos de la migración local 16 quedaban partidos (`… );` / `END;`), SQLite respondía *incomplete input* y toda la actualización del almacenamiento se revertía. Ahora se envían en una sola línea. La base de 0.3.0 quedó intacta en su versión anterior (la transacción se revirtió), así que 0.3.1 la actualiza normalmente.
- **Arranque con diagnóstico:** la pantalla de carga indica la etapa (clave, conexión, apertura, actualización, archivos). Si algo falla muestra qué etapa, un código (`FC-ARR-01…06`), *Reintentar* y *Copiar diagnóstico* (sin claves ni datos de pacientes). Nunca crea otra clave si ya existe una base cifrada y nunca borra ni reemplaza datos.
- **Sincronización:**
  - Una venta con sus líneas y cobros se confirma o se rechaza entera en el escritorio (también con más de 50 líneas y si se pierde la respuesta).
  - El resumen del teléfono distingue nuevos, modificados, borrados pendientes, enviados sin confirmar, en conflicto y sincronizados.
  - Un archivo ausente, dañado o sin permiso ya no viaja como «sin archivo»: se informa y no se borra nada.
  - El soporte de pago tiene una identidad local estable.

## Compatibilidad
- Teléfono y escritorio deben actualizarse juntos a 0.3.1: un escritorio 0.3.0 rechaza los lotes de una venta de más de 50 cambios y un teléfono 0.3.0 no entiende el estado «archivo no disponible».
- 0.2.0 (`com.footopiacare.client`, otra firma) es otra app: no se actualiza a 0.3.x.

## Verificado / pendiente
Verificado en la nube (Linux): `npm ci`, compilación, 433 pruebas automáticas (incluido el arranque nativo simulado y la actualización desde versiones locales 14 y 15), `verify:sql`, `verify:trace`, réplica del troceado del plugin con su código Java original (38 llamadas), E2E Android local y responsivo, comercio. APK: firma v2 (`apksigner`), paquete/versión (`aapt`), SQLCipher en las 4 arquitecturas.
Pendiente (sin emulador ni dispositivo en la nube): instalar 0.3.1 sobre 0.3.0 en un teléfono físico y comprobar que abre con los datos; `npm run test:android:native`; instalar en Windows 10/11 real.

Para que el monitor detecte esta versión, publica un GitHub Release con la etiqueta `ts-v0.3.1` (marcado como *pre-release*) y adjunta estos archivos (al menos el instalador).
