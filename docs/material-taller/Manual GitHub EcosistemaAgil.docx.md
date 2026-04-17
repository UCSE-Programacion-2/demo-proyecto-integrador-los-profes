**GitHub como Ecosistema Ágil**

**Manual práctico**

*Curso-Taller: Desarrollo Ágil con IA*

*Cátedra Programación II*

*Ingeniería en Informática*  

*UCSE-DASS*

| ¿Para qué sirve este manual? |
| :---- |
| Este manual te acompaña para configurar GitHub como entorno de trabajo Scrum completo y entender el flujo de trabajo desde que existe una idea hasta que el código llega a producción. |
| Proyecto de referencia: Sistema de Turnos para un Centro de Salud Municipal. |

Contenido  
[1\. El tablero Scrum en GitHub Projects	3](#1.-el-tablero-scrum-en-github-projects)

[2\. Labels — etiquetas para clasificar el trabajo	5](#2.-labels-—-etiquetas-para-clasificar-el-trabajo)

[3\. Milestones — los Sprints en GitHub	6](#3.-milestones-—-los-sprints-en-github)

[4\. El template de Issue — la Historia de Usuario	7](#4.-el-template-de-issue-—-la-historia-de-usuario)

[5\. Épicas e Historias de Usuario — la jerarquía	9](#5.-épicas-e-historias-de-usuario-—-la-jerarquía)

[6\. El tablero en acción — flujo de un Issue	11](#6.-el-tablero-en-acción-—-flujo-de-un-issue)

[7\. Branches y commits — convenciones del equipo	12](#7.-branches-y-commits-—-convenciones-del-equipo)

[8\. Pull Requests — cerrar el ciclo	14](#8.-pull-requests-—-cerrar-el-ciclo)

[9\. El flujo completo de punta a punta	17](#9.-el-flujo-completo-de-punta-a-punta)

[10\. Referencia rápida	17](#10.-referencia-rápida)

# **1\. El tablero Scrum en GitHub Projects** {#1.-el-tablero-scrum-en-github-projects}

GitHub Projects es el tablero donde el equipo visualiza el estado del trabajo en cada Sprint. Se configura una sola vez al inicio del proyecto.

**Cómo crear el tablero**

| 1 | Ir al repositorio → pestaña Projects → New project |
| ----- | :---- |
|  | Elegir el template 'Board' (tablero tipo Kanban). |
|  | Darle un nombre: 'Sistema de Turnos — Scrum Board'. |

| 2 | Borrar las columnas que trae por defecto y crear estas 5 |
| ----- | :---- |
|  | Las columnas representan los estados posibles de una Historia de Usuario: |

| Columna | Qué contiene | Quién mueve la card |
| :---- | :---- | :---- |
| 📋 Product Backlog | Todo lo que no entró al Sprint todavía. | Product Owner (define el orden) |
| 🎯 Sprint Backlog | Lo que el equipo se comprometió en el Planning. | Developers (en el Planning) |
| 🔨 In Progress | En desarrollo activo. Máximo 1-2 por persona. | Developer (cuando empieza) |
| 👀 In Review | PR abierto, esperando revisión. | Developer (cuando abre el PR) |
| ✅ Done | Mergeado y cerrado. Cumple el DoD. | GitHub (automático al cerrar el Issue) |

| 💡 Tip |
| :---- |
| El pasaje entre columnas es manual, excepto Done que es automático cuando se cierra el Issue con Closes \#N en el PR. |

**Configurar el movimiento automático a Done**

Por defecto el tablero no mueve las cards automáticamente. Hay que activarlo una sola vez:

| 1 | Ir al tablero → clic en los tres puntos ... arriba a la derecha → Workflows |
| :---: | :---- |

| 2 | Buscar el workflow Item closed → activarlo |
| ----- | :---- |
|  | Configurar: cuando un Issue se cierra → mover a la columna Done. |

| 3 | Guardar |
| ----- | :---- |
|  | A partir de este momento, cuando un PR con Closes \#N se mergea: |
|  |   1\. El Issue se cierra automáticamente. |
|  |   2\. La card pasa a la columna Done automáticamente. |

| ⚠️  Dos condiciones para que Done sea automático |
| :---- |
| Condición 1: el PR debe tener 'Closes \#N' en el CUERPO (no en el título). |
| Condición 2: el merge debe hacerse sobre el branch principal del repositorio (main). |
|   |
| Si ambas se cumplen y el workflow está activado, la card pasa a Done sola. |
| Si la card no se mueve, verificar estas dos condiciones primero. |

# **2\. Labels — etiquetas para clasificar el trabajo** {#2.-labels-—-etiquetas-para-clasificar-el-trabajo}

Los labels permiten filtrar y priorizar el backlog de un vistazo. Se crean una sola vez y se reusan en todos los Issues del proyecto.

**Cómo crear labels**

| 1 | Ir a la pestaña Issues → botón Labels (arriba a la derecha) |
| :---: | :---- |

| 2 | Clic en New label → completar nombre, color y descripción → Create label |
| ----- | :---- |
|  | Repetir para cada label de la lista. |

**Labels recomendados para el proyecto**

**Tipo de trabajo**

| Label | Color | Cuándo usarlo |
| :---- | :---- | :---- |
| epic | \#1B3A6B (azul oscuro) | Issues que representan una Épica completa |
| feature | \#1A6B3A (verde) | Historia de Usuario — nueva funcionalidad |
| bug | \#8B1A1A (rojo oscuro) | Defecto reportado o detectado |
| tech-debt | \#B8690A (naranja) | Deuda técnica o refactor necesario |

**Prioridad**

| Label | Color | Significado |
| :---- | :---- | :---- |
| P0 — crítico | \#CC0000 (rojo) | Bloquea el Sprint Goal. Se resuelve primero. |
| P1 — alto | \#FF6600 (naranja oscuro) | Importante pero no bloqueante. |
| P2 — medio | \#CCAA00 (amarillo) | Backlog normal, entra según capacidad. |

**Tamaño estimado**

| Label | Color | Significa |
| :---- | :---- | :---- |
| S — small | \#90EE90 (verde claro) | Menos de 1 día de trabajo |
| M — medium | \#87CEEB (azul claro) | 1 a 2 días de trabajo |
| L — large | \#9370DB (violeta) | 3 o más días — considerar dividir la historia |

# **3\. Milestones — los Sprints en GitHub** {#3.-milestones-—-los-sprints-en-github}

Un Milestone es un contenedor que agrupa Issues bajo un nombre y una fecha límite. En Scrum lo usamos para representar un Sprint.

| GitHub | Scrum |
| :---- | :---- |
| Milestone 'Sprint 1' | Sprint 1 |
| Fecha de cierre del Milestone | Último día del Sprint |
| Issues asignados al Milestone | Sprint Backlog |
| Barra de progreso del Milestone | Burn-down simplificado |

**Cómo crear un Milestone**

| 1 | Ir a Issues → botón Milestones (arriba a la derecha) |
| :---: | :---- |

| 2 | Clic en New Milestone → completar los campos |
| ----- | :---- |
|  | Título: Sprint 1 |
|  | Fecha de vencimiento: último día del Sprint |
|  | Descripción: Sprint Goal — 'Al final del Sprint 1, un paciente puede registrarse y confirmar su primer turno.' |

| 3 | Repetir para Sprint 2 |
| ----- | :---- |
|  | Título: Sprint 2 |
|  | Fecha de vencimiento: último día del Sprint 2 |
|  | Descripción: Sprint Goal del Sprint 2 |

| 💡 ¿Qué va en un Milestone y qué no? |
| :---- |
| Sí van al Milestone: Historias de Usuario, bugs, tasks técnicas. |
| No van al Milestone: Épicas (una épica puede abarcar varios Sprints). |

# **4\. El template de Issue — la Historia de Usuario** {#4.-el-template-de-issue-—-la-historia-de-usuario}

El template garantiza que todas las historias tengan la misma estructura: título, criterios de aceptación verificables y el Definition of Done del equipo. Se crea una vez y GitHub lo ofrece automáticamente al crear nuevos Issues.

**Cómo crear el template**

| 1 | Ir a la pestaña Code → Add file → Create new file |
| :---: | :---- |

| 2 | En el campo del nombre escribir exactamente esto: |
| ----- | :---- |
|  | .github/ISSUE\_TEMPLATE/historia-de-usuario.md |
|  |   |
|  | Cuando escribís la barra /, GitHub crea las carpetas automáticamente. |
|  | Vas a ver que .github/ e ISSUE\_TEMPLATE/ aparecen separadas mientras escribís. |

| 3 | Pegar este contenido en el editor |
| :---: | :---- |

\---

name: Historia de Usuario

about: Template para escribir historias de usuario con criterios de aceptación

title: 'HU-XX — '

labels: feature

\---

\#\# Historia de Usuario

Como \[paciente / profesional / administrativo\]

quiero \[funcionalidad concreta\]

para \[beneficio o valor real\].

\#\# Criterios de Aceptación

\- \[ \] Dado que... cuando... entonces...

\- \[ \] Dado que... cuando... entonces...

\#\# Notas técnicas

(Dependencias, restricciones, APIs involucradas.)

\#\# Definition of Done

\- \[ \] Código revisado (mínimo 1 aprobación en el PR)

\- \[ \] Tests unitarios pasando en CI

\- \[ \] PR mergeado con referencia: Closes \#N

\- \[ \] Issue cerrado automáticamente

| 4 | Hacer clic en Commit changes → confirmar |
| ----- | :---- |
|  | A partir de este momento, cada vez que alguien haga clic en New issue, |
|  | GitHub va a ofrecer el template 'Historia de Usuario' para seleccionar. |

| 💡 El encabezado YAML es obligatorio |
| :---- |
| Las líneas entre \--- al inicio son el encabezado YAML. Sin ellas, GitHub no reconoce el archivo como template y no lo muestra al crear un Issue. Si el template no aparece, verificar que el archivo empiece exactamente con \---. |

# **5\. Épicas e Historias de Usuario — la jerarquía** {#5.-épicas-e-historias-de-usuario-—-la-jerarquía}

En GitHub representamos dos niveles de trabajo:

| Tipo | Qué es | Ejemplo del proyecto |
| :---- | :---- | :---- |
| Épica | Agrupa un conjunto de Historias de Usuario relacionadas. Abarca varios Sprints. | \[ÉPICA\] E1 — Gestión de Pacientes |
| Historia de Usuario | La unidad de trabajo que entra al Sprint. Se puede completar en pocos días. | HU-01 — Registro de paciente con email y contraseña |

**Cómo crear una Épica**

| 1 | Ir a Issues → New issue → Open a blank issue (sin template) |
| ----- | :---- |
|  | La épica no usa el template de Historia de Usuario. |

| 2 | Completar el Issue |
| ----- | :---- |
|  | Título: \[ÉPICA\] E1 — Gestión de Pacientes |
|  | Cuerpo: descripción breve de qué agrupa esta épica. |
|  | Label: epic |
|  | Milestone: ninguno (la épica puede abarcar varios Sprints). |

| 3 | Submit new issue |
| :---: | :---- |

**Cómo crear una Historia de Usuario**

| 1 | Ir a Issues → New issue → Get started (en el template Historia de Usuario) |
| :---: | :---- |

| 2 | Completar el Issue usando el template |
| :---: | :---- |

Título: HU-01 — Registro de paciente con email y contraseña

 

Historia:

Como paciente quiero registrarme con mi email y contraseña

para poder acceder al sistema y sacar turnos.

 

CA 1: Dado que completo el formulario con email válido y contraseña de al menos

8 caracteres, cuando hago clic en 'Crear cuenta', entonces recibo un email de

verificación y se muestra 'Revisá tu email para activar tu cuenta'.

 

CA 2: Dado que intento registrarme con un email ya existente, cuando hago clic

en 'Crear cuenta', entonces veo el mensaje 'Ya existe una cuenta con ese email'.

 

Notas técnicas: Épica padre: \#1

| 3 | Asignar en el panel derecho |
| ----- | :---- |
|  | Labels: feature, P0 — crítico, M — medium |
|  | Milestone: Sprint 1 |
|  | Assignees: el Developer responsable |

| 4 | Submit new issue |
| :---: | :---- |

**Vincular la Historia a la Épica — Sub-issues**

| 1 | Abrir el Issue de la Épica (ej: \#1 — E1 Gestión de Pacientes) |
| :---: | :---- |

| 2 | Buscar la sección Sub-issues → Add sub-issue |
| ----- | :---- |
|  | Podés agregar un Issue existente (buscar por \#número) o crear uno nuevo directamente. |
|  | GitHub muestra una barra de progreso automática: cuántas historias hijas están cerradas. |

| 💡 La jerarquía completa del proyecto |
| :---- |
| Épica E1 — Gestión de Pacientes |
|    └── HU-01 — Registro de paciente          (Sprint 1\) |
|    └── HU-02 — Login de paciente              (Sprint 1\) |
|    └── HU-03 — Recuperar contraseña           (Sprint 2\) |
|   |
| Épica E2 — Búsqueda y reserva de turnos |
|    └── HU-04 — Buscar turnos por especialidad (Sprint 1\) |
|    └── HU-05 — Confirmar turno                (Sprint 1\) |
|    └── HU-06 — Cancelar turno                 (Sprint 2\) |

# **6\. El tablero en acción — flujo de un Issue** {#6.-el-tablero-en-acción-—-flujo-de-un-issue}

Una vez creados los Issues, se agregan al tablero y se mueven entre columnas a medida que avanza el trabajo.

**Agregar un Issue al tablero**

| 1 | Ir a la pestaña Projects → abrir el tablero Scrum |
| :---: | :---- |

| 2 | En la columna Product Backlog → Add item → escribir \# → buscar el Issue por número o nombre → seleccionarlo |
| ----- | :---- |
|  | El Issue aparece como una card en la columna. |
|  |   |
|  | Importante: Add item NO crea un Issue nuevo. Solo agrega al tablero un Issue que ya existe. |

**Mover las cards entre columnas**

| Cuándo | Quién mueve | De → A |
| :---- | :---- | :---- |
| Sprint Planning: el equipo se compromete con la historia | Developers | Product Backlog → Sprint Backlog |
| El Developer empieza a trabajar en la historia | Developer | Sprint Backlog → In Progress |
| El Developer abre el Pull Request | Developer | In Progress → In Review |
| El PR se mergea con Closes \#N | GitHub (automático) | In Review → Done |

| 💡 WIP Limit — máximo de cards In Progress por persona |
| :---- |
| Una buena práctica es limitarse a 1 o 2 historias In Progress por persona al mismo tiempo. |
| Tener 5 historias en In Progress simultáneamente generalmente significa que ninguna avanza bien. |
| Terminar una antes de empezar otra es más eficiente que dividir el foco. |

# **7\. Branches y commits — convenciones del equipo** {#7.-branches-y-commits-—-convenciones-del-equipo}

Las convenciones de nombres hacen que el historial del proyecto sea legible. En seis meses, cuando necesiten entender por qué se hizo un cambio, los nombres de branches y commits son la primera línea de investigación.

**Nombres de branches**

| Formato |
| :---- |
| tipo/US-\[número\]-\[descripción-corta-en-kebab-case\] |

| Tipo | Cuándo usarlo | Ejemplo |
| :---- | :---- | :---- |
| feature/ | Nueva funcionalidad | feature/US-01-registro-paciente |
| bugfix/ | Corrección de bug | bugfix/US-02-login-token-expiry |
| refactor/ | Mejora sin cambiar comportamiento | refactor/US-05-extraer-validaciones |
| docs/ | Documentación | docs/actualizar-readme-variables-entorno |

**Mensajes de commit — Conventional Commits**

| Formato |
| :---- |
| tipo: descripción breve en imperativo (qué hace este commit, no qué hiciste vos) |

| Tipo | Cuándo usarlo | Ejemplo |
| :---- | :---- | :---- |
| feat: | Nueva funcionalidad | feat: agregar validación de email único en registro |
| fix: | Corrección de bug | fix: corregir cálculo de tiempo en cancelación de turno |
| test: | Agregar o corregir tests | test: agregar casos borde para cancelación de turno |
| refactor: | Mejora sin cambiar comportamiento | refactor: extraer lógica de validación a servicio |
| docs: | Documentación | docs: agregar README con instrucciones de instalación |
| chore: | Mantenimiento, dependencias | chore: actualizar dependencias de Jest a 29.7 |

**Ejemplo completo — HU-01 Registro de paciente**

| 1 | Crear el branch desde main |
| ----- | :---- |
| git checkout main |  |
| git pull origin main |  |
| git checkout \-b feature/US-01-registro-paciente |  |

| 2 | Trabajar y hacer commits pequeños y descriptivos |
| ----- | :---- |
|  | Un commit por cada pieza de trabajo significativa. No esperar a 'terminar todo' para commitear. |
| git add src/models/Paciente.js |  |
| git commit \-m "feat: agregar modelo Paciente con validación de email único" |  |
|  |  |
| git add src/controllers/pacientesController.js |  |
| git commit \-m "feat: implementar endpoint POST /pacientes/registro" |  |
|  |  |
| git add tests/pacientes.test.js |  |
| git commit \-m "test: agregar tests de registro con happy path y email duplicado" |  |

| 3 | Subir el branch a GitHub |
| ----- | :---- |
| git push origin feature/US-01-registro-paciente |  |

# **8\. Pull Requests — cerrar el ciclo** {#8.-pull-requests-—-cerrar-el-ciclo}

El Pull Request es el mecanismo que conecta el código con el Issue. Cuando el PR se mergea con Closes \#N, el Issue se cierra automáticamente y la card pasa a Done en el tablero.

**Cómo abrir el PR**

| 1 | Después del git push, ir al repositorio en GitHub |
| ----- | :---- |
|  | Va a aparecer un banner amarillo: 'feature/US-01-registro-paciente had recent pushes'. |
|  | Hacer clic en Compare & pull request. |

| 2 | Completar el título y la descripción del PR |
| ----- | :---- |
|  | Título: feat: implementar registro de paciente (\#1) Descripción (copiar esta estructura): \#\# Qué se hizo Se implementó el registro de paciente con validación de email único y envío de email de verificación. \#\# Por qué Resuelve HU-01: el paciente puede crear su cuenta en el sistema. Closes \#2 \#\# Cómo probar 1\. npx jest tests/pacientes.test.js \--verbose 2\. POST /pacientes/registro con { email, password } 3\. Verificar que llega el email de verificación \#\# Notas para el reviewer La validación de email único está en el modelo (índice único en MongoDB). |

| ⚠️  La línea más importante del PR: Closes \#2 |
| :---- |
| Cuando el PR se mergea, GitHub lee esa línea y cierra automáticamente el Issue \#2. |
| El Issue pasa a Closed y la card en el tablero pasa a Done. |
| Sin esa línea, el Issue queda abierto aunque el código esté mergeado. |

| 3 | Asignar reviewers en el panel derecho |
| ----- | :---- |
|  | Asignar al menos 1 compañero como reviewer. Mínimo 1 aprobación antes de mergear. |

| 4 | El reviewer hace el code review |
| ----- | :---- |
|  | El reviewer lee el código, prueba los cambios y deja comentarios. |
|  | Si todo está bien: clic en Review changes → Approve. |
|  | Si hay cambios: clic en Request changes → dejar comentarios específicos. |

| 5 | Mergear el PR |
| ----- | :---- |
|  | Con al menos 1 aprobación: clic en Merge pull request → Confirm merge. |
|  | GitHub cierra automáticamente el Issue referenciado con Closes \#N. |
|  | La card en el tablero pasa a Done. |
|  | Borrar el branch después del merge (GitHub lo propone automáticamente). |

**Template de Pull Request**

Igual que el template de Issue, podés crear un template de PR para que la descripción se cargue automáticamente cada vez que alguien abre un PR.

| 1 | Ir a Code → Add file → Create new file |
| :---: | :---- |

| 2 | En el nombre escribir exactamente: |
| ----- | :---- |
|  | .github/PULL\_REQUEST\_TEMPLATE.md |
|  |   |
|  | GitHub crea la carpeta automáticamente al escribir la barra /. |

| 3 | Pegar este contenido y hacer Commit changes |
| :---: | :---- |

\#\# Qué se hizo

(Resumen del cambio en 2-3 oraciones)

\#\# Por qué

(User Story o Issue relacionado)

Closes \#

\#\# Cómo probar

1\.

2\.

3\.

\#\# Uso de IA

(Qué generó la IA y qué corregiste manualmente. Si no usaste IA: No aplica.)

\#\# Notas para el reviewer

(Algo a prestar atención, deuda técnica pendiente, decisiones de diseño tomadas.)

\#\# Definition of Done

\- \[ \] Tests pasando

\- \[ \] Código revisado por al menos 1 persona

\- \[ \] Issue cerrado con Closes \#N

| 💡 A partir de este momento |
| :---- |
| Cada vez que alguien abra un PR en el repositorio, la descripción va a estar pre-cargada con esta estructura. |
| Solo hay que completar los campos. No hay que recordar el formato de memoria. |

**El vínculo que queda en GitHub**

| Trazabilidad completa del trabajo |
| :---- |
| Issue \#2 — HU-01 Registro de paciente |
|    └── PR \#1 — feat: implementar registro de paciente |
|          └── commit: feat: agregar modelo Paciente |
|          └── commit: feat: implementar endpoint POST /pacientes/registro |
|          └── commit: test: agregar tests de registro |
|   |
| Desde el Issue podés ver el PR vinculado. |
| Desde el PR podés ver los commits y el Issue que cierra. |
| Todo trazable desde la idea hasta el código en producción. |

# 

# **9\. El flujo completo de punta a punta** {#9.-el-flujo-completo-de-punta-a-punta}

Este es el ciclo completo que se repite en cada Historia de Usuario de cada Sprint:

| \# | Etapa | Qué hacés |
| :---: | :---- | :---- |
| **1** | **Crear el Issue** | Issues → New issue → template Historia de Usuario → completar título, historia, CAs, labels, milestone → Submit. |
| **2** | **Agregar al tablero** | Projects → tablero → Add item → \# → seleccionar el Issue. Colocarlo en Product Backlog o Sprint Backlog. |
| **3** | **Crear el branch** | git checkout main && git pull && git checkout \-b feature/US-XX-nombre |
| **4** | **Desarrollar y commitear** | Commits pequeños y descriptivos: feat:, fix:, test:, etc. Uno por cada pieza de trabajo significativa. |
| **5** | **Mover la card** | Pasar la card del Issue de Sprint Backlog → In Progress en el tablero. |
| **6** | **Abrir el PR** | git push → GitHub → Compare & pull request → completar descripción → Closes \#N → asignar reviewer. |
| **7** | **Mover la card** | Pasar la card de In Progress → In Review en el tablero. |
| **8** | **Code review** | El reviewer aprueba o solicita cambios. Mínimo 1 aprobación. |
| **9** | **Mergear** | Merge pull request → el Issue se cierra automáticamente → la card pasa a Done. |
| **10** | **Limpiar** | Borrar el branch mergeado. Verificar en el Milestone que el progreso subió. |

# **10\. Referencia rápida** {#10.-referencia-rápida}

**Comandos git más usados**

\# Crear y cambiar a un branch nuevo

git checkout \-b feature/US-XX-nombre

\# Ver en qué branch estás

git branch

\# Agregar archivos al commit

git add nombre-del-archivo.js

git add .                          \# agrega todos los cambios

\# Hacer el commit

git commit \-m "feat: descripción del cambio"

\# Subir el branch a GitHub

git push origin feature/US-XX-nombre

\# Volver a main y actualizar

git checkout main

git pull origin main

**Checklist antes de abrir un PR**

* El branch está actualizado con main: git pull origin main

* Los commits tienen mensajes descriptivos en formato Conventional Commits

* La descripción del PR tiene las 4 secciones: Qué, Por qué, Cómo probar, Notas

* La descripción incluye Closes \#N con el número del Issue correspondiente

* Hay al menos 1 reviewer asignado

**Errores frecuentes**

| Error | Causa | Solución |
| :---- | :---- | :---- |
| El Issue no se cierra al mergear | Falta 'Closes \#N' en el cuerpo del PR (no en el título). | Editar la descripción del PR y agregar 'Closes \#N' en el cuerpo antes de mergear. |
| El template no aparece al crear un Issue | Falta el encabezado YAML (---) al inicio del archivo. | Editar el archivo .github/ISSUE\_TEMPLATE/historia-de-usuario.md y asegurarse de que empiece con \---. |
| La card no pasa a Done automáticamente | Dos causas posibles: 1\. El workflow 'Item closed' no está activado. 2\. Falta 'Closes \#N' en el cuerpo del PR o el merge no fue sobre main. | Activar el workflow: tablero → ... → Workflows → Item closed → activar. Verificar que el PR tiene 'Closes \#N' en el cuerpo y que el merge fue sobre main. |
| Copilot no sugiere nada útil | El comentario o contexto del archivo es insuficiente. | Escribir el JSDoc completo antes de escribir código: qué hace la función, parámetros, retorno y casos borde. |

| ¿Dudas? Recursos oficiales |
| :---- |
| Documentación de GitHub Projects: docs.github.com/en/issues/planning-and-tracking-with-projects |
| Conventional Commits: conventionalcommits.org |
| GitHub Student Pack (Copilot gratuito): education.github.com/pack |

