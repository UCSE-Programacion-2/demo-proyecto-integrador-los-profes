

| MÓDULO 2  —  Ingeniería en Informática IA como Copiloto del Equipo |
| :---- |

**Curso-Taller: Desarrollo Ágil con IA**

*Maximizando el Potencial de Scrum con Herramientas Inteligentes*

**Pre requisito:** Haber completado el Módulo 1 y la Actividad Asincrónica 1  
**Herramientas:** GitHub Copilot, VS Code, ChatGPT / Claude, GitHub

## **Objetivos del módulo**

Al finalizar este módulo, los estudiantes serán capaces de integrar la IA en todas las dimensiones de un equipo Scrum: desde la asistencia técnica individual (como Developers) hasta la facilitación de ceremonias y la adaptación del rol humano en un entorno con agentes autónomos.

| 2.1 | La IA como Copiloto en cada Rol de Scrum |
| :---: | :---- |

Antes de abrir VS Code, necesitamos un modelo mental claro sobre cómo funciona la relación entre un profesional de software y la IA. La metáfora más precisa que propone el mercado en 2025-2026 no es 'la IA como herramienta' ni 'la IA como jefe': es la IA como compañero de equipo junior, muy capaz en tareas específicas, pero que necesita guía, supervisión y corrección constante.

| CONCEPTO CLAVE  —  El modelo mental: IA como 'junior teammate' Scrum.org llama a este rol cybernetic teammate: un colaborador que puede cumplir algunos roles sociales y técnicos de un humano, pero que no tiene contexto de negocio, no toma accountability del resultado y comete errores con la misma seguridad con que escribe respuestas correctas. Tratar a la IA como un junior al que hay que guiar, criticar y corregir es la estrategia más efectiva para no quemarse ni depender ciegamente de sus outputs. |
| :---- |

### **Ciclo de colaboración humano-IA**

Todo trabajo asistido por IA en un equipo Scrum sigue este ciclo. Saltear pasos no ahorra tiempo: genera deuda técnica, bugs no detectados y perdida de comprensión del propio código.

| Paso | Quien lidera | Que ocurre |
| :---- | :---- | :---- |
| 1\. Contexto | Humano | El profesional define la tarea, el scope y las restricciones. La IA no sabe que existe el Sprint Goal si no se lo contamos. |
| 2\. Generación | IA | La IA produce un borrador: código, tests, descripción, priorización, etc. |
| 3\. Revisión critica | Humano | El profesional evalúa el output: es correcto? es apropiado para este contexto? sigue las convenciones del equipo? |
| 4\. Ajuste | Humano \+ IA | Se corrige, se refina con un segundo prompt, o se reescribe manualmente si el output no sirve. |
| 5\. Validación | Humano \+ CI | El código pasa por tests, code review y pipeline. La IA no puede hacer este paso por nosotros. |
| 6\. Aprendizaje | Humano | El profesional entiende lo que produjo, aunque lo haya generado la IA. Si no lo entiende, no puede mantenerlo. |

### **IA como asistente del Product Owner**

El Product Owner  no es el que escribe todas las historias: es el que tiene la visión y el criterio para decidir qué construir. La IA le da velocidad de análisis y generación; el PO le da contexto, estrategia y la capacidad de decir NO.

| Responsabilidad del PO | Que puede hacer la IA | Lo que sigue siendo humano |
| :---- | :---- | :---- |
| Gestionar el Product Backlog | Detectar duplicados, dependencias, historias ambiguas; sugerir criterios de aceptación; ordenar por valor estimado basado en datos | Decisión final de prioridad; negociación con stakeholders; visión del producto |
| Refinar User Stories | Generar borradores de historias a partir de ideas vagas; sugerir criterios Given/When/Then; descomponer Épicas en historias | Validar que la historia refleja la necesidad real del usuario; ajustar el lenguaje al contexto del negocio |
| Analizar feedback de usuarios | Procesar grandes volúmenes de comentarios, reseñas y tickets; identificar puntos de dolor; sugerir features con mayor impacto | Interpretar el contexto emocional y cultural; decidir que feedback priorizar; hablar con usuarios reales |
| Análisis competitivo y de mercado | Resumir tendencias, comparar features de competidores, generar reportes de posicionamiento | Definir la estrategia de diferenciación; tomar decisiones de pivote o perseverancia |
| Preparar el Sprint Planning | Sugerir el Sprint Goal basado en el backlog y la velocidad histórica; estimar impacto de cada historia | Liderar la reunión, defender el objetivo ante el equipo, negociar el alcance |

### **IA como asistente del Scrum Master**

El Scrum Master usa la IA para liberar tiempo de tareas administrativas y enfocarse en lo que la IA no puede hacer: el coaching humano, la escucha activa y la facilitación de conversaciones difíciles.

| Responsabilidad del SM | Que puede hacer la IA | Lo que sigue siendo humano |
| :---- | :---- | :---- |
| Facilitar ceremonias | Sugerir dinámicas de retrospectiva, generar agendas, tomar notas automáticas y producir sumaries | Leer la sala, gestionar silencios, manejar conflictos, construir seguridad psicológica |
| Remover impedimentos | Identificar issues estancadas, detectar patrones de bloqueo en el historial del tablero, sugerir soluciones basadas en casos similares | Negociar con otras áreas, influir sin autoridad, sostener conversaciones incomodas |
| Monitorear el progreso | Analizar métricas de flujo (cycle time, lead time, WIP), detectar anomalías, predecir si el Sprint Goal esta en riesgo | Interpretar las causas humanas de los datos; decidir cómo intervenir |
| Mejorar practicas del equipo | Evaluar madurez agil del equipo, sugerir experimentos de mejora, generar reportes de retrospectivas anteriores | Adaptar las practicas al contexto y cultura del equipo especifico |
| Gestionar la dinámica del equipo | Analizar patrones de comunicación en canales digitales, detectar señales de sobrecarga o desmotivación | Conversaciones 1:1, contención emocional, desarrollo de confianza del equipo |

### **IA como asistente del Developer: el Agent Orchestrator**

