# Footopia Care (TypeScript) · ts-v0.3.0

Construido desde `Roylizzz/FootopiaCare-Typescript`, rama `feat/migracion-integral-original-ts-sqlite` (commit cda3d4d), el 21-nov-2026.

> **Prototipo de desarrollo.** No uses información real de pacientes hasta completar la aceptación.

| Archivo | Uso |
|---|---|
| `FootopiaCare-Servidor-Setup-0.3.0.exe` | Instalador Windows x64 (servidor + monitor de escritorio). Sin permisos de administrador. Actualiza una instalación anterior conservando los datos. |
| `FootopiaCare-Servidor-0.3.0-win-x64.zip` | Mismo contenido, portable. |
| `FootopiaCare-Monitor-0.3.0-win-x64.zip` | Solo el monitor de escritorio, para reemplazarlo dentro de una instalación existente. |
| `FootopiaCare-Android-0.3.0-debug.apk` | App Android de desarrollo (Android 7 o superior), autónoma con su propio almacenamiento. Firmada con clave de depuración. |
| `SHA256SUMS.txt` | Hashes SHA-256. |

## Novedades frente a 0.2.0
- **App Android autónoma:** funciona sin conexión con su propio almacenamiento (pacientes, agenda, atenciones, tratamientos, formularios, consentimientos, fotos y documentos, comercio, informes, tareas, lista de espera y descuentos).
- **Sincronización PC ↔ Android** por HTTPS en la red local: pacientes, datos del negocio y horario, agenda (con aviso de citas que chocan), historia clínica, archivos (fotos, documentos, firmas), ventas, cobros e inventario. Nunca sobrescribe un cambio hecho en ambos equipos: lo muestra para revisarlo. Se sincroniza sola cada 10 minutos con la app abierta y al recuperar la red.
- **Monitor rediseñado:** estado visible con una acción principal, pestañas (Resumen, Celulares, Actualizaciones, Ajustes, Registro) y vinculación de celulares paso a paso.
- **Diseño:** pantallas revisadas en PC, tableta y móvil (sin desbordes); Inicio, ficha del paciente y listas más claras; acciones peligrosas en rojo y separadas.

## Uso rápido
1. En el PC: ejecuta el instalador y abre **Footopia Care** (monitor). Pulsa *Abrir Footopia Care* y crea la primera cuenta (o entra con la tuya si actualizas).
2. Para celulares: en el monitor, pestaña *Celulares*, activa *Permitir celulares de esta red*, elige la IP del PC y guarda. Si Windows pregunta por el firewall, permite solo redes privadas.
3. En el PC, abre Footopia Care por la dirección HTTPS que muestra el monitor y, en *Configuración → Vinculación con Android*, genera un código. En el celular: instala el APK (permitir fuentes desconocidas), crea tu cuenta, pega ese código en el mismo apartado y usa *Sincronizar todo*.

## Verificado / pendiente
Verificado en la nube (Linux): compilación, pruebas automáticas, sincronización con el servidor real por HTTPS, auditorías de diseño en 16 anchos de PC y 10 de Android, firma APK v2 (`apksigner`) y metadatos (`aapt`), contenido del paquete Windows.
Pendiente: instalar y usar en Windows 10/11 real (ventana WebView2, bandeja, SmartScreen avisará de editor desconocido), instalar el APK en teléfonos físicos y probar la sincronización por la red local real.

Para que el monitor detecte esta versión como actualización, publica un GitHub Release con la etiqueta `ts-v0.3.0` y adjunta estos archivos (al menos el instalador).
