# Tablero GitHub Projects y automatización

Este documento alinea la demo con el [Manual GitHub Ecosistema Ágil](../material-taller/Manual%20GitHub%20EcosistemaAgil.docx.md) y con los README de sprint de este repo.

## Columnas recomendadas (vista Scrum del manual)

| Columna | Contenido | Quién mueve |
|---------|-----------|-------------|
| **Product Backlog** | Historias aún no planificadas para el sprint actual. | PO ordena prioridad. |
| **Sprint Backlog** | Compromiso del sprint (Planning). | Developers / acuerdo del equipo. |
| **In Progress** | Desarrollo activo. Pocas tarjetas por persona (WIP limit). | Developer al iniciar. |
| **In Review** | PR abierto esperando revisión. | Developer al abrir PR. |
| **Done** | Mergeado en `main`, cumple DoD, issue cerrado. | Automático si configuraron workflow (ver abajo). |

## Workflow: Issue cerrado → columna Done

1. En el proyecto de GitHub: menú **···** → **Workflows**.
2. Activar **Item closed** (o equivalente): al **cerrarse** un Issue, mover la tarjeta a **Done**.

### Condiciones para que el cierre sea automático por PR

1. En el **cuerpo** del Pull Request (no basta el título): `Closes #12` (número real del issue).
2. El merge del PR debe ser hacia la rama por defecto (**main**).

Si la tarjeta no se mueve: revisar esas dos condiciones y que el issue esté **vinculado** al mismo repositorio que el proyecto.

## Mapeo con la vista “mínima” de cuatro columnas

En algunas guías de cursada aparece: `Backlog`, `To Do`, `In Progress`, `Done`. Es válido para empezar, pero **no es contradictorio** con el manual de cinco columnas:

| Vista 4 columnas | Correspondencia sugerida |
|------------------|---------------------------|
| Backlog | Product Backlog (o mezcla Product + Sprint si simplifican). |
| To Do | Sprint Backlog (comprometido y aún no iniciado). |
| In Progress | In Progress. |
| Done | Done (cerrado + merge). |

**In Review** puede omitirse al principio si el equipo mueve la tarjeta directamente de *In Progress* a *Done* al mergear; el manual la incluye para **visibilizar el code review**, práctica que la cátedra puede exigir en Programación II.

## Labels y milestones

- Crear labels según [.github/labels.md](../../.github/labels.md) (tipo, prioridad, tamaño).
- Crear **Milestones** `Sprint 0` … `Sprint 4` con fechas de cierre orientativas.

## DoD (Definition of Done) mínimo para mover a Done

Acordar en voz alta en la demo:

- Código mergeado a `main`.
- PR con al menos una aprobación (o dos, según regla del README del equipo).
- Issue cerrado con trazabilidad (`Closes #N`).