El rol de Developer en equipos con IA es el que más está cambiando. El Developer ya no es solo quien escribe código: es quien orquesta agentes de IA, valida sus outputs y mantiene la accountability del resultado. Esta transición tiene un nombre en la industria: Agent Orchestrator.

| Responsabilidad del Developer | Que puede hacer la IA | Lo que sigue siendo humano |
| :---- | :---- | :---- |
| Escribir código de features | Generar implementaciones completas a partir de comentarios o especificaciones; completar boilerplate; sugerir patrones de diseño | Arquitectura del sistema; decisión de patrones; garantía de que el codigo generado es mantenerle y seguro |
| Testing | Generar tests unitarios; sugerir casos borde; crear datos de prueba sintéticos; detectar código sin cobertura | Decidir que probar; validar que los tests realmente verifican el comportamiento esperado; tests de integración complejos |
| Code review | Sugerir comentarios en PRs; detectar code smells comunes; verificar convenciones de estilo | Evaluar el diseño y la mantenibilidad; detectar problemas de lógica de negocio; decidir si el PR cumple el DoD |
| Documentación | Generar docstrings, READMEs, comentarios inline, diagramas de arquitectura en texto | Asegurar que la documentación refleja la intención real del código; mantenerla actualizada con cada cambio |
| Debugging | Analizar stack traces, sugerir causas probables, proponer fixes | Entender el contexto del bug en el sistema completo; decidir el fix correcto; prevenir regresiones |

| 2.2 | GitHub Copilot en el Editor |
| :---: | :---- |

GitHub Copilot no es magia: es un modelo de lenguaje entrenado con código público que predice el texto más probable dado el contexto de tu archivo. Eso explica por qué funciona bien con patrones comunes y falla en lógica de negocio específica. Entender esto es la base para usarlo con criterio.

| Modo de uso | Como se activa | Mejor para |
| :---- | :---- | :---- |
| Completado inline (ghost text) | Escribir código o comentario y esperar 1-2 segundos. Tab para aceptar, Esc para rechazar. | Boilerplate, patrones repetitivos, continuación de código en contexto |
| Copilot Chat (panel lateral) | Ctrl+Shift+I / Cmd+Shift+I en VS Code | Explicar código, debuggear, generar alternativas, preguntar sobre el proyecto |
| Inline Chat (en el editor) | Ctrl+I / Cmd+I sobre código seleccionado | Refactorizar, agregar tests a una función específica, reescribir con mejoras |
| Copilot en terminal | @terminal en el chat | Sugerir comandos, explicar errores de CLI, git commands |

### **Técnica central: Comment-Driven Development**

La técnica más efectiva para trabajar con Copilot no es esperar que 'adivine' lo que necesitas: es escribir el COMMENT PRIMERO, antes de escribir una sola línea de código. Esto obliga a pensar en la lógica antes de implementar y le da a Copilot el contexto necesario para generar algo útil.

| CONCEPTO CLAVE  —  Comment-Driven Development — el flujo 1\. Escribís el comentario describiendo QUE debe hacer la función, sus parámetros, lo que retorna y los casos borde importantes. 2\. Copilot sugiere una implementación completa basada en el comentario. 3\. Vos revisas críticamente: ¿es correcto? ¿es eficiente? ¿sigue las convenciones del proyecto? 4\. Aceptas, modificas o rechazas según el resultado. Nunca aceptar sin entender. 5\. Vas al paso 1 para la siguiente función o lógica. |
| :---- |

| ✏  EJEMPLO DE CODIGO  —  Ejemplo de Comment-Driven Development en JavaScript (Node.js / Express) JSDoc que escribe el Developer → Copilot genera la implementación: // js/validaciones.js /\*\*  \* Verifica si un estudiante puede inscribirse a un examen.  \* @param {Object}  datos                    \- Datos del formulario  \* @param {number}  datos.promedio            \- Promedio general (0 a 10\)  \* @param {boolean} datos.correlativaAprobada \- Aprobo la materia previa  \* @param {number}  datos.intentos            \- Intentos previos en esta materia  \* @returns {{ puede: boolean, mensaje: string }}  \* Condiciones (TODAS deben cumplirse):  \*   \- promedio \>= 4.0  \*   \- correlativaAprobada \=== true  \*   \- intentos \< 3  \* mensaje \= 'OK' si puede inscribirse, o la razon por la que no puede.  \*/ function validarInscripcion(datos) {   // Copilot sugerira la implementacion aqui } module.exports \= { validarInscripcion }; |
| :---- |

| ACTIVIDAD  —  Practica A: Comment-Driven Development (10 min) Abrir VS Code con el repositorio del proyecto de la materia. Elegir una función que necesiten implementar para el Sprint 1 o usar el ejemplo de canRegisterForExam. Escribir el JSDoc completo ANTES de escribir el cuerpo. Incluir: que hace, @param con tipos, @returns, casos borde. Dejar que Copilot sugiera la implementación. Tab para aceptar. Revisar críticamente: ¿el código hace lo que el comentario promete? ¿qué cambiarían? Pregunta de reflexión: Si el comentario era ambiguo, ¿la implementación de Copilot aclaro o amplifico la ambigüedad? |
| :---- |

| 2.3 | Tests y Calidad con GitHub Copilot |
| :---: | :---- |

La generación de tests es uno de los casos de uso más poderosos de Copilot, y también uno de los más peligrosos si se usa sin criterio. Copilot puede generar tests en segundos, pero un test que solo verifica lo que la IA ya género no tiene valor real. La habilidad critica es saber qué casos borde pedir y como verificar que los tests realmente atrapan bugs.

| CONCEPTO CLAVE  —  Por qué el testing con IA cambia el juego Antes de IA: escribir tests era una tarea adicional que muchos equipos postergaban por falta de tiempo. Con IA: generar una suite de tests básica toma minutos. Eso elimina la excusa del tiempo y sube el piso de calidad de todo el equipo. La trampa: Copilot genera tests que pasan con la implementación que el mismo género. Eso no es testing; es confirmación de lo que ya existe. El valor real está en los casos borde que vos pedis explícitamente. |
| :---- |

### **Como generar tests útiles con Copilot**

