# Sprint 2 — Backend core (Node.js, Express y MongoDB)

## Objetivo

Construir la **API REST** que alimentará TurniMed: turnos, especialidades, disponibilidad y usuarios (paciente / profesional / admin según diseño del equipo).

## Reglas vigentes (metodología)

Siguen vigentes las reglas del Sprint 1:

1. Repo configurado para **bloquear commits directos a `main`**.
2. Integrar código mediante **Pull Request**.
3. El PR requiere **aprobación de 2 compañeros** (o lo que defina la cátedra).
4. En la descripción del PR debe existir el vínculo al Issue/Tarjeta.

## Requerimientos técnicos

### A. Estructura de proyecto (MVC en `/backend`)

1. `/config`: conexión a BD y variables de entorno
2. `/models`: esquemas de Mongoose
3. `/controllers`: lógica
4. `/routes`: endpoints
5. `/middlewares`: validaciones y seguridad

### B. Funcionalidades nucleares (API)

La API debe cubrir al menos:

1. **Usuarios y autenticación (mínimo viable)**
   - Registro e inicio de sesión (o el modelo que elijan con la cátedra).

2. **Dominio TurniMed (CRUD y consultas)**
   - **Especialidades** o tipo de consulta: listado y detalle.
   - **Franjas / turnos disponibles:** listado con filtros por especialidad y fecha.
   - **Reservas:** crear reserva (paciente), consultar “mis turnos”, cancelar (liberar franja).
   - Rutas de **escritura** protegidas para roles admin/profesional según el diseño (por ejemplo: alta de disponibilidad).

3. **Opcional según alcance del sprint**
   - Endpoints de métricas agregadas para el panel administrativo (counts por especialidad, ocupación).

## Backlog sugerido (tarjetas = ramas)

1. `chore/backend-setup` — servidor responde en el puerto acordado.
2. `feat/db-connection` — MongoDB con `.env` no versionado.
3. `feat/model-user` — usuario con rol (`paciente`, `profesional`, `admin` o equivalente).
4. `feat/api-specialties-slots` — `GET` de especialidades y franjas disponibles.
5. `feat/api-appointments` — `POST` reserva, `GET` mis turnos, `DELETE` o `PATCH` cancelación.
6. `chore/seed-data` — script con datos de prueba (especialidades + franjas).

## Documentación de apoyo

- **[api-contract.md](./api-contract.md)**: contrato mínimo recomendado.
- **[errores-comunes.md](./errores-comunes.md)**

## Herramientas de prueba

Probar con Postman, REST Client o Thunder Client. Verificar **códigos HTTP** (`200`, `201`, `400`, `401`, `404`, etc.).

## Entregable del Sprint 2

1. Link al repositorio con PRs del sprint cerrados.
2. Link al tablero actualizado.
3. Colección exportada (`.json`) de pruebas de API.
4. `backend/.env.example` sin secretos reales.
