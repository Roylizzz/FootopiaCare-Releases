# Footopia Care (TypeScript) · ts-v0.3.8 — candidata de prueba

Construido desde `Roylizzz/FootopiaCare-Typescript`, rama `feat/migracion-integral-original-ts-sqlite` (commit b156514), el 24-nov-2026. Todo lo de 0.3.7 más:

## Reserva rápida: cita sin crear paciente
- En **Nueva cita**, elige «Reserva rápida» y escribe el nombre de quien asistirá y su teléfono (y, si llamó otra persona, quién y su parentesco). No se crea ficha ni se piden datos clínicos. Si aún no hay servicios, puedes escribir el motivo.
- En la **agenda** aparece como «Reserva» con borde punteado. Al pulsarla puedes confirmarla, moverla, cancelarla, marcar que no asistió o **asociarla a un paciente**, lo que crea su cita en la misma franja.
- Una reserva **ocupa su franja**: no se puede agendar otra cita ni otra reserva encima, y el buscador de horarios no la ofrece.
- Las reservas se guardan en el equipo donde se crean: todavía no viajan entre el PC y el teléfono.

APK con la misma firma (versionCode 308): se instala encima sin borrar datos.

## Verificado / pendiente
Verificado en la nube: 467 pruebas automáticas (incluidas las reservas en escritorio y en Android), y las E2E de reserva rápida de punta a punta, alta de cita, agenda e inicio. Pendiente: dispositivo físico y Windows real.