Hay dos formas principales de pedir tests a Copilot. La segunda es siempre más efectiva:

| Enfoque | Como hacerlo | Resultado típico |
| :---- | :---- | :---- |
| Directo (menos efectivo) | Seleccionar la función, Copilot Chat: 'generate unit tests' | Tests básicos del happy path. No cubre casos borde críticos. |
| Con casos borde (más efectivo) | Copilot Chat: 'generate unit tests incluyendo: \[lista de casos borde específicos\]' | Tests más completos. Fuerza a Copilot a cubrir los escenarios que importan. |
| Iterativo (mejor) | Generar tests básicos, luego pedir explícitamente: 'Que casos borde importantes no estoy cubriendo?' | Copilot identifica gaps en la cobertura que no habías pensado. |

| PROMPT SUGERIDO  —  Prompt para generar tests con casos borde Genera tests unitarios para la funcion \[nombre\]. Cubre los siguientes casos: \- Happy path: todos los parámetros validos \- Input undefined o null \- Valores en el limite (ej: exactamente 3 intentos) \- Valores de tipo incorrecto \- \[caso borde especifico de tu dominio\] Luego dime: ¿que casos borde importantes NO estoy cubriendo? Usa Jest como framework. El archivo va en tests/\[nombre\].test.js |
| :---- |

| ✏  EJEMPLO DE CODIGO  —  Ejemplo: tests generados con Jest para canRegisterForExam // tests/validaciones.test.js const { validarInscripcion } \= require('../js/validaciones'); describe('validarInscripcion', () \=\> {   test('happy path: cumple todos los requisitos', () \=\> {     const datos \= { promedio: 7.5, correlativaAprobada: true, intentos: 1 };     const { puede, mensaje } \= validarInscripcion(datos);     expect(puede).toBe(true);     expect(mensaje).toBe('OK');   });   test('sin correlativa aprobada', () \=\> {     const datos \= { promedio: 8.0, correlativaAprobada: false, intentos: 0 };     const { puede, mensaje } \= validarInscripcion(datos);     expect(puede).toBe(false);     expect(mensaje).toMatch(/correlativa/i);   });   test('limite exacto: exactamente 3 intentos (caso borde)', () \=\> {     const datos \= { promedio: 6.0, correlativaAprobada: true, intentos: 3 };     const { puede } \= validarInscripcion(datos);     expect(puede).toBe(false);  // 3 intentos \= no puede   }); }); |
| :---- |

### **Datos de prueba sintéticos**

Otra aplicación poderosa: generar datos de prueba realistas sin usar datos reales de usuarios (que podrían violar privacidad).

| PROMPT SUGERIDO  —  Prompt para generar datos de prueba sinteticos Genera 10 objetos JavaScript representando datos de formularios de inscripcion a examenes, con los campos:   promedio (number entre 0 y 10),   correlativaAprobada (boolean),   intentos (number entre 0 y 5). Incluye casos borde: promedio exactamente 4.0, intentos \= 0, intentos \= 3, correlativaAprobada \= false con buen promedio. Formato: array de objetos JavaScript listo para usar en Jest. No uses frameworks ni imports. Solo un array con objetos literales. |
| :---- |

| ACTIVIDAD  —  Practica B: Generar y evaluar tests (10 min) Tomar la función de la Practica A (o una función de su proyecto). Usar Copilot Chat con el prompt de casos borde para generar la suite de tests. Ejecutar los tests: npm test o npx jest \_\_tests\_\_/validaciones.test.js \--verbose Preguntar a Copilot: 'Que casos borde no estoy cubriendo?'. Agregar al menos 1 test adicional sugerido. Pregunta de reflexión: ¿Alguno de los tests generados por Copilot fallo con la implementación que el mismo género? Si es así, ¿qué dice eso sobre la calidad del código? |
| :---- |

| 2.4 | Git Workflow con IA: Commits, PRs y Code Review |
| :---: | :---- |

Ya saben git y pull requests. En esta sección, la IA entra como asistente en los tres momentos del workflow colaborativo donde más tiempo se pierde: escribir el mensaje de commit, redactar la descripción del PR, y hacer una primera pasada de code review.

### **Commit messages semánticos con Copilot**

Un commit bien escrito es documentación del proyecto. En seis meses, cuando el equipo necesite entender por qué se hizo un cambio, el commit message es la primera línea de investigación. Copilot puede sugerir mensajes semánticos a partir del diff.

| Tipo (Conventional Commits) | Cuando usarlo | Ejemplo |
| :---- | :---- | :---- |
| feat: | Nueva funcionalidad para el usuario | feat: agregar validación de intentos máximos en POST /exams/register |
| fix: | Corrección de bug | fix: corregir cálculo de promedio cuando el campo es undefined en MongoDB |
| test: | Agregar o corregir tests | test: agregar casos borde para canRegisterForExam con Jest |
| refactor: | Mejora de código sin cambiar comportamiento | refactor: extraer lógica de validación a middleware de Express |
| docs: | Documentación | docs: actualizar README con variables de entorno requeridas |
| chore: | Tareas de mantenimiento | chore: actualizar dependencias de jest a 29.7 |

| PROMPT SUGERIDO  —  Como obtener el commit message con Copilot En la terminal integrada de VS Code o en el Copilot Chat: \# Opcion 1: En Copilot Chat (panel lateral) @terminal Sugiere un commit message en formato Conventional Commits para los cambios en staging. El cambio agrega validacion de intentos maximos de examen en la funcion de inscripcion. \# Opcion 2: Copilot completado en el campo de mensaje de commit \# Al escribir el tipo (ej: 'feat:'), Copilot sugiere el resto \# basado en el diff de los archivos en staging |
| :---- |

### **PR Descriptions con IA**

Una buena descripción de PR es un resumen ejecutivo del cambio: que se hizo, por qué, cómo probarlo y cualquier decisión de diseño importante. Copilot puede generar el borrador; el Developer agrega el contexto de la User Story.

