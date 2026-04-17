# GitHub Classroom y repositorio plantilla

Este documento es la **checklist docente** para publicar el demo y crear la tarea que verán los alumnos.

## 1. Publicar este repositorio como plantilla

1. Crear un repositorio vacío en la **organización de la cátedra** (recomendado) o en una cuenta dedicada, por ejemplo `ucse-prog-ii/demo-proyecto-integrador`.
2. Subir el contenido de esta carpeta (`demo-proyecto-integrador`) con `git push` desde el entorno local.
3. En GitHub: **Settings** → **General** → marcar **Template repository** y guardar.
4. (Opcional) Añadir descripción: “Plantilla demo — TurniMed — Programación II”.

Los alumnos **no** reciben el template crudo: reciben una **copia** generada por GitHub Classroom a partir del template.

## 2. GitHub Classroom: crear la asignación

1. Ir a [https://classroom.github.com](https://classroom.github.com) con una cuenta que administre la aula.
2. Elegir la **classroom** de Programación II (o crear una “Prog II — Demo docentes” para ensayar).
3. **New assignment** → tipo **Individual** o **Group** según cómo cursen el integrador (el integrador real suele ser **grupal**).
4. En **Add a starter code from a template repository**, seleccionar el repo marcado como template del paso anterior.
5. Configurar visibilidad de los repos alumno (**private** recomendado si la org lo permite).
6. Generar el **invitation link** y guardarlo: lo usarán docentes (ensayo) y luego alumnos.

## 3. Equipo entre docentes (ensayo)

1. Crear un **equipo de prueba** con las cuentas GitHub de los tres profesores (si la asignación es grupal, invitar a un único grupo “Equipo Docente”).
2. Cada docente **acepta** la invitación de Classroom y verifica que tiene acceso al repo generado.
3. Designar **un** repo de prueba como “canónico” para la demo en vivo (evita que cada uno muestre URLs distintas sin consenso).

## 4. Qué NO hace Classroom por vos

GitHub Classroom **no** configura automáticamente:

- GitHub Projects ni columnas del tablero.
- Labels estándar (ver [.github/labels.md](../../.github/labels.md)).
- Milestones de Sprint 0 a 4.
- Branch protection rules.

Eso debe quedar explícito en el enunciado o demostrarse en el taller (ver [guion-demostracion-tres-docentes.md](guion-demostracion-tres-docentes.md)).

## 5. Checklist post-creación (alumnos)

- [ ] Todos los integrantes aparecen en **Settings → Collaborators** (o membresía de equipo) del repo generado.
- [ ] `README.md` actualizado con nombre del equipo y links (tablero, brief).
- [ ] Tablero creado y enlazado desde el README.
- [ ] Milestones con fechas.
- [ ] Primer issue de Sprint 0 o 1 creado desde template de Historia de Usuario.

## 6. Separación demo vs plantilla oficial de cursada

Si la plantilla “oficial” del año es otro repositorio (`proyecto-integrador-2026`), aclarar en clase:

- El **demo TurniMed** sirve para **metodología y herramientas**.
- El **proyecto real** puede mantener el enunciado y dominio del año (por ejemplo comercio local), reutilizando el **mismo flujo** de issues, PRs y sprints.
