# Guión de demostración — Tres docentes (90 a 120 minutos)

Objetivo: mostrar **de punta a punta** cómo se configura el proyecto integrador con metodología ágil, GitHub como ecosistema Scrum y el caso **TurniMed Municipal**, para que luego los alumnos repliquen el flujo en GitHub Classroom.

**Frase ancla (Módulo 1):** “Lo que murió es la ceremonia sin propósito. Lo que vive es el empirismo.”

---

## Roles sugeridos

| Rol docente | Enfoque en la demo |
|-------------|-------------------|
| **Product Owner (PO)** | Brief, épicas, prioridad del backlog, Sprint Goal enunciado en voz alta. |
| **Scrum Master (SM)** | Tablero, columnas, workflow automático, milestones, facilitación del “planning” simulado. |
| **Developer (DEV)** | Rama, commits convencionales, PR, `Closes #N`, code review entre docentes. |

Los roles pueden rotar en otra sesión; lo importante es que los alumnos **vean las tres voces**.

---

## Minutaje propuesto

### Bloque 1 — Contexto y producto (15 min) — PO

1. Abrir [docs/product-brief.md](../product-brief.md) y sintetizar: problema, usuarios, épicas y **fuera de MVP**.
2. Explicar por qué TurniMed sirve como caso único para el taller (salud pública, turnos, sin pasarela de pagos).
3. Mostrar [docs/material-taller/Modulo1.docx.md](../material-taller/Modulo1.docx.md) en una diapositiva o fragmento: roles Scrum y Definition of Done a alto nivel.

### Bloque 2 — Repositorio plantilla y material (10 min) — DEV o PO

1. Mostrar la raíz del repo: `backend/`, `frontend/`, `docs/`, `.github/`.
2. Enlace a [docs/material-taller/README.md](../material-taller/README.md) (Módulos 1 y 2 + Manual GitHub).
3. Mencionar **Conventional Commits** y comando `node scripts/install-git-hooks.mjs` (sin instalar en vivo salvo que quieran mostrar el error de un commit mal formado).

### Bloque 3 — Issues: de épica a historia (20 min) — PO + SM

1. PO: crear (o mostrar ya creadas) **2 épicas** alineadas al brief usando el template “Épica” (`.github/ISSUE_TEMPLATE`).
2. PO: crear **1 historia de usuario** hija, con criterios Given/When/Then, etiqueta `feature` y tamaño `S — small`.
3. SM: asociar la historia al **Milestone** “Sprint 1” y ubicar la tarjeta en el tablero (columna acordada).

### Bloque 4 — Tablero y transparencia (15 min) — SM

1. Abrir GitHub Projects vinculado al repo; recorrer columnas según [tablero-y-automatizacion.md](tablero-y-automatizacion.md).
2. Activar o verificar el workflow **Item closed → Done** (si usan Projects nuevo).
3. Explicar límite de WIP en **In Progress** (1–2 por persona) como disciplina docente.

### Bloque 5 — Sprint 0 en el repo (15 min) — SM + DEV

1. Mostrar [docs/sprint-0/README.md](../sprint-0/README.md): entregables `relevamiento.md`, `fotos/`, `logo/` (sin datos personales reales).
2. Opcional: pegar contenido de [ejemplo-relevamiento-sprint-0.md](ejemplo-relevamiento-sprint-0.md) en una rama de demo.
3. PR de ejemplo solo con documentación: mostrar revisión y merge.

### Bloque 6 — Sprint 1: flujo Git completo (25 min) — DEV + SM

1. DEV: desde `main`, `git pull` y `git checkout -b feat/ui-home-demo`.
2. Cambio mínimo visible (por ejemplo título en HTML de la landing o texto “TurniMed”).
3. Commits con formato `feat(ui-home): ...` alineado a [docs/convencional-commits.md](../convencional-commits.md).
4. `git push` y **Pull Request** hacia `main`: en el **cuerpo** del PR escribir `Closes #XX` (número real del issue).
5. Otro docente hace **code review** (comentario breve) y aprueba; merge.
6. SM: mover tarjeta a **In Review** antes del merge y verificar cierre automático a **Done** si configuraron el workflow.

### Bloque 7 — IA como copiloto (10 min) — DEV

Conectar con [docs/material-taller/Modulo2.docx.md](../material-taller/Modulo2.docx.md):

1. Ciclo contexto → generación → revisión → validación (tests/CI).
2. Demo corta: **Comment-Driven Development** en una función o en un bloque HTML/CSS (sin depender de Copilot si no hay licencia: describir el flujo).

### Bloque 8 — GitHub Classroom y cierre (10 min) — SM

1. Seguir el checklist de [github-classroom-y-template.md](github-classroom-y-template.md).
2. Deberes para alumnos: aceptar assignment, clonar, configurar tablero, completar Sprint 0 y abrir primer PR del Sprint 1.

---

## Preguntas frecuentes para anticipar en voz alta

- **¿Classroom crea el tablero?** No; el equipo lo crea después de aceptar el repo.
- **¿Pueden pushear a main?** Depende de las reglas de la org; en cursada suele prohibirse y la demo debe mostrar **PR + revisión**.
- **¿El demo debe tener MERN completo?** No en esta sesión: el foco es **proceso y trazabilidad**; el código es plantilla para evolución.