| PROMPT SUGERIDO  —  Prompt para generar descripcion de PR Genera la descripcion de un Pull Request en markdown con estas secciones: \#\# Que se hizo \[resumen del cambio en 2-3 oraciones\] \#\# Por que (contexto) \[User Story o issue relacionado, decision de diseno\] \#\# Como probar \[pasos para reproducir y validar el cambio\] \#\# Notas para el reviewer \[algo a prestar atencion, deuda tecnica pendiente, etc.\] Basate en estos commits: \[pegar lista de commits del PR\] Issue relacionado: \#\[numero\] |
| :---- |

| ✏  EJEMPLO DE CODIGO  —  Ejemplo de PR descripción bien estructurada \#\# Que se hizo Se agrego la funcion validarInscripcion() en js/validaciones.js. Valida del lado del cliente si un estudiante cumple los requisitos para inscribirse: promedio minimo, correlativa aprobada e intentos disponibles. \#\# Por que Resuelve la US \#12: 'Como estudiante quiero que el formulario me avise si no puedo inscribirme antes de enviar el formulario.' Closes \#12 \#\# Como probar 1\. Ejecutar los tests: npx jest tests/validaciones.test.js \--verbose 2\. Abrir index.html en el browser y probar el formulario con datos invalidos 3\. Debe mostrar el mensaje de error correspondiente debajo del campo \#\# Notas para el reviewer La logica de validacion esta en js/validaciones.js (funcion pura, sin dependencias). Pendiente: conectar la funcion con el evento submit del formulario (Issue \#15) |
| :---- |

### **Code Review asistido por IA**

Copilot puede hacer una primera pasada de code review antes de que el humano lo revise. Esto no reemplaza el code review humano: lo hace más eficiente eliminando comentarios sobre issues mecanicos (formato, convenciones, bugs obvios) para que el revisor pueda enfocarse en diseño, lógica de negocio y mantenibilidad.

* **En GitHub:** GitHub Copilot Code Review puede agregar comentarios automáticos al PR antes de que el equipo lo revise.  
* **En VS Code:** seleccionar código y usar Copilot Chat: 'Review this code for bugs, security issues and style violations'.  
* **Limitación critica:** la IA no conoce el contexto de negocio ni el Sprint Goal. Un reviewer humano siempre es necesario para evaluar si el cambio resuelve lo que la User Story requiere.

| ACTIVIDAD  —  Practica C: Commit \+ PR completo (10 min) Hacer un cambio pequeño en el repositorio del proyecto (puede ser agregar el test de la Practica B). Usar git add \-p para seleccionar el cambio y pedir a Copilot que sugiera el mensaje de commit. Crear un branch (feature/US-XX-descripcion) y hacer push. Abrir un PR en GitHub usando el template de descripción con IA. Incluir 'Closes \#\[issue\]'. Pedirle a un compañero que revise el PR. El reviewer puede usar Copilot Chat para hacer la primera pasada. |
| :---- |

## **Anti-patterns: cuando la IA hace daño**

Tan importante como saber usar la IA es saber cuándo NO usarla y que practicas convertir la IA de ayuda en problema. Estos anti-patterns son los más frecuentes en equipos que adoptan IA sin criterio:

| ⚠  ANTI-PATRON  —  Ship It Mentality — aceptar sin entender El anti-pattern mas común: aceptar el código de Copilot con Tab sin leerlo, hacer commit y mergear. El resultado es código que nadie del equipo entiende, que nadie puede mantener y cuyos bugs nadie puede debuggear cuando aparecen en producción. Regla: si no entendiste por que el código funciona, no tienes derecho a mergearlo. La IA no toma accountability del resultado; vos sí. |
| :---- |

| ⚠  ANTI-PATRON  —  Test Theater — tests que no testean Generar tests con IA que solo verifican el comportamiento del código que la IA misma género. Resultado: 90% de cobertura de líneas, 0% de cobertura real de comportamiento. Los tests pasan en CI pero los bugs de lógica de negocio pasan desapercibidos. Regla: un test valioso es aquel que fallaría si se introduce un bug conocido. Si no podes nombrar el bug que cada test atrapa, el test no tiene valor. |
| :---- |

| ⚠  ANTI-PATRON  —  Context Blindness — prompts sin contexto Pedirle a la IA que 'escriba el módulo de autenticación' sin darle contexto del stack tecnologico, las convenciones del equipo, los requisitos de seguridad o las decisiones de arquitectura previas. El resultado es código técnicamente valido pero incompatible con el proyecto real. Regla: el nivel de calidad del output de la IA es directamente proporcional al nivel de contexto del prompt. Garbage in, garbage out sigue siendo verdad. |
| :---- |

| ⚠  ANTI-PATRON  —  Prompt Dumping — delegar el pensamiento Pedirle a la IA que 'genere toda la arquitectura del sistema', 'escriba todos los tests' o 'diseñe el schema de la base de datos' sin entender los trade-offs de cada decisión. Cuando el sistema falla o necesita cambiar, el equipo no sabe cómo razonar sobre el problema porque nunca construyo ese entendimiento. Regla: la IA puede generar opciones; la decisión y el entendimiento son del equipo. Usar IA para explorar, no para pensar. |
| :---- |

| 2.5 | Prompt Engineering para Equipos Agiles |
| :---: | :---- |

En esta sección vamos a hacer explicita esa estructura y agregar técnicas avanzadas que van a multiplicar la calidad de los outputs de IA en las ceremonias del Sprint.

| CONCEPTO CLAVE  —  Que es Prompt Engineering en el contexto de Scrum Es la habilidad de comunicarle a la IA exactamente lo que necesitas, con el contexto suficiente para que el output sea útil sin revisión exhaustiva. En un equipo ágil, el prompt engineering no es una skill técnica opcional: es comunicación aplicada. Y como toda comunicación, mejora con practica y con un marco de referencia. |
| :---- |

### **Anatomía de un prompt efectivo**

Un prompt de alta calidad tiene cinco componentes. No todos son obligatorios en todos los casos, pero cuantos más incluyas, mejor el output:

