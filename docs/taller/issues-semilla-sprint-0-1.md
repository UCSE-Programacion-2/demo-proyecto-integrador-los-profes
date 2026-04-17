# Issues semilla — Sprint 0 y Sprint 1 (TurniMed)

Textos orientativos para **crear en vivo** en GitHub (templates: Épica e Historia de usuario). Ajustar numeración de issues al crear las épicas primero.

---

## Épicas (tipo `epic`, label `epic`)

### Épica E1 — Reserva self-service

**Título:** `EPIC — Reserva de turnos (paciente)`

**Descripción:**  
Implementar el flujo en el que un paciente autogestivo busca por especialidad y fecha, ve franjas disponibles y confirma una reserva, con feedback claro. Alineado al brief [docs/product-brief.md](../product-brief.md) (épica “Reserva de Turnos”).

---

### Épica E2 — Operación municipal

**Título:** `EPIC — Panel admin y métricas`

**Descripción:**  
Superficie para el administrador municipal: ocupación, especialidades más solicitadas y gestión básica de catálogo de especialidades o disponibilidad (según alcance). Alineado a “Panel de Monitoreo Administrativo” y backoffice del Sprint 1.

---

## Sprint 0 — Historias sugeridas

### HU-S0-01 — README del equipo

**Historia:**  
Como **docente** quiero un **README** completo con equipo, link al tablero y link al brief para que los alumnos entiendan el panel de control del repositorio.

**Criterios de aceptación:**

- [ ] Dado que abro el repo en GitHub, cuando leo el `README.md`, entonces veo nombre del equipo y lista de integrantes con link a GitHub.
- [ ] Dado que busco el tablero, cuando sigo el link del README, entonces accedo al GitHub Project del equipo.
- [ ] Dado el brief, cuando busco la referencia, entonces hay enlace a `docs/product-brief.md`.

**Rama sugerida:** `docs/readme-sprint0`

---

### HU-S0-02 — Relevamiento de contexto

**Historia:**  
Como **integrante del equipo** quiero documentar el **contexto** del centro modelo y necesidades de turnos para fundamentar el diseño en Sprint 1.

**Criterios de aceptación:**

- [ ] Dado el Sprint 0, cuando abro `docs/sprint-0/relevamiento.md`, entonces hay al menos tres necesidades explícitas ligadas al brief.
- [ ] Dado la carpeta `docs/sprint-0/fotos/`, cuando reviso el relevamiento, entonces cada grupo de fotos tiene una descripción de aporte (sin datos personales).
- [ ] Dado `docs/sprint-0/logo/`, cuando reviso los archivos, entonces existe un logo o propuesta con justificación breve.

**Rama sugerida:** `docs/sprint0-relevamiento`

---

## Sprint 1 — Historias sugeridas (demo corta)

Elegir **una** para el flujo en vivo del taller (DEV + PR).

### HU-S1-01 — Landing TurniMed

**Historia:**  
Como **paciente** quiero una **landing** clara con acceso a la búsqueda de turnos para entender el valor del sistema municipal.

**Criterios de aceptación:**

- [ ] Dado que ingreso al sitio estático, cuando veo la home, entonces hay navbar, mensaje de valor y footer responsive.
- [ ] Dado el navbar, cuando hago clic en “Reservar turno” (o similar), entonces navego a la página de búsqueda maquetada.
- [ ] Dado un viewport móvil, cuando comparo con desktop, entonces el layout no se rompe (mobile first).

**Épica padre:** `#<id-E1>`  
**Rama sugerida:** `feat/ui-home`

---

### HU-S1-02 — Búsqueda maquetada

**Historia:**  
Como **paciente** quiero **filtros** por especialidad y fecha (solo UI) para encontrar visualmente una franja de ejemplo.

**Criterios de aceptación:**

- [ ] Dado la página de búsqueda, cuando aplico filtros (mock), entonces la grilla muestra al menos tres franjas de ejemplo estáticas.
- [ ] Dado una franja, cuando hago clic en “Ver detalle”, entonces navego a la vista de confirmación maquetada.

**Épica padre:** `#<id-E1>`  
**Rama sugerida:** `feat/ui-busqueda-turnos`

---

## Tips para el PO en el aula

- Crear primero las **épicas** y anotar sus números `#N` antes de las historias hijas.
- Etiquetar con `S — small` las historias de demo en vivo para que el cierre quepa en el tiempo del taller.
