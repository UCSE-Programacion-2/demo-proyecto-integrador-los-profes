# Sprint 3 — Integración frontend-backend (JavaScript vanilla + Fetch)

## Objetivo

Conectar el maquetado del Sprint 1 con la API del Sprint 2: datos reales con **JavaScript ES6+** y **Fetch API**.

## Reglas vigentes (metodología)

1. No commits directos a `main`.
2. Integración vía **Pull Request** con revisión.
3. PR con enlace al Issue/Tarjeta en la descripción.

## Documentación de apoyo

- [../sprint-2/api-contract.md](../sprint-2/api-contract.md)
- [errores-comunes.md](./errores-comunes.md)

## Requerimientos técnicos

### A. Consumo de API

1. **Búsqueda de turnos**
   - Al cargar la vista de búsqueda: `fetch` (GET) a especialidades y/o franjas (`/api/specialties`, `/api/slots?...`).
   - Render dinámico de tarjetas o filas.

2. **Detalle y reserva**
   - Capturar `slotId` (query o estado).
   - `POST /api/appointments` y feedback al usuario.

### B. Panel administrativo (CRUD)

- Consumir API para crear/editar/borrar **especialidades** o **franjas** (según contrato acordado).
- Mensajes de éxito/error en UI.

### C. Mis turnos y cancelación

- Listar reservas del usuario autenticado.
- Cancelar con `DELETE` o `PATCH` según contrato.

### D. CORS

Si el front y el back corren en distintos orígenes, configurar `cors` en Express para el origen del front local y el de deploy.

## Backlog sugerido (tarjetas = ramas)

1. `chore/enable-cors`
2. `feat/js-specialties-slots` — listados desde API en la vista de búsqueda.
3. `feat/js-appointment-book` — reserva con `POST`.
4. `feat/js-auth-login-register` — flujo mínimo de sesión.
5. `feat/js-my-appointments` — listado y cancelación.
6. `feat/js-admin-crud` — panel admin conectado a endpoints de escritura.
7. `feat/js-professional-view` — agenda del profesional si aplica al contrato.

## Entregable del Sprint 3

1. Link al repositorio y al tablero.
2. Video corto (unos 5 min): registro o login, búsqueda de franja, reserva, ver “mis turnos”, cancelar; opcional: acción admin.