| Componente | Descripcion | Ejemplo aplicado a Scrum |
| :---- | :---- | :---- |
| ROL | Qué tipo de experto debe ser la IA para esta tarea | “Actúa como Scrum Master experimentado con foco en equipos técnicos universitarios” |
| CONTEXTO | Toda la información de fondo que la IA necesita y no puede inferir | “Mi equipo es de 3 personas, estamos en el Sprint 2, la velocidad histórica es de 8 puntos” |
| TAREA | Que debe hacer, con verbos de acción concretos | “Genera el Sprint Goal para el proximo Sprint basándote en el backlog adjunto” |
| FORMATO | Como debe presentar el resultado | “Responde en bullet points, máximo 5 items, en español, sin introducción” |
| RESTRICCIONES | Lo que NO debe hacer o limitaciones importantes | “No incluyas tareas de testing ya que las manejamos por separado. No superes 2 semanas de alcance” |

### **Técnicas clave**

* **Role Prompting:** asignar un rol especifico a la IA antes de la tarea. “Actúa como Product Owner” produce outputs muy diferentes a “actúa como desarrollador senior” para la misma pregunta. Usar el rol que más se alinea con el tipo de razonamiento que necesitas.  
* **Few-Shot:** dar 1-2 ejemplos del formato que esperas antes de pedir el resultado. Si necesitas User Stories en un formato especifico, mostrar un ejemplo bien escrito antes de pedir las nuevas. La IA imita el patrón.  
* **Chain-of-Thought:** pedirle a la IA que razone paso a paso antes de dar la respuesta final. Para tareas complejas (ej: priorizar un backlog de 20 items) agregar “Primero analiza cada item por valor e impacto, luego ordénalos”. Mejora dramáticamente la calidad del razonamiento.  
* **Iterative Refinement:** el primer prompt rara vez es el mejor. Usar el output como punto de partida y refinar con un segundo prompt: “Bien. Ahora ajusta el punto 3 para que sea más especifico y agrega un criterio de aceptación para cada historia.”  
* **Context Injection:** pegar directamente el contenido relevante en el prompt. En lugar de describir el backlog, pegarlo. En lugar de describir las retros anteriores, pegarlas. La IA trabaja mejor con datos reales que con descripciones de datos.

### **Cheatsheet: Prompts listos para cada ceremonia**

Estos prompts están diseñados para copiar, adaptar el contexto y usar. Cada uno usa al menos 4 de los 5 componentes de la anatomía de prompts.

| PROMPT SUGERIDO  —  Sprint Planning — Generar Sprint Goal Actúa como Scrum Master de un equipo de 3 developers universitarios. Estamos por empezar el Sprint \[N\]. El Product Goal es: \[descripcion\]. Los items mas prioritarios del backlog son: \[pegar los 5-8 items mas prioritarios del backlog con sus estimaciones\] La velocidad promedio del equipo en los últimos Sprints fue de \[N\] puntos. Sugiere un Sprint Goal claro y 3 posibles combinaciones de items que lo cumplan, respetando la capacidad del equipo. Formato: Sprint Goal en 1 oración, luego cada opción como lista numerada. No incluyas tareas de infraestructura. |
| :---- |

| PROMPT SUGERIDO  —  Refinement — Detectar ambigüedades y mejorar historias Actúa como Developer senior revisando User Stories antes del Sprint Planning. Analiza estas historias de usuario y para cada una: 1\. Identifica ambigüedades o información faltante que podrían causar    malentendidos durante el desarrollo 2\. Sugiere criterios de aceptación faltantes en formato Given/When/Then 3\. Indica si cumple el criterio INVEST (especialmente Small y Testable) 4\. Propone como dividirla si es demasiado grande para un Sprint Historias a revisar: \[pegar las User Stories del backlog\] |
| :---- |

| PROMPT SUGERIDO  —  Daily Scrum — Resumen de estado del Sprint Actúa como Scrum Master preparando el contexto para la Daily. Basandote en esta informacion del tablero de GitHub Projects: \[pegar el estado actual: issues In Progress, bloqueados, completados\] Sprint Goal: \[describir el objetivo del Sprint\] Dias restantes del Sprint: \[N\] Genera un resumen de 5 líneas del estado del Sprint que incluya: \- Progreso hacia el Sprint Goal (en terminos de valor, no de tareas) \- Items en riesgo de no completarse \- Un impedimento potencial a resolver hoy No uses jerga tecnica. El resumen es para todo el equipo, no solo developers. |
| :---- |

| PROMPT SUGERIDO  —  Sprint Review — Generar release notes y resumen ejecutivo Actua como Technical Writer preparando materiales para el Sprint Review. El Sprint Goal fue: \[objetivo del Sprint\] Los Pull Requests mergeados en este Sprint fueron: \[pegar titulos y descripciones de los PRs del Sprint\] Genera: 1\. Release notes en formato markdown: que funcionalidades se entregaron,    en lenguaje de usuario (no tecnico) 2\. Un parrafo de resumen ejecutivo de 3 oraciones para presentar    al stakeholder: que se logro, que valor aporta al usuario, que sigue |
| :---- |

| PROMPT SUGERIDO  —  Retrospectiva — Sintetizar y sugerir action items Actua como Scrum Master facilitando la sintesis de una retrospectiva. El equipo completo la dinamica 4Ls (Liked / Learned / Lacked / Longed For). Estas son las respuestas de cada integrante: \[pegar el contenido de GitHub Discussions de la retro\] Por favor: 1\. Identifica los 3 temas que mas se repiten entre las respuestas 2\. Para cada tema, sugiere 1 action item especifico y medible para    el proximo Sprint (con responsable sugerido y forma de verificar) 3\. Destaca algo positivo que el equipo deberia seguir haciendo El formato debe ser claro para que el equipo vote los action items en clase. |
| :---- |

| 2.6 | IA en las Ceremonias del Sprint |
| :---: | :---- |

Ahora que tienen los prompts, el foco es entender el ROL de la IA en cada ceremonia: cuanto antes interviene, cuanto ayuda y, sobre todo, que no debe reemplazar. El principio es siempre el mismo: la IA prepara, el equipo decide.

