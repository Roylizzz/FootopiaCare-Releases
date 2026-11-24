# Footopia Care (TypeScript) · ts-v0.3.6 — candidata de prueba

Construido desde `Roylizzz/FootopiaCare-Typescript`, rama `feat/migracion-integral-original-ts-sqlite` (commit 23f19e8), el 24-nov-2026. Todo lo de 0.3.5 más:

## Una sola dirección, con el certificado instalado
- El PC y los celulares usan la misma dirección: `https://<IP del PC>:4443` (en una instalación nueva el Monitor elige sola la IP). Ya no se muestra la de 127.0.0.1.
- Al abrir Footopia Care desde el Monitor (o al activar la red), si este PC aún no confía en el certificado de la clínica, se instala en el almacén del usuario: Windows pide confirmarlo una vez y no hace falta administrador. Edge, Chrome y la ventana del Monitor lo usan (Firefox tiene su propio almacén).
- Celulares: la app Android confía sola al vincularse con el QR. Para usar también el navegador del celular, la página de descarga de la app (QR del Monitor → Celulares) ofrece el certificado y los pasos para instalarlo en Android.
- Al actualizar, inicia sesión una vez en la nueva dirección (la sesión de la dirección 127.0.0.1 no se comparte).

APK con la misma firma que 0.3.0–0.3.5 (versionCode 306): se instala encima sin borrar datos.

## Verificado / pendiente
Verificado en la nube: 465 pruebas automáticas, prueba visual del Monitor, compilación de la APK y del instalador, sumas SHA-256. Pendiente: confirmar en Windows real el diálogo de instalación del certificado y la apertura en la dirección de la red; dispositivo físico.
