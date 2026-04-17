# Documentación del proyecto (demo TurniMed)

Este directorio organiza la documentación del **proyecto integrador de demostración** por sprints. El producto de referencia es **TurniMed Municipal** (gestión de turnos en salud pública municipal). Ver el brief en [product-brief.md](product-brief.md).

## Qué tenés que completar

1. **Sprint 0:** contexto del caso, materiales visuales y base para diseño (sin datos personales reales).
2. **Sprint 1:** wireframes, Figma (o equivalente) y maquetado estático HTML/CSS de las pantallas del MVP.
3. **Sprint 2:** backend core (Node.js, Express, MongoDB/Mongoose) y API REST (recursos alineados a turnos, pacientes, agendas).
4. **Sprint 3:** integración frontend-backend (Fetch API), flujos de reserva y panel admin.
5. **Sprint 4:** modernización a React (SPA con Router), deploy y Demo Day.

## Estructura sugerida

- `sprint-0/`: relevamiento del contexto, referencias visuales y logo (marca ficticia permitida en el demo).
- `sprint-1/`: wireframes, recursos de diseño y documentación UI.
- `sprint-2/`: endpoints, modelos, pruebas con Postman u otras herramientas.
- `sprint-3/`: consumo de API, flujos paciente/profesional/admin y evidencias de integración.
- `sprint-4/`: SPA con React, rutas, deploy y evidencias para Demo Day.

## Reglas simples

- Archivos con nombres claros (ej.: `referencia-centro-01.jpg`).
- Comprimí imágenes razonablemente; no subas archivos enormes sin necesidad.
- Cada sprint incluye un `README.md` de referencia y conviene un **resumen** de lo hecho (`resumen-sprint-N.md` o similar).

## Documentos útiles

- **Sprint 2:** [sprint-2/api-contract.md](sprint-2/api-contract.md) — contrato de API (adaptar entidades a turnos y agendas).
- **Sprint 4:** [sprint-4/deploy-checklist.md](sprint-4/deploy-checklist.md) — checklist antes de publicar.
- [como-ejecutar.md](como-ejecutar.md): quickstart backend y frontends.
- [errores-comunes.md](errores-comunes.md): índice con enlaces por sprint.
- [convencional-commits.md](convencional-commits.md): formato de commits y hooks.

## Taller docente

Guías para la demo en aula y GitHub Classroom: [taller/README.md](taller/README.md).