| Ceremonia | La IA antes | La IA durante | La IA despues | Nunca reemplaza |
| :---- | :---- | :---- | :---- | :---- |
| Sprint Planning | Sugiere Sprint Goal, estima historias, detecta dependencias | Responde preguntas tecnicas sobre historias del backlog | Genera el Sprint Backlog documentado | La negociación del scope y el compromiso del equipo |
| Refinement | Detecta ambiguedades, sugiere criterios de aceptación faltantes | Ayuda a descomponer épicas en historias durante la sesión | Actualiza descripciones de issues con el resultado del refinement | La conversación entre PO y Developers para entender el “por que” |
| Daily Scrum | Resume el estado del Sprint desde el tablero | (No participa en vivo: la Daily es del equipo) | Detecta patrones de impedimentos para el SM | La sincronización humana y la detección de señales no verbales |
| Sprint Review | Genera release notes y resumen ejecutivo desde los PRs | Responde preguntas técnicas del stakeholder si se necesita | Sintetiza el feedback del stakeholder para el siguiente Sprint | La presentación en vivo y la relación con el stakeholder |
| Retrospectiva | Facilita la recolección asíncrona de respuestas 4Ls | Sintetiza patrones en tiempo real si el equipo lo decide | Genera action items y los agrega al backlog del proximo Sprint | Las conversaciones difíciles, la escucha activa, la reparación de confianza |

**Herramientas de IA para cada Ceremonia y Rol **

El siguiente mapeo conecta herramientas concretas de IA con las ceremonias de Scrum. El objetivo no es aprender a configurarlas todas, sino conocer el ecosistema y saber qué opciones existen para agilizar el trabajo diario.

**Nota importante:** Ninguna herramienta reemplaza la conversación humana ni la toma de decisiones del equipo. Úsalas para **preparar, resumir o automatizar lo repetitivo**.

