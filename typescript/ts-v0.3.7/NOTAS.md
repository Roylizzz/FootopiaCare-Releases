# Footopia Care (TypeScript) · ts-v0.3.7 — candidata de prueba

Construido desde `Roylizzz/FootopiaCare-Typescript`, rama `feat/migracion-integral-original-ts-sqlite` (commit e300bef), el 24-nov-2026. Todo lo de 0.3.6 más una puesta en marcha más clara:

- **Horario:** los días son botones de un toque, con atajos «Lunes a viernes», «Lunes a sábado» y «Todos los días». Se propone lunes a viernes. Sólo los días abiertos tienen fila, y los que usan el horario habitual muestran la hora con «Cambiar».
- **Servicios:** el primer servicio tiene título y explicación; la importación desde Excel ocupa una fila compacta.
- **Importar pacientes:** una zona clara para elegir el archivo, con la plantilla al lado.
- **Revisión:** lista compacta con estado y resumen en una línea, y botón «Cambiar» en cada punto.

APK con la misma firma (versionCode 307): se instala encima sin borrar datos.

## Verificado / pendiente
Verificado en la nube: 465 pruebas automáticas; E2E del asistente de PC y del horario; auditoría responsiva estricta de horario, servicios y puesta en marcha en 1280, 768, 390 y 320 px; revisión visual en modo oscuro. La E2E `android-local` llega al final del asistente y de la importación, y después se detiene en la ficha del paciente: busca un título que la 0.3.5 quitó y hay que actualizarla. Pendiente: dispositivo físico y Windows real.
