# Trazabilidad: Módulos 1 y 2 + Manual GitHub ↔ repositorio

Tabla de **evidencia pedagógica**: qué concepto del material del taller se materializa en qué parte de este repo.

| Concepto / fuente | Dónde se evidencia en el repo |
|-------------------|------------------------------|
| Roles Scrum (PO, SM, Developers) | Guión [guion-demostracion-tres-docentes.md](guion-demostracion-tres-docentes.md); issues con asignación y tablero. |
| Historia de usuario + INVEST | Template [.github/ISSUE_TEMPLATE/historia-de-usuario.yml](../../.github/ISSUE_TEMPLATE/historia-de-usuario.yml); [issues-semilla-sprint-0-1.md](issues-semilla-sprint-0-1.md). |
| Criterios Given / When / Then | Mismo template de historia; ejemplos en issues semilla. |
| Product Goal / épicas | [docs/product-brief.md](../product-brief.md); template Épica; labels `epic` / `feature` en [.github/labels.md](../../.github/labels.md). |
| Product Backlog vs Sprint Backlog | [tablero-y-automatizacion.md](tablero-y-automatizacion.md) + manual en [docs/material-taller/Manual GitHub EcosistemaAgil.docx.md](../material-taller/Manual%20GitHub%20EcosistemaAgil.docx.md). |
| Definition of Done | README de sprint ([docs/sprint-1/README.md](../sprint-1/README.md) condición PR + issue); DoD explícito en template de historia. |
| Conventional Commits | [docs/convencional-commits.md](../convencional-commits.md); hook [.githooks/commit-msg](../../.githooks/commit-msg); workflow [conventional-commits.yml](../../.github/workflows/conventional-commits.yml). |
| PR + revisión | [.github/PULL_REQUEST_TEMPLATE.md](../../.github/PULL_REQUEST_TEMPLATE.md); guion bloque 6. |
| Transparencia / inspección / adaptación | Sprint Review simulado: mostrar tablero antes/después del merge; mención Módulo 1 sección empirismo. |
| IA como “junior teammate” (Módulo 2) | Bloque 7 del guion; recordatorio de revisión humana antes de merge. |
| Comment-Driven Development | Demostración opcional en código del `frontend/` durante el taller (sin exigir entrega). |
| Tests + Copilot (Módulo 2) | Cuando el equipo agregue lógica en backend, vincular a `npm test` del paquete correspondiente (plantilla MERN). |

## Lectura sugerida para alumnos (orden)

1. [docs/product-brief.md](../product-brief.md)  
2. [docs/material-taller/Modulo1.docx.md](../material-taller/Modulo1.docx.md) (secciones 1.1–1.2)  
3. [docs/material-taller/Manual GitHub EcosistemaAgil.docx.md](../material-taller/Manual%20GitHub%20EcosistemaAgil.docx.md) (tablero + PR)  
4. [docs/sprint-0/README.md](../sprint-0/README.md) y [docs/sprint-1/README.md](../sprint-1/README.md)  
5. [docs/material-taller/Modulo2.docx.md](../material-taller/Modulo2.docx.md) (Copilot y flujo de PR/commits)
