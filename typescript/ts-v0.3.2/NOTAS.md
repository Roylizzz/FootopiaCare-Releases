# Footopia Care (TypeScript) · ts-v0.3.2 — candidata de prueba

Construido desde `Roylizzz/FootopiaCare-Typescript`, rama `feat/migracion-integral-original-ts-sqlite` (commit 84c1571), el 21-nov-2026. Mismo contenido funcional que 0.3.1 más mejoras de diseño. Misma firma que 0.3.0/0.3.1 (versionCode 302): se instala encima sin borrar datos.

## Diseño
- La barra lateral queda fija a la altura de la pantalla; sólo se desplaza el contenido. La barra superior (buscar, avisos, cuenta) también queda fija.
- Configuración ordenada por parejas: datos del negocio | correo de salida, vinculación | accesos rápidos.
- Inicio: indicadores en filas completas; en tableta la agenda ocupa el ancho y los pendientes se reparten debajo.
- Los paneles laterales cortos (ficha del paciente, nueva atención, expediente, producto, copias) acompañan el desplazamiento.

## Verificado / pendiente
Verificado en la nube: pruebas automáticas (433), auditoría responsiva estricta en 16 anchos de PC y en Android (incluido 1124 px), E2E de horario, Android local, Inicio, correo y administración. Pendiente: aceptación en dispositivo físico y Windows real.
