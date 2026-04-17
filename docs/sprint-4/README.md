# Sprint 4 — React, deploy y Demo Day

## Errores comunes de esta etapa

Ver **[errores-comunes.md](./errores-comunes.md)** (variables `VITE_`, SPA en producción, CORS en deploy, build).

## Objetivo

Migrar a una **SPA con React** (Vite), rutas con **React Router**, y **deploy** público de frontend y backend.

## Refactorización

No copiar el vanilla “tal cual” dentro de React: pensar en **componentes** y efectos.

- Conservar `frontend-vanilla` como referencia.
- Trabajar en `frontend-react` (Vite) según la estructura del repo plantilla.

## Requerimientos técnicos

### A. SPA y rutas

1. Navegación sin recarga completa de página.
2. **React Router DOM**.
3. Componentes reutilizables (`Navbar`, cards de turno, `Footer`, etc.).
4. Rutas protegidas para **admin** y/o **profesional** según el diseño.

### B. Estado y datos

1. `useState` para formularios y UI local.
2. `useEffect` para llamadas a la API.
3. **Context** (opcional) para usuario logueado o datos compartidos de reserva.

### C. Deploy

Revisar [deploy-checklist.md](./deploy-checklist.md). Backend en Render/Railway/etc. y frontend en Vercel/Netlify (o equivalente). Variables de entorno sin URLs hardcodeadas a `localhost` en producción.

## Backlog sugerido (tarjetas = ramas)

1. `chore/react-init`
2. `feat/react-layout` — layout común.
3. `feat/react-routing` — rutas paciente / admin / 404.
4. `feat/react-search-appointments` — listado de franjas desde API.
5. `feat/react-booking-flow` — reserva y confirmación.
6. `feat/react-auth` — login/registro controlados.
7. `ops/deploy-prod` — URLs HTTPS públicas.

## Demo Day

1. Duración acordada con la cátedra (referencia: 20–30 min por equipo).
2. **Demo con URL pública** (evitar depender de `localhost`).
3. Flujo sugerido TurniMed:
   - alta o login de paciente;
   - buscar especialidad/fecha y reservar;
   - ver turnos reservados y cancelar uno;
   - (si aplica) mostrar panel admin o profesional.

## Entregable final

1. `README.md` con URLs de producción e integrantes.
2. Tablero con trabajo del sprint cerrado.
3. Video de respaldo breve.
