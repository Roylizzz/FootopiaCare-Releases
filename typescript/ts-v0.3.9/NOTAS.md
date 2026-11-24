# Footopia Care (TypeScript) · ts-v0.3.9 — candidata de prueba

Construido desde `Roylizzz/FootopiaCare-Typescript`, rama `feat/migracion-integral-original-ts-sqlite` (commit db0eab0), el 24-nov-2026. Todo lo de 0.3.8 más:

## Vincular el celular cuando «no se pudo conectar con el PC»
- **Monitor:** comprueba si el firewall de Windows permite el puerto de Footopia Care y si la wifi está marcada como «pública». Si algo bloquea a los celulares, muestra un aviso con el botón **Permitir celulares en el firewall**. Windows pide permiso de administrador una vez; se crea una regla solo para redes privadas, el puerto del servidor y la subred local, y la red activa pasa a privada.
- **App Android:** dice por qué no llegó al PC: no respondió (firewall, red pública o wifi que aísla los equipos), rechazó la conexión (servidor detenido) o falló el certificado. También muestra la dirección a la que intentó conectarse.

APK con la misma firma (versionCode 309): se instala encima sin borrar datos.

## Verificado / pendiente
Verificado en la nube: 468 pruebas automáticas (incluidos los mensajes de conexión en Android) y prueba visual del Monitor. Pendiente: confirmar en Windows real el aviso de permisos y la regla del firewall, y vincular un teléfono físico.