| Ceremonia / Rol | Herramientas (Gratis / Open Source destacado) | ¿Qué ayuda a hacer? |
| :---- | :---- | :---- |
| Daily Scrum | Standuply, Geekbot, DailyBot, [Read.ai](https://read.ai/) | Recoger actualizaciones asíncronas, transcribir la daily, detectar bloqueos recurrentes y resumir el estado del Sprint. |
| Sprint Planning | ChatGPT, Claude, Jira+Atlassian Intelligence, Linear AI | Sugerir Sprint Goals, estimar historias, detectar dependencias y generar el Sprint Backlog. |
| Refinement (Grooming) | Copilot for Docs, Notion AI, ClickUp AI, Visual Paradigm AI | Descomponer épicas en historias, completar criterios de aceptación y detectar ambigüedades. |
| Sprint Review | Gamma, Tome, [Beautiful.ai](https://beautiful.ai/), [Otter.ai](https://otter.ai/) | Generar presentaciones, release notes, resúmenes ejecutivos y transcribir feedback del stakeholder. |
| Retrospectiva | Kollabe, Miro \+ IA, Neatro, Prosto.retro, Visual Paradigm AI | Facilitar dinámicas 4Ls, agrupar temas, sugerir action items y sintetizar respuestas anónimas. |
| Product Owner | ProdPad, Airfocus, Productboard (IA), NotebookLM | Priorizar backlog, analizar feedback de usuarios y detectar patrones en reseñas. |
| Scrum Master | Parabol, Scrumwise, ActionableAgile, Otter AI | Medir métricas de flujo, detectar impedimentos y preparar agendas de ceremonias. |
| Developer | GitHub Copilot, Codeium,  Claude , Gemini, CodeRabbit, Documentation Write | Generación de código, revisión automática, debugging y documentación. |

### **Sprint Planning con IA: el flujo completo**

El Sprint Planning es la ceremonia que más se beneficia de la preparación con IA, porque el input (backlog) ya está en formato digital y el output (Sprint Backlog) necesita ser concreto y acordado.

| Momento | Quien usa la IA | Que hace | Resultado |
| :---- | :---- | :---- | :---- |
| 2 días antes (PO) | Product Owner | Usa el Prompt de Sprint Goal para generar 3 opciones de objetivo | 3 opciones de Sprint Goal para proponer en la reunión |
| 1 día antes (PO) | Product Owner | Pide a la IA que detecte ambigüedades en las 8-10 historias más prioritarias | Lista de preguntas a resolver con el equipo antes de la Planning |
| Durante la Planning | Todo el equipo | Usa la IA para responder dudas técnicas puntuales (“cuanto tardaría implementar OAuth con este stack?”) | Estimaciones más informadas, menos discusiones circulares |
| Al terminar (SM) | Scrum Master | Genera el documento del Sprint Backlog con el Sprint Goal y los issues seleccionados | Sprint Backlog documentado y publicado en GitHub Projects |

### **Retrospectiva con IA: el modelo asíncrono \+ síncrono**

La Retrospectiva es la ceremonia donde la IA puede aportar más valor sin reemplazar lo más importante: la conversación honesta del equipo. El modelo hibrido asincrono-sincrono funciona mejor:

* **48h antes (asíncrono):** cada integrante completa la dinámica 4Ls en la herramienta elegida, por ejemplo, GitHub Discussions usando el template. **Liked** (me gustó), **Learned** (aprendí), **Lacked** (faltó / necesitábamos), **Longed For** (deseo para el próximo Sprint)  
* **24h antes (SM con IA):** el Scrum Master usa el Prompt de Retrospectiva para que la IA:

\-Identifique los 3 temas que más se repiten  
\-Sugiera posibles action items  
\-Proponga una agenda para la reunión sincrónica 

* **Durante la retro sincrónica:** el equipo discute los temas identificados, profundiza en las causas raíz y vota los action ítems concretos. La IA no participa en vivo.  
* **Al terminar (SM con IA):** los action items acordados se convierten en Issues en el backlog del siguiente Sprint, con responsable asignado.

| CONCEPTO CLAVE  —  La conversación que la IA no puede facilitar El momento más valioso de una buena retrospectiva no es identificar que salió mal: es la conversación que sigue, donde el equipo habla honestamente sobre por qué y cómo cambiar. Esa conversación requiere confianza psicológica, escucha activa y la disposición de alguien a decir algo incómodo. Ninguna de esas condiciones puede crearse con un prompt. La IA hace la parte preparatoria más rápida para que el equipo tenga más tiempo para la parte que importa. |
| :---- |

| ACTIVIDAD  —  Práctica D: Preparar una ceremonia real con IA (10 min) Elegir la proxima ceremonia de su proyecto (Planning del Sprint 2 o la primera Retrospectiva) y preparar el material usando la IA: Si eligen Sprint Planning: usar el Prompt de Sprint Goal con el backlog real del proyecto. Generar también la lista de preguntas para el equipo. Si eligen Retrospectiva: usar el template 4Ls y crear la Discussion en GitHub. Usar el Prompt de Retrospectiva para generar una agenda de la reunión sincronía. Evaluar: ¿qué parte del output de la IA usarían sin cambios? ¿Qué ajustarían? |
| :---- |

| 2.7 | Agentes de IA y el Futuro Cercano |
| :---: | :---- |

Hasta ahora vimos la IA como copiloto: asiste, sugiere, genera. La siguiente frontera son los agentes autónomos: sistemas que pueden tomar un objetivo y ejecutar múltiples pasos sin intervención humana continua. Ya no son el futuro: algunas de estas herramientas existen hoy.

| 🤖  Agentes de código disponibles Herramienta Que puede hacer de forma autónoma Nivel de autonomía GitHub Copilot Workspace Tomar un Issue, analizar el repositorio, proponer un plan de cambios y ejecutar el código en un entorno aislado Alto — revisión humana requerida antes del merge Claude Code Leer el repositorio completo, escribir código, ejecutar tests y hacer commits de forma iterativa Alto — opera en la terminal del developer Cursor (modo Composer) Editar múltiples archivos simultáneamente para implementar una feature compleja Medio — el developer guía y aprueba cada paso GitHub Actions \+ IA Ejecutar pipelines que incluyen análisis de código con IA, auto-fix de issues de estilo, generación de changelogs Medio — configuración inicial humana, ejecución automática  |
| :---- |

### **Que cambia en Scrum cuando los agentes entran al equipo**

La llegada de agentes autónomos no elimina la necesidad de Scrum: la hace más critica. Cuando un agente puede generar 500 líneas de código en 10 minutos, el equipo necesita más estructura, no menos, para mantenerse orientado al valor.

| Elemento de Scrum | Antes de agentes autónomos | Con agentes autónomos |
| :---- | :---- | :---- |
| Sprint Goal | Orientación para el equipo humano | Restricción de scope para el agente: sin Sprint Goal claro, el agente puede generar código correcto pero irrelevante |
| Definition of Done | Checklist de calidad para el Developer | La primera línea de defensa para el trabajo generado por agentes: el DoD es lo que distingue “el agente termino” de “el Increment está listo” |
| Code Review | Validación técnica por un humano | Responsabilidad ética y de negocio: el reviewer no solo aprueba la técnica sino que garantiza que el código generado es seguro, correcto y alineado con los valores del equipo |
| Daily Scrum | Sincronización del equipo humano | Inspección del trabajo de agentes: qué genero cada agente, que anomalías se detectaron, que decisiones tomaron sin consultar |
| Sprint Review | Presentación del Incremento al stakeholder | Validación de que el Incremento generado con agentes cumple el Sprint Goal y no introduce riesgos no evaluados |

| CONCEPTO CLAVE  —  La habilidad que más vale en un mundo con agentes Cuando el código se puede generar en segundos, la pregunta ya no es “¿puedo escribir este código?” sino “debería escribir este código, y si es así, cómo se integra con el resto del sistema, que riesgos introduce y quien es responsable si falla?”. Esa pregunta requiere comprensión de arquitectura, contexto de negocio y accountability. Ninguna de las tres cosas puede delegarse a un agente. |
| :---- |

| 2.8 | El Factor Humano en Equipos AI-Augmented |
| :---: | :---- |

Este módulo, y el curso, cierra con una paradoja que vale la pena nombrar en voz alta: cuanto más hace la IA, más visible se vuelve lo que los humanos hacen que la IA no puede. La IA iguala rápido la capacidad técnica. Lo que diferencia a los profesionales en ese escenario no es el conocimiento técnico — es lo que siempre fue más difícil de aprender.

### **La paradoja de la IA y las habilidades blandas**

Cuando escribir código tarda segundos, el cuello de botella del equipo ya no es técnico. Es humano: comunicar con precisión, tomar criterio en condiciones de incertidumbre, facilitar conversaciones donde el equipo no está de acuerdo, y responder por el resultado cuando algo falla. Esas son exactamente las habilidades que Scrum siempre requirió y que la IA hace más visibles porque ya no se pueden esconder detrás de la velocidad de escritura.

| Habilidad | Por qué se vuelve más crítica con IA | Como se manifiesta en Scrum |
| :---- | :---- | :---- |
| Pensamiento critico | La IA genera con confianza tanto respuestas correctas como incorrectas. Sin pensamiento crítico, el equipo no puede distinguir las unas de las otras. | Revisar código generado con Copilot. Cuestionar el output de la IA en ceremonias. Detectar cuando un agente tomo una decisión incorrecta. |
| Comunicación precisa | El prompt engineering ES comunicación técnica aplicada. Un prompt ambiguo produce un output ambiguo. El mismo principio aplica a las User Stories, al Sprint Goal y a los criterios de aceptación. | Escribir User Stories que no necesiten explicación adicional. Formular Sprint Goals que la IA pueda usar como restricción de scope. Dar feedback de code review que sea accionable. |
| Facilitación | Con IA, los equipos tienen más datos, más opciones y más velocidad. Alguien tiene que dar sentido a esa abundancia y guiar al equipo hacia decisiones, especialmente cuando no hay consenso. | Liderar retrospectivas donde el equipo habla honestamente. Facilitar un Sprint Planning donde hay desacuerdo sobre el scope. Ayudar al equipo a decidir cuándo rechazar el output de la IA. |
| Accountability | La IA produce pero no responde. El equipo firma. En un mundo con agentes autónomos, la accountability se vuelve el valor diferencial del profesional humano: alguien que puede ser responsable del resultado. | Mergear solo código que entender. Comprometerte con el Sprint Goal y responder si no se cumple. Decirle al stakeholder “nos equivocamos” cuando corresponde. |
| Adaptabilidad | Las herramientas de IA cambian cada 3-6 meses. La habilidad de aprender nuevas herramientas rápidamente, sin perder el criterio sobre cuales valen la pena, es en sí misma una ventaja competitiva. | Experimentar con nuevas herramientas en un Sprint dedicado. Evaluar en la Retrospectiva si una herramienta nueva agrego valor real. Saber cuándo una herramienta complica más de lo que simplifica. |

### **Lo que la IA definitivamente no puede hacer en un equipo Scrum**

No por limitación tecnológica actual, sino por naturaleza: estas capacidades requieren presencia, historia compartida y la posibilidad de ser responsable de las consecuencias.

* Facilitar una conversación difícil en una retrospectiva donde hay tensión entre integrantes del equipo.  
* Generar confianza psicológica en un equipo nuevo o en uno que tuvo un conflicto reciente.  
* Leer el lenguaje no verbal de un stakeholder que dice que está conforme pero claramente no lo está.  
* Decir “esto está mal” cuando hay presión del cliente, del jefe o del cronograma para entregarlo igual.  
* Comprometerse con el Sprint Goal y cargar con el peso de ese compromiso durante dos semanas.  
* Aprender de un error y cambiar el comportamiento en el siguiente Sprint.

| ✨  Pregunta para llevarse En cinco años, cuando la IA pueda hacer el 80% de las tareas técnicas que hoy hacen los Developers, ¿qué parte de tu trabajo queres que sea irremplazablemente tuya? No hay respuesta correcta. Pero tener una respuesta propia — y trabajar para desarrollar esa capacidad — es la diferencia entre adaptarse al cambio y ser reemplazado por él.  |
| :---- |

| ASYNC 2 | Actividad Final: Sprint Simulado Completo |
| :---: | :---- |

Esta es la actividad integradora del curso. Simula un Sprint completo usando todas las herramientas y técnicas de los tres módulos. 

| ACTIVIDAD  —  Sprint Simulado — Parte 1: Planning con IA  Objetivo: planificar el Sprint 2 del proyecto usando los prompts del Módulo 3\. Usar el Prompt de Sprint Goal para generar 3 opciones de objetivo para el Sprint 2\. Como equipo, elegir y ajustar el Sprint Goal final. Documentarlo en el Milestone Sprint 2 de GitHub. Usar el Prompt de Refinement para detectar ambigüedades en las 5 historias más prioritarias del backlog. Seleccionar 3-4 historias para el Sprint 2 y asignarlas al Milestone. Crear sub-issues (tasks) para al menos 1 historia. |
| :---- |

| ACTIVIDAD  —  Sprint Simulado — Parte 2: Desarrollo con Copilot  Objetivo: implementar una historia completa usando las técnicas del Módulo 2\. Elegir la historia de mayor prioridad del Sprint 2 y moverla a “In Progress” en el tablero. Implementar usando Comment-Driven Development con GitHub Copilot. Generar tests unitarios con Copilot (al menos 3 casos: happy path \+ 2 casos borde). Crear el branch, hacer commits con Conventional Commits y abrir el PR con descripción completa generada con IA. Incluir “Closes \#\[issue\]” y la sección “Uso de IA”. Un compañero hace code review y aprueba o solicita cambios con al menos 2 comentarios. Mergear cuando este aprobado. |
| :---- |

| ACTIVIDAD  —  Sprint Simulado — Parte 3: Review y Retrospectiva  Objetivo: cerrar el ciclo con las ceremonias de cierre del Sprint. Usar el Prompt de Sprint Review para generar release notes del Sprint 1 (los PRs mergeados hasta ahora). Publicarlas en el README o en una GitHub Discussion. Cada integrante completa la dinámica 4Ls en una GitHub Discussion nueva (categoría Retrospectivas). Usar el Prompt de Retrospectiva para sintetizar las respuestas e identificar los 3 temas principales y los action items sugeridos. Como equipo, acordar 1 action item concreto para el Sprint 2\. Crearlo como Issue en el backlog con responsable asignado. |
| :---- |

| ACTIVIDAD  —  Sprint Simulado — Parte 4: Reflexión individual  Objetivo: cerrar el curso con una reflexión personal documentada. Crear un archivo docs/reflexion-final.md en el repositorio. Responder estas 3 preguntas (mínimo 1 párrafo cada una): ¿En qué parte del Sprint simulado la IA agrego más valor? ¿En cuál fue un obstáculo? ¿Qué habilidad propia (técnica o blanda) fue más necesaria para trabajar bien con IA? ¿Qué cambiarias en tu forma de trabajar en el próximo proyecto real? Hacer commit y push del archivo. El link al repositorio es el entregable final del curso. |
| :---- |

### **Entregable final**

Repositorio de GitHub con: tablero del Sprint 2 configurado, PR mergeado con tests, release notes del Sprint 1, Discussion de retrospectiva con action item como Issue, y archivo docs/reflexion-final.md.

### **Criterio de aprobación**

* El Sprint Goal del Sprint 2 está documentado en el Milestone.  
* El PR de la historia implementada tiene descripción completa y sección “Uso de IA”.  
* Los tests unitarios pasan y cubren al menos happy path \+ 2 casos borde.  
* La reflexión final muestra pensamiento crítico sobre el uso de IA, no solo descripción de herramientas.

## **Referencias y recursos**

* GitHub Copilot Docs: docs.github.com/en/copilot  
* Scrum.org — 'AI as a Scrum Team Member' (2024)  
* Scrum.org — 'AI Augmented Scrum Framework' (2026)  
* Conventional Commits specification: conventionalcommits.org  
* GitHub Student Developer Pack (Copilot gratuito): education.github.com/pack  
* Scrum.org — “AI Augmented Scrum Framework” (2026): scrum.org/resources  
* Scrum.org — “AI as a Scrum Team Member” (2024): scrum.org/resources  
* GitHub Copilot Workspace: githubnext.com  
* Claude Code: claude.ai/code  
* Schwaber, K. & Sutherland, J. (2020). The Scrum Guide: scrumguides.org  
* Caroli, P. (2018). Lean Inception: caroli.org/lean-inception

