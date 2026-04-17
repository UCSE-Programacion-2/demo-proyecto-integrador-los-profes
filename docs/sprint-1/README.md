# Sprint 1 — Wireframes, Figma y maquetado estático (TurniMed)

## Errores comunes de esta etapa

Ver **[errores-comunes.md](./errores-comunes.md)** (rutas de assets, deploy estático, enlaces entre páginas).

## Objetivo

Traducir el relevamiento del Sprint 0 y el [Product Brief](../product-brief.md) en **pantallas** (wireframes), trabajo de diseño (Figma u otra herramienta) y **HTML/CSS estático** del flujo de turnos municipales.

## Qué tenés que entregar en esta carpeta

1. `figma/`
   - Link al archivo de Figma.
   - Capturas o exportaciones de las pantallas principales (mínimo 3).
   - Si usás variables/tokens, documentá nombres (paleta, tipografías).

2. `wireframes/`
   - Wireframes por pantalla (PNG/PDF).
   - Mínimo 1 wireframe por vista obligatoria.

3. `decisiones-ui.md`
   - Componentes principales (cards de turno, formularios, tablas de agenda, KPIs).
   - Paleta (referencia al Sprint 0).
   - Tipografías y reglas de estilo (márgenes, estados loading/error).

4. `flujo/`
   - Mapa de navegación: paciente (reserva/cancelación), profesional (agenda), admin (métricas y backoffice).

5. `resumen-sprint-1.md`
   - Un párrafo de logros.
   - 3 decisiones clave y por qué.
   - 3 riesgos o pendientes para el Sprint 2.

## Checklist

- [ ] Wireframes legibles con nombre de pantalla.
- [ ] Flujo coherente entre paciente, profesional y admin (aunque sea simplificado).
- [ ] `decisiones-ui.md` con contenido propio (no solo capturas).
- [ ] El resultado sirve como base para implementación en sprints siguientes.

## Criterio de corrección

Coherencia con el relevamiento y el brief, trazabilidad decisión → pantalla → implementación futura, flujo bien definido.

---

## Condición de aprobación (metodología)

1. No se aceptan commits directos a `main`.
2. Todo cambio sustantivo debe estar asociado a una **Issue** o tarjeta en **GitHub Projects**.
3. Regla: si no hay Issue en GitHub, el trabajo no cuenta para evaluación de proceso.

## Requerimientos técnicos (frontend estático)

1. **HTML5 semántico** y **CSS3** (Tailwind/Bootstrap opcional si ya dominan CSS base).
2. Diseño **responsive** (mobile first).
3. Sin lógica JS compleja: foco en maquetado y navegación estática.

## Vistas obligatorias (TurniMed)

1. **Home / Landing:** navbar, mensaje de valor (turnos sin filas), accesos a reserva y login simulado, footer.
2. **Búsqueda de turnos:** filtros por **especialidad** y **fecha** (solo UI), listado de franjas disponibles (mock estático).
3. **Detalle / confirmación de reserva:** datos de la franja elegida, botón “Confirmar reserva” (sin backend).
4. **Mis turnos y cancelación:** listado de turnos de ejemplo y acción “Cancelar” (confirmación modal o vista simple).
5. **Registro / identidad (paciente):** formulario maquetado (nombre, documento, email) según épica de validación de identidad (sin persistencia).
6. **Panel profesional:** agenda del día o semana (tabla o cards estáticas), bloqueo de fecha (UI).
7. **Panel administrativo (métricas):** tarjetas o gráficos simulados (ocupación, especialidades más solicitadas).
8. **404:** página no encontrada.
9. **Backoffice admin:** tabla maquetada de **especialidades** o **disponibilidad** con acciones visuales y formulario modal o vista para “alta” (mock).

## Backlog sugerido (tarjetas = ramas)

1. `chore/initial-setup`: repo, `.gitignore`, README con integrantes y link al brief.
2. `design/style-guide`: `variables.css` con colores y tipografías.
3. `feat/layout-base`: navbar y footer responsive en todas las HTML.
4. `feat/ui-home`: landing con CTAs hacia búsqueda de turnos.
5. `feat/ui-busqueda-turnos`: filtros y grilla de franjas mock.
6. `feat/ui-reserva-cancelacion`: detalle de reserva + mis turnos con cancelación maquetada.
7. `feat/ui-profesional-admin`: panel profesional y panel de métricas (pueden ser dos PR si divide el equipo).
8. `feat/ui-registro-paciente`: formulario de alta de paciente.
9. `feat/ui-backoffice`: tabla admin + formulario de alta mock.

## Flujo de trabajo obligatorio

1. En el tablero: asignarse la tarjeta y moverla a **In Progress** (o equivalente).
2. En Git: rama desde `main` (ej. `feat/ui-home`).
3. Commits pequeños con **Conventional Commits**.
4. PR hacia `main` con `Closes #ID` en el cuerpo del PR.
5. Code review: aprobación de un compañero antes del merge.

## Entregable del Sprint 1

Documento (PDF o link) con:

1. Link al repositorio.
2. Link al **GitHub Projects**.
3. Listado de PRs mergeados (evidencia de ramas).
4. URL del deploy estático (GitHub Pages o Vercel).
