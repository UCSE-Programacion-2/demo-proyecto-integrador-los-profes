# Sprint 0 — Relevamiento de contexto (TurniMed)

## Objetivo

Dejar documentado el **punto de partida** del producto: contexto del centro municipal de salud (modelo para el caso **TurniMed**), necesidades detectadas y material visual (referencias y logo) para que el equipo diseñe y construya con criterios claros.

En el **repositorio demo** no se exige un relevamiento de campo con datos sensibles: se usa un **centro modelo ficticio** o referencias públicas (sitio web genérico de un centro similar, **sin** fotografiar pacientes ni documentos reales).

## Qué tenés que entregar en esta carpeta

1. `relevamiento.md`
   - Resumen del contexto: qué ofrece el centro, público atendido, modalidad de turnos.
   - Problemas o necesidades alineados al [Product Brief](../product-brief.md) (2 a 5).
   - Qué aspectos del mundo real impactan en la app (turnos, especialidades, cancelaciones, métricas, etc.).

2. `fotos/` (o `referencias-visuales/`)
   - Mínimo 5 imágenes representativas del **entorno tipo** (sala de espera genérica, cartelería de turnos, recepción) usando **bancos de imágenes con licencia** o material provisto por la cátedra.
   - En `relevamiento.md`, indicá qué aporta cada grupo de imágenes.

3. `logo/`
   - Logo de **TurniMed Municipal** (propuesta del equipo: SVG/PNG) con breve justificación de colores y tipografía.

4. (Opcional) `extras/`
   - Paleta aproximada (HEX).
   - Capturas de referencias de UX (otras apps de turnos, sin copiar marca registrada de terceros).

## Errores comunes de esta etapa

Ver **[errores-comunes.md](./errores-comunes.md)** (GitHub Classroom, README, tablero, milestones).

## Checklist

- [ ] `relevamiento.md` con resumen y decisiones iniciales.
- [ ] Imágenes de referencia ordenadas y citadas (licencia o origen).
- [ ] Logo o propuesta con justificación breve.
- [ ] Queda claro cómo el contexto se conecta con las épicas del brief.

## Criterio de corrección

Se evalúa la claridad del documento, la evidencia visual y que el relevamiento **se traduzca** en decisiones para el Sprint 1.

---

## Viabilidad del caso (demo y cursada)

Para **TurniMed**, la viabilidad no depende de un comercio físico en Jujuy sino de:

1. **Coherencia con el brief:** las épicas del [product-brief.md](../product-brief.md) deben reflejarse en el relevamiento.
2. **Complejidad suficiente:** al menos 3 **especialidades** o tipos de consulta distintos en el relato del contexto.
3. **Variabilidad de datos:** turnos con fecha, hora, profesional, estado (reservado/cancelado/liberado).
4. **Rol administrativo:** procesos que luego se digitalicen vía CRUD (gestión de disponibilidad, especialidades, métricas).
5. **Activos visuales:** material gráfico suficiente para inspirar UI (logo + referencias).

## Configuración del repositorio y README (obligatorio)

El `README.md` raíz debe incluir:

1. **Nombre del equipo**
2. **Integrantes** con link a GitHub
3. **Ficha del producto / cliente modelo:**
   - Nombre: **TurniMed Municipal** (o variante acordada con la cátedra)
   - Dominio: salud pública municipal / turnos programados
   - Enlace al [Product Brief](../product-brief.md) y al **GitHub Projects**
4. **Tablero:** link directo al proyecto en GitHub Projects

## Entregables formales del Sprint 0

1. Aceptación del repo en **GitHub Classroom** (todo el equipo en el repo oficial).
2. `README.md` en `main` con la información anterior.
3. Tablero creado. La cátedra recomienda columnas alineadas al manual ágil: ver [docs/taller/tablero-y-automatizacion.md](../taller/tablero-y-automatizacion.md) y el mapeo con la vista mínima de 4 columnas si la usan los alumnos.
4. **Milestones** con fechas de los sprints siguientes.
5. (Recomendado) Instalar hooks de **Conventional Commits:** `node scripts/install-git-hooks.mjs`
