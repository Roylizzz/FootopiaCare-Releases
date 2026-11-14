# Footopia Care (TypeScript) · ts-v0.2.0

Construido desde `Roylizzz/FootopiaCare-Typescript`, rama `ccr-3e72e79a-d9jda7` (commit e328cf6), el 14-nov-2026.

> **Prototipo de desarrollo.** No uses información real de pacientes hasta completar la aceptación.

| Archivo | Uso |
|---|---|
| `FootopiaCare-Servidor-Setup-0.2.0.exe` | Instalador Windows x64 (servidor + monitor de escritorio). Sin permisos de administrador. |
| `FootopiaCare-Servidor-0.2.0-win-x64.zip` | Mismo contenido, portable. |
| `FootopiaCare-Monitor-0.2.0-win-x64.zip` | Solo el monitor de escritorio, para reemplazarlo dentro de una instalación existente. |
| `FootopiaCare-Android-0.2.0.apk` | App Android (Android 7 o superior). |
| `SHA256SUMS.txt` | Hashes SHA-256. |

## Novedades frente a 0.1.0
- Monitor de escritorio nativo: ventana propia (WebView2) e icono en la bandeja del sistema; cerrar la ventana deja el servidor activo.
- Nombre «Footopia Care» y logo original en la web, el monitor, el instalador y la app.

## Uso rápido
1. En el PC: ejecuta el instalador y abre **Footopia Care** (monitor). Pulsa *Abrir Footopia Care* y crea la primera cuenta.
2. Para celulares: en el monitor activa *Permitir celulares de esta red (HTTPS)*, elige la IP del PC y guarda. Si Windows pregunta por el firewall, permite solo redes privadas.
3. En el celular: instala el APK (permitir fuentes desconocidas), ábrelo y escanea el QR del monitor o escribe la dirección y el código de vinculación.

## Verificado / pendiente
Verificado en Linux + Wine: instalación, monitor de escritorio (proceso, instancia única, reinicio automático, cierre ordenado), servidor (SQLite y Argon2 nativos), actualización sobre instancia en ejecución y desinstalación conservando datos. APK firmado y verificado con `apksigner`.
Pendiente: ventana WebView2 e icono de bandeja en Windows 10/11 real (WebView2 no funciona en Wine), teléfonos físicos, firma de código del instalador (SmartScreen avisará de editor desconocido).

Para que el monitor detecte esta versión como actualización, publica un GitHub Release con la etiqueta `ts-v0.2.0` y adjunta estos archivos.
