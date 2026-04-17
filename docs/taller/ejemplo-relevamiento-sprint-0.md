# Ejemplo de `relevamiento.md` — Sprint 0 (TurniMed, centro modelo)

Los equipos deben **adaptar** y reemplazar por su propia redacción. Este texto sirve para la **demo docente** o como partida si el taller es corto.

---

## Resumen del contexto

**Nombre ficticio del centro:** Centro de Salud Municipal Modelo “Norte”.  
**Público:** familias del barrio que solicitan turnos para consultas ambulatorias (clínica médica, pediatría, traumatología).  
**Modalidad actual:** turno por ventanilla y agenda en planilla; filas en picos matutinos.

## Necesidades detectadas (vinculadas al brief)

1. **Saturación de ventanilla:** los vecinos pierden tiempo en cola para operaciones que podrían resolverse en línea (alineado a “Saturación de canales físicos” del brief).
2. **Poca visibilidad de demanda:** la dirección no tiene gráficos en tiempo real de especialidades más solicitadas (brief: “Falta de visibilidad de datos”).
3. **Cancelaciones y huecos:** cuando un paciente no asiste, la franja no se reasigna rápido (brief: “Capacidad ociosa por ausentismo”).

## Impacto en la app

- Pantalla de **búsqueda** por especialidad y fecha.
- **Confirmación** y listado “mis turnos” con **cancelación** que libera la franja.
- **Panel admin** con KPIs simples (aunque sea mock en Sprint 1).
- **Registro de paciente** para trazabilidad sin exponer datos sensibles en el repo de práctica.

## Referencias visuales (`fotos/`)

- `sala-espera-01.jpg`: referencia genérica de sala de espera (banco de imágenes con licencia).
- `cartel-turnos.jpg`: señalética de “tome turno” (genérica).
- `recepcion.jpg`: mostrador de recepción sin personas identificables.

Indicar en cada pie de foto el **origen/licencia** (por ejemplo Unsplash + nombre del autor).

## Logo (`logo/`)

Propuesta **TurniMed Municipal:** tipografía sans legible, color primario verde/teal asociado a salud pública, ícono simple de calendario + cruz municipal. Justificar en dos líneas en `logo/README.txt` si se desea.
