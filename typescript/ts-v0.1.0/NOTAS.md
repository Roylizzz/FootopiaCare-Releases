# FootopiaCare 2 (TypeScript) · ts-v0.1.0

Construido desde `Roylizzz/FootopiaCare-Typescript`, rama `ccr-3e72e79a-d9jda7` (commit 9578b77), el 14-nov-2026.

> **Prototipo de desarrollo.** No uses información real de pacientes hasta completar la aceptación.

| Archivo | Uso |
|---|---|
| `FootopiaCare2-Servidor-Setup-0.1.0.exe` | Instalador Windows x64 (servidor + monitor). Sin permisos de administrador. |
| `FootopiaCare2-Servidor-0.1.0-win-x64.zip` | Mismo contenido, portable. |
| `FootopiaCare2-Monitor-0.1.0-win-x64.zip` | Solo el monitor, para reemplazarlo dentro de una instalación existente. |
| `FootopiaCare2-Android-0.1.0.apk` | App Android (Android 7 o superior). |
| `SHA256SUMS.txt` | Hashes SHA-256. |

## Uso rápido
1. En el PC: ejecuta el instalador y abre **FootopiaCare 2** (monitor). Pulsa *Abrir FootopiaCare* y crea la primera cuenta.
2. Para celulares: en el monitor activa *Permitir celulares de esta red (HTTPS)*, elige la IP del PC y guarda. Si Windows pregunta por el firewall, permite solo redes privadas.
3. En el celular: instala el APK (permitir fuentes desconocidas), ábrelo y escanea el QR del monitor o escribe la dirección y el código de vinculación.

## Verificado / pendiente
Verificado en Linux + Wine: instalación, monitor, servidor (SQLite y Argon2 nativos), HTTPS LAN, actualización sobre instancia en ejecución y desinstalación conservando datos. APK firmado y verificado con `apksigner`.
Pendiente: Windows 10/11 real, teléfonos físicos, firma de código del instalador (SmartScreen avisará de editor desconocido).

Para que el monitor detecte esta versión como actualización, publica un GitHub Release con la etiqueta `ts-v0.1.0` y adjunta estos archivos.
