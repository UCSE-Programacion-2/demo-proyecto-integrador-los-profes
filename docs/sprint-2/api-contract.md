# API contract (recomendado) — TurniMed Municipal

Documento para **Sprint 2** (backend); mantenerlo alineado con el frontend en Sprints 3 y 4.

Contrato **mínimo recomendado** para integrar sin desalinearse. Si el equipo cambia rutas o nombres, debe actualizar consumidores y documentar el cambio en el PR.

## Autenticación

Para la cursada suele bastar:

- validar credenciales en backend
- devolver datos básicos del usuario
- estado de sesión simple en frontend (`localStorage` u otro acordado)

### Roles sugeridos

- `admin`: gestiona especialidades, disponibilidad y ve métricas.
- `profesional`: consulta/modifica su agenda según diseño.
- `paciente`: reserva y cancela sus turnos.

## Endpoints de auth

### Registrar usuario

- `POST /api/auth/register`
- Body (ejemplo):
```json
{ "name": "Ana", "email": "ana@mail.com", "password": "********", "role": "paciente" }
```
- Respuestas: `201` creado, `400` datos inválidos.

### Login

- `POST /api/auth/login`
- Body:
```json
{ "email": "ana@mail.com", "password": "********" }
```
- Respuesta `200`:
```json
{ "user": { "id": "....", "name": "Ana", "role": "paciente" } }
```
- `401` credenciales inválidas.

## Especialidades

### Listar

- `GET /api/specialties`
- Respuesta:
```json
{ "items": [ { "id": "....", "name": "Clinica médica", "description": "..." } ] }
```

### Detalle

- `GET /api/specialties/:id`

## Franjas / turnos disponibles

### Listar franjas libres

- `GET /api/slots`
- Query recomendada: `?specialtyId=...&date=YYYY-MM-DD`
- Respuesta:
```json
{
  "items": [
    { "id": "....", "specialtyId": "....", "startsAt": "2026-05-10T09:00:00Z", "professionalName": "Dr. ...", "status": "available" }
  ]
}
```

### Crear franja (admin o profesional)

- `POST /api/slots`
- Body (ejemplo):
```json
{ "specialtyId": "....", "startsAt": "2026-05-10T09:00:00Z", "durationMinutes": 30 }
```
- Respuestas: `201`, `400`, `401/403`.

### Editar / borrar franja

- `PUT /api/slots/:id` o `PATCH`
- `DELETE /api/slots/:id`

## Reservas (appointments)

### Crear reserva (paciente)

- `POST /api/appointments`
- Body:
```json
{ "slotId": "...." }
```
- Respuestas: `201` con la reserva, `400` slot no disponible, `401` no autenticado.

### Mis turnos

- `GET /api/appointments/me`
- Respuesta:
```json
{
  "items": [
    { "id": "....", "slotId": "....", "specialtyName": "...", "startsAt": "...", "status": "confirmed" }
  ]
}
```

### Cancelar

- `DELETE /api/appointments/:id` (o `PATCH` con `status: cancelled`)
- Respuestas: `200`, `404`, `401`.

## Métricas (opcional en Sprint 2)

- `GET /api/metrics/overview`
- Ejemplo:
```json
{ "occupancyRate": 0.72, "topSpecialties": [ { "name": "Pediatría", "appointments": 42 } ] }
```

## Formato de errores

```json
{ "error": { "code": "BAD_REQUEST", "message": "Texto claro para el cliente" } }
```

## Regla de oro

Si cambia ruta, método o body, el frontend y este documento deben actualizarse en el mismo ciclo de PR.
