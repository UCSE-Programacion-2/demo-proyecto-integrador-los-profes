

| MÓDULO 1   —  Ingeniería en Informática Scrum en el Mundo Real |
| :---- |

**Curso-Taller: Desarrollo Ágil con IA**

*Maximizando el Potencial de Scrum con Herramientas Inteligentes*

Herramientas: GitHub, GitHub Copilot, ChatGPT / Claude

## **Objetivos del modulo**

* Comprender el marco Scrum desde lo práctico, con foco en el propósito de cada elemento.  
* Escribir Historias de Usuario efectivas con criterios de aceptación verificables.  
* Entender como la incorporación de la IA esta reconvirtiendo los roles y prácticas de Scrum.  
* Aplicar la técnica Lean Inception asistida por IA para clarificar el alcance del proyecto.  
* Generar un prototipo rápido de la pantalla principal usando IA como copiloto de diseño.  
* Elaborar un Product Brief liviano con IA e identificar las Épicas iniciales del producto.  
* Configurar GitHub como ecosistema Scrum completo, conectando las Épicas del Brief con el tablero.

| 1.1 | Fundamentos de Scrum |
| :---: | :---- |

Scrum no es un proceso rígido ni una lista de pasos. Es un marco de trabajo liviano que ayuda a los equipos a generar valor en entornos complejos. El Scrum Guide 2020 tiene apenas 13 paginas, precisamente porque Scrum es intencional en lo que NO prescribe: deja que cada equipo defina su propia forma de trabajar dentro del marco.

### **Por qué falla el desarrollo en cascada**

El principio de incertidumbre de Humphrey es brutal en su honestidad: “Para un nuevo sistema de software, los requisitos no serán completamente conocidos hasta después de que los usuarios lo hayan usado.” Construir durante meses para mostrar el resultado al final no solo es riesgoso, es estructuralmente incompatible con cómo funcionan los requisitos reales.

| Criterio | Gestión Tradicional (Waterfall) | Gestión Ágil (Scrum) |
| :---- | :---- | :---- |
| Enfoque | Secuencial y lineal | Iterativo e incremental |
| Requisitos | Fijos desde el inicio | Flexibles, evolucionan con el proyecto |
| Entrega de valor | Al final del proyecto | Desde el primer Sprint |
| Respuesta al cambio | Resistencia (costo alto) | Bienvenida (aprendizaje) |
| Control | Rigido: seguimiento de plan | Adaptativo: ajustes continuos |

### **El marco Scrum: Roles, Artefactos y Eventos**

Scrum define tres responsabilidades, tres artefactos y cinco eventos. Nada más, nada menos. Lo importante es entender el propósito de cada elemento, no memorizarlos.

### **Roles — Accountabilities (responsabilidades)**

* **Product Owner:** Es el responsable de maximizar el valor del producto. Gestiona y ordena el Product Backlog. Es la única persona con autoridad para decidir que se construye y en qué orden. NO es un jefe de equipo ni asigna tareas.  
* **Scrum Master:** Es el guardián del marco. Remueve impedimentos, facilita las ceremonias y protege al equipo de interferencias externas. Es un líder servidor, NO un project manager. No asigna tareas ni controla el tiempo individual.  
* **Developers:** Equipo auto-organizado y multifuncional responsable de convertir los elementos del Sprint Backlog en un Increment funcional. “Developer” no significa solo “programador”: incluye analistas, testers, diseñadores, quien sea necesario para producir el Incremento.

### **Artefactos**

* **Product Backlog:** Lista ordenada de todo lo que se conoce que podría mejorar el producto. Es propiedad del Product Owner. Nunca esta “completo”: evoluciona mientras el producto existe. Commitment: Product Goal.  
* **Sprint Backlog:** Subconjunto del Product Backlog seleccionado para el Sprint, más el plan del equipo para alcanzar el Sprint Goal. Es propiedad de los Developers. Commitment: Sprint Goal.  
* **Increment:** Suma de todos los elementos completados en el Sprint actual mas todos los anteriores. Debe cumplir el Definition of Done y ser potencialmente entregable, aunque no se entregue. Commitment: Definition of Done.

### **Eventos (Sprint de 2 semanas como referencia)**

| Evento | Proposito | Duracion maxima |
| :---- | :---- | :---- |
| Sprint | Contenedor de todos los demas eventos. Produce un Increment. | 1 a 4 semanas (fijo) |
| Sprint Planning | Definir el Sprint Goal y seleccionar el trabajo del Sprint. | 4 horas |
| Daily Scrum | Inspeccion diaria del progreso hacia el Sprint Goal. Solo Developers. | 15 minutos |
| Sprint Review | Inspeccionar el Increment con stakeholders y adaptar el Product Backlog. | 2 horas |
| Sprint Retrospective | Reflexionar sobre el proceso e identificar mejoras concretas. | 1.5 horas |

### **Definition of Ready (DoR) y Definition of Done (DoD)**

| CONCEPTO CLAVE  —  DoR y DoD Definition of Ready (DoR): Criterios que debe cumplir un elemento del Product Backlog para poder entrar al Sprint. Lo define el equipo. Ejemplo: “La historia tiene criterios de aceptación escritos y estimación acordada.” Definition of Done (DoD): Criterios que debe cumplir el Increment para considerarse terminado. Es la promesa de calidad del equipo. Ejemplo: “Código revisado, tests pasando, PR mergeado, issue cerrado.” |
| :---- |

### **Los 5 Valores de Scrum**

Estos valores no son decorativos. Son las condiciones que permiten que el empirismo funcione en la práctica:

* Compromiso: el equipo se compromete con los objetivos del Sprint y entre sí.  
* Foco: durante el Sprint, el equipo se concentra en el trabajo elegido.  
* Apertura: todos son transparentes sobre el trabajo y los obstáculos.  
* Respeto: los miembros del equipo se respetan como personas capaces e independientes.  
* Coraje: hacer lo correcto y trabajar en problemas difíciles aunque sea incómodo.

| 1.2 | Historias de Usuario Efectivas |
| :---: | :---- |

Una Historia de Usuario no es un requisito funcional. Es una promesa de conversación: una descripción breve de una funcionalidad desde la perspectiva del usuario que abre el dialogo entre el equipo y quien pidió la funcionalidad. Si escribís una historia y ya no hay nada que conversar sobre ella, probablemente este mal escrita.

### **Formato estándar**

| CONCEPTO CLAVE  —  Estructura de una Historia de Usuario Como *\[tipo de usuario\]* quiero *\[funcionalidad\]* para *\[beneficio o valor\].* |
| :---- |

### **Criterio INVEST**

Una buena Historia de Usuario cumple con el criterio INVEST. Si alguna de estas condiciones falla, es una señal de que hay que reescribirla o dividirla:

| Letra | Significado | Pregunta para verificar |
| :---- | :---- | :---- |
| I  —  Independent | Independiente de otras historias | ¿Se puede construir sin depender de otra historia sin entregar? |
| N  —  Negotiable | El cómo es negociable | ¿El equipo tiene libertad para elegir la solución técnica? |
| V  —  Valuable | Aporta valor al usuario | ¿Alguien pagaría por esta funcionalidad? |
| E  —  Estimable | Se puede estimar el esfuerzo | ¿El equipo entiende lo suficiente para estimar? |
| S  —  Small | Completable en un Sprint | ¿Puede hacerse en menos de 2-3 días? |
| T  —  Testable | Se puede verificar si esta lista | ¿Sabemos cuándo la historia está terminada? |

### **Criterios de Aceptacion con Given / When / Then**

Los Criterios de Aceptación definen el comportamiento esperado del sistema de forma verificable. El formato Gherkin (Given/When/Then) es el más usado porque estructura el criterio como un escenario concreto:

| Parte | Significado | Ejemplo |
| :---- | :---- | :---- |
| Given (Dado que) | Contexto o estado previo del sistema | Dado que el usuario está en la pantalla de login |
| When (Cuando) | Acción que realiza el usuario | Cuando hace clic en “Olvide mi contraseña” e ingresa su email |
| Then (Entonces) | Resultado esperado y verificable | Entonces recibe un email con link de recuperacion en menos de 2 minutos |

Ejemplo completo de Historia con Criterios de Aceptación:

| CONCEPTO CLAVE  —  Ejemplo: Historia bien escrita Historia: Como usuario registrado quiero poder recuperar mi contraseña para acceder a mi cuenta si la olvide. CA 1: Dado que estoy en la pantalla de login, cuando hago clic en “Olvide mi contraseña” e ingreso mi email, entonces recibo un email con link de recuperación en menos de 2 minutos. CA 2: Dado que hago clic en el link de recuperación, cuando han pasado más de 24 horas desde que fue generado, entonces el link es invalido y se me informa el error. |
| :---- |

### **Practica: Detectar y reescribir historias mal escritas**

| ACTIVIDAD A  —  Reescribir 2 historias defectuosas Identifiquen que principio INVEST viola cada historia y reescríbanla correctamente con al menos un Criterio de Aceptación en formato Given/When/Then. Historia A: Quiero que el login funcione bien. Que está mal: No tiene usuario, no tiene valor explicito, “funcione bien” no es verificable. Historia B: Como administrador quiero poder gestionar todos los datos del sistema. Que está mal: Es demasiado grande (no es Small), “todos los datos” es ambiguo (no Testable). |
| :---- |

| 1.3 | ¿Scrum murió? La reconversión del framework |
| :---: | :---- |

Desde 2023, con la explosión de los LLMs y las herramientas de AI coding, circulan argumentos del tipo “Scrum is dead”, “las dailies son una perdida de tiempo” o “los equipos de IA no necesitan sprints”. ¿Qué hay de cierto?

| Postura: Scrum está obsoleto | Postura: Scrum se reconvierte |
| :---- | :---- |
| “Scrum fue diseñado para equipos de 3-9 personas. La IA puede hacer lo que hacían 9 desarrolladores. Las ceremonias son overhead innecesario.” | “Los pilares empíricos de Scrum —transparencia, inspección, adaptación— son más críticos que nunca cuando la IA puede generar código más rápido de lo que los equipos pueden validarlo.” |

### **Los 3 cambios reales que si están ocurriendo**

El mercado no dice que Scrum murió. Dice que está cambiando. Y los cambios son concretos:

**Cambio 1: Reconversión de roles.**

El Developer ya no solo escribe código: es un “Agent Orchestrator” que guía, valida y corrige el trabajo de herramientas de IA. El Scrum Master evoluciona hacia un agente de cambio organizacional que usa datos para tomar decisiones. Y el Product Owner descubre que su habilidad más valiosa en un equipo AI-augmented no es crear historias — la IA puede hacer eso — sino decir NO con criterio.

**Cambio 2: Nuevas métricas.**

La velocity (cuantos puntos hizo el equipo) pierde relevancia cuando la IA puede generar código en segundos. Las métricas que importan ahora son: cycle time (cuánto tarda una historia desde “en progreso” hasta “en producción”), lead time (desde que se crea el ítem hasta que se entrega) y calidad del Increment (cuantos bugs pasan a producción).

**Cambio 3: El Sprint Goal se vuelve más crítico, no menos.**

Sin una dirección clara, la IA puede generar volumen sin valor. El Sprint Goal es el ancla que evita que el equipo quede atrapado en un loop hiperactivo de generación de código sin propósito estratégico. Las ceremonias que definen y revisan el Sprint Goal — Planning y Review — ganan importancia, no la pierden.

| CONCEPTO CLAVE  —  Frase ancla del curso *Lo que murió es la ceremonia sin propósito. Lo que vive es el empirismo.* |
| :---- |

| 1.4 | Lean Inception, Prototipado y Product Brief con IA |
| :---: | :---- |

Esta sección sigue un flujo completo de discovery de producto asistido por IA: partimos de una idea, la clarificamos con la técnica de Lean Inception, la hacemos visible con un prototipo rápido y la formalizamos en un Product Brief que da origen al Product Backlog. Cada paso alimenta al siguiente.

| Parte | Técnica | Tiempo |
| :---- | :---- | :---- |
| A | Lean Inception — Es / No es / Hace / No hace | 15 min |
| B | Prototipado rápido con IA | 10 min |
| C | Product Brief con IA → Épicas | 15 min |
| → | Conexión con la Sección 1.5 (GitHub Projects) | 5 min |

### **Parte A — Lean Inception: Es / No es / Hace / No hace**

La técnica “Es / No es / Hace / No hace” del libro Lean Inception (Paulo Caroli) es la forma más rápida de alinear un equipo en torno a los límites del producto. Antes de hablar de funcionalidades, hay que acordar que ES el producto y que NO ES.

| ES Características y definiciones clave del producto. | NO ES Aquello que alguien podría asumir que es el producto, pero no lo es. |
| :---- | :---- |
| **HACE Funcionalidades o acciones concretas que el producto realiza.** | **NO HACE Lo que explícitamente no hará en esta etapa del MVP.** |

1. (3 min) Describir el proyecto en exactamente 2 oraciones. La restricción es intencional: obliga a priorizar lo esencial.  
2. (4 min) Usar el Prompt A para completar la matriz. No editar el resultado todavía, solo generarlo.  
3. (6 min) Comparar con lo que el equipo tenía en mente. Marcar en cada cuadrante: que acertó la IA, que asumió sin preguntar, que le falta contexto.  
4. (2 min) Cada equipo comparte UNA sorpresa con el resto de la clase.

| PROMPT SUGERIDO  —  Prompt A — Generar la matriz Lean Inception Actúa como Product Owner experimentado. Mi equipo está construyendo el siguiente producto: \[descripción en 2 oraciones\] Completa una matriz “Es / No es / Hace / No hace” para clarificar el alcance del MVP. Da 3 a 5 ítems por cuadrante. Considera malentendidos comunes en proyectos similares. |
| :---- |

**Lección clave:** Lo que la IA asume que no discutiste, generalmente es lo que el equipo tampoco discutió entre sí. Esa brecha es exactamente donde el Product Owner agrega valor irreemplazable.

### **Parte B — Product Brief con IA**

El Product Brief NO es un PRD (Product Requirements Document). Es un documento liviano — idealmente una página — que da suficiente contexto para que el equipo pueda construir el Product Backlog inicial. Su valor no está en la exhaustividad, sino en la alineación: todos leen lo mismo y entienden lo mismo.

| CONCEPTO CLAVE  —  Diferencia clave: PRD vs Product Brief PRD (evitar en Agile) Product Brief (lo que hacemos) 30-100 páginas de requisitos detallados 1 página con contexto esencial Se escribe antes de empezar, no cambia Evoluciona Sprint a Sprint Asume que los requisitos son conocibles desde el inicio Reconoce la incertidumbre, permite ajustes Genera ilusión de certeza Genera alineación sobre lo que se sabe hoy  |
| :---- |

### **Estructura del Product Brief**

El Brief tiene 7 secciones. Cada una debe poder escribirse en 2-3 oraciones o bullets. Si necesita más, es una señal de que el equipo no tiene suficiente claridad todavía:

* **Nombre del producto:** nombre de trabajo del proyecto.  
* **Visión:** una oración que explica por qué existe el producto. El “para que” de más alto nivel.  
* **Problema que resuelve:** 2-3 bullets con los dolores reales del usuario que el producto atiende.  
* **Usuarios objetivo:** 2-3 perfiles de usuario. No demografías genéricas: perfiles con un contexto concreto.  
* **Épicas (funcionalidades clave):** 3-5 áreas funcionales de alto nivel. Cada una se va a convertir en un conjunto de Historias de Usuario en el Product Backlog.  
* **Lo que NO incluye el MVP:** viene directamente del cuadrante NO HACE de la matriz. Es igual de importante que lo que si incluye.  
* **Restricciones conocidas:** técnicas (lenguaje, plataforma, integraciones) y de negocio (plazo, presupuesto, regulaciones).

| PROMPT SUGERIDO  —  Prompt B — Generar el Product Brief Actúa como Product Manager senior. Tengo la siguiente información sobre mi producto: Descripción: \[2 oraciones del paso A\] Matriz Lean Inception: \- ES: \[ítems del cuadrante\] \- NO ES: \[ítems del cuadrante\] \- HACE: \[ítems del cuadrante\] \- NO HACE: \[ítems del cuadrante\] Genera un Product Brief liviano con estas secciones: 1\. Nombre del producto 2\. Visión (1 oración) 3\. Problema que resuelve (3 bullets) 4\. Usuarios objetivo (2-3 perfiles concretos) 5\. Épicas / funcionalidades clave (3-5, en formato: Nombre \- descripción breve) 6\. Lo que NO incluye el MVP 7\. Restricciones conocidas El Brief debe caber en una página. Se conciso. |
| :---- |

### **De las Épicas al Product Backlog**

Las Épicas del Brief son el primer nivel del Product Backlog. Cada Épica agrupa un conjunto de Historias de Usuario relacionadas. Esta jerarquía conecta directamente con GitHub Projects: cada Épica puede ser un Issue de tipo “epic” (o un Milestone si el proyecto es pequeño), y las Historias de Usuario son los Issues hijos.

| CONCEPTO CLAVE  —  Flujo completo: de la idea al Sprint Idea  →  Lean Inception (alineación de alcance)  →  Prototipo rápido (visualización)  →  Product Brief (contexto formalizado)  →  Épicas en el Product Backlog  →  Historias de Usuario  →  Sprint 1 |
| :---- |

| ACTIVIDAD  B — Práctica  Usar el Prompt C para generar el Product Brief completo de su proyecto. Identificar las 3-5 Épicas del Brief. Escribirlas en un papel o en una nota del repositorio. Para cada Épica, pensar al menos 2 Historias de Usuario posibles. No escribirlas completas todavía: solo el “Como \[usuario\] quiero \[algo\]”. Conexión con la próxima sección: Las Épicas que identificaron ahora se van a convertir en los primeros Issues de GitHub Projects en la Sección 1.5. |
| :---- |

### **Parte C — Prototipado rápido con IA**

Una vez que el equipo tiene el Product Brief y las Épicas definidas, surge una pregunta natural: ¿cómo se vería la pantalla principal de la primera Épica? Ver algo concreto —aunque sea un boceto en texto— cambia la conversación sobre requisitos de forma dramática. Las ambigüedades que sobrevivieron al Brief aparecen en segundos cuando alguien intenta visualizar la interfaz.

Para generar un prototipo rápido podemos usar distintos enfoques según el tiempo disponible y el nivel de fidelidad que necesitemos:

| Herramienta | Qué genera | Acceso |
| :---- | :---- | :---- |
| **ChatGPT / Claude (prompt)** | Descripción textual detallada de la interfaz por componentes (header, navegación, áreas de contenido, acciones) | Gratuito, sin registro |
| [**v0.dev**](https://v0.dev/)** (Vercel)** | Componente React funcional con UI real, exportable | Cuenta gratuita (Google o GitHub) |
| [**Bolt.new**](https://bolt.new/) | App web completa con frontend \+ lógica básica | Cuenta gratuita |
| **Visily** | Wireframes y prototipos de alta fidelidad a partir de texto, capturas o bocetos | Plan gratuito disponible |
| **Lovable** | App full-stack completa (frontend \+ backend \+ despliegue) a partir de descripciones en lenguaje natural | Plan gratuito con créditos diarios |
| **Stitch (by Google Labs)** | Prototipos interactivos de alta fidelidad a partir de descripciones en lenguaje natural o voz. Incluye canvas infinito, agente de diseño, exportación a HTML/CSS/React y DESIGN.md para reglas de diseño compartibles  | Completamente gratuito (sin límites durante fase experimental). Requiere cuenta de Google. 350 generaciones/mes en modo estándar \+ 200 en modo experimenta |

En esta clase vamos a usar el **Prompt C** (ChatGPT/Claude) para no depender de registros externos. El resultado será una **descripción clara de la interfaz** que el equipo puede leer, criticar y ajustar en minutos. La actividad con [v0.dev](https://v0.dev/), [Bolt.new](https://bolt.new/), Visily o Lovable queda como exploración opcional para la actividad asincrónica.

| PROMPT SUGERIDO  —  Prompt C —Generar descripción de la interfaz principal  Actúa como diseñador UX. Basándote en este producto: \[pegar descripción del producto de 2 oraciones\] Y en la siguiente Épica del Product Brief (la de mayor prioridad): \[Nombre de la Épica\] — \[descripción breve de la Épica\] Genera una descripción estructurada de la pantalla principal que soporta esta Épica. Usa el siguiente formato: \#\# Estructura de la pantalla principal \#\#\# Header \- \[qué elementos contiene: logo, título, perfil de usuario, etc.\] \#\#\# Navegación principal \- \[lista de secciones o pestañas disponibles, relacionadas con la Épica\] \#\#\# Área principal \- \[describe cada bloque de contenido, orden y propósito, alineado con la Épica\] \#\#\# Acciones clave \- \[botones o interacciones principales que el usuario puede realizar\] \#\#\# Estado inicial (cuando el usuario abre la pantalla por primera vez) \- \[qué datos se ven, qué está cargando, qué está vacío\] Después de la descripción, lista 3 decisiones de diseño que tomaste y que el equipo debería validar explícitamente con usuarios reales.  |
| :---- |

| ACTIVIDAD  C — Práctica  Usar el Prompt C (el que generamos con la Épica) para obtener la descripción estructurada de la pantalla principal.. Revisar las “3 decisiones de diseño” que lista la IA al final. ¿Alguna sorprende al equipo? ¿Hay alguna decisión que el equipo no había considerado? Iterar rápidamente: pedir a la IA que ajuste un elemento específico. Ejemplo: “En el área principal, cambia el orden: primero el listado de cursos y después el resumen del perfil.” Opcional \- v0.dev: pegar la descripción generada y ver el componente React.\- Visily: subir una captura de pantalla de referencia o usar un prompt para generar wireframes.\-Lovable: pegar la descripción y observar cómo genera una aplicación full-stack.  Pregunta de reflexión: La descripción y prototipo generado por la IA, ¿refleja lo que el equipo tenía en mente? ¿Qué cambiarían antes de mostrárselo a un usuario real? |
| :---- |

| 1.5 | Herramientas para gestión ágil de proyectos |
| :---: | :---- |

## Antes de sumergirnos en GitHub Projects, vale la pena conocer el ecosistema de herramientas de gestión ágil. GitHub Projects es una opción excelente cuando el código ya está en GitHub y el equipo es pequeño. Pero no es la única. Dependiendo del contexto, el presupuesto y las necesidades del equipo, existen alternativas más especializadas.

## La siguiente tabla compara las herramientas más utilizadas en la industria, incluyendo Azure DevOps, que es una opción potente y gratuita para equipos pequeños.

| Herramienta | Tipo de licencia | Beneficios clave | ¿Para qué equipo / contexto? |
| :---- | :---- | :---- | :---- |
| GitHub Projects | Gratuito (con límites) \+ planes pagos | Integración nativa con repositorios, tableros Kanban, Roadmap, automatizaciones básicas | Equipos que ya usan GitHub, proyectos de hasta 10-15 personas, código y gestión en un solo lugar |
| Azure DevOps (Microsoft) | Gratis para hasta 5 usuarios (luego pago) | Ecosistema completo: Boards (Scrum/Kanban), Repos (Git/TFVC), Pipelines (CI/CD), Test Plans, Artifacts. Informes avanzados, integración con GitHub | Equipos de hasta 5 desarrolladores (ideal para proyectos universitarios, startups pequeñas, MVPs). Muy usado en empresas grandes que ya usan Microsoft |
| Jira (Atlassian) | Freemium (hasta 10 usuarios gratis) / Pago | Potente para Scrum y Kanban, informes avanzados (velocity, burn-down), workflows personalizables, integración con Confluence, Bitbucket, GitHub | Equipos grandes (15+), proyectos complejos con múltiples equipos, organizaciones que ya usan ecosistema Atlassian |
| Trello | Freemium (gratuito generoso) / Pago | Sencillez extrema, tableros Kanban visuales, power-ups (incluyendo integración con IA), curva de aprendizaje mínima | Equipos pequeños, proyectos personales, startups tempranas, equipos no técnicos |

### 

### **¿Cuál elegir? Guía rápida de decisión**

| Si tu contexto es... | Recomendación |
| :---- | :---- |
| Proyecto universitario / personal (2-5 personas, presupuesto cero) | GitHub Projects (integración con código) o Azure DevOps (si quieren aprender una herramienta industrial) o Trello (mínima curva) |
| Startup / equipo chico (5-15 personas, buscan velocidad) | Linear o ClickUp (gratuitos hasta 10-15 usuarios) o Azure DevOps (si ya usan Microsoft) |
| Empresa mediana / grande (múltiples equipos, reporting complejo) | Jira (estándar industrial) o Azure DevOps (si la empresa ya usa Microsoft) |
| Equipo con políticas de datos estrictas | Plane o Taiga (auto-hospedados, open source) |
| Equipo multidisciplinario (no sólo ingeniería) | Asana, ClickUp o [Monday.com](https://monday.com/) |
| Quieren aprender una herramienta que sume al CV y sea gratuita | Azure DevOps (gratis 5 usuarios) o Jira (gratis 10 usuarios) |

| 1.6 | GitHub como Ecosistema Ágil |
| :---: | :---- |

Ustedes ya saben git y pull requests. El objetivo de esta sección no es aprender GitHub desde cero, sino usarlo como tablero Scrum completo. GitHub Projects, Issues, Milestones y Discussions cubren todos los artefactos y ceremonias de Scrum sin instalar nada extra.

### **GitHub Projects como tablero Scrum**

GitHub Projects permite crear tableros con tres vistas: Board (Kanban), Table (lista ordenable) y Roadmap (vista temporal). Para un equipo Scrum la vista Board es la más útil en el día a día.

Configuración de columnas recomendada para el Sprint Backlog:

* Product Backlog — Todo lo que aún no ingreso al Sprint  
* Sprint Backlog — Seleccionado para este Sprint (en Planning)  
* In Progress — En desarrollo (máximo 1-2 ítems por persona al mismo tiempo)  
* In Review — PR abierto, esperando revisión  
* Done — Merged, cerrado, cumple el DoD

### **Issues como Product Backlog Ítems**

Cada Issue de GitHub puede representar una Historia de Usuario, un bug, o una tarea técnica. Usar una plantilla de Issue garantiza que todas las historias tengan los elementos necesarios.

| PROMPT SUGERIDO  —  Template de Issue para Historia de Usuario Crear en el repo: .github/ISSUE\_TEMPLATE/historia-de-usuario.md \#\# Historia de Usuario Como \[tipo de usuario\] quiero \[funcionalidad\] para \[beneficio\]. \#\# Criterios de Aceptación \- \[ \] Dado que... cuando... entonces... \- \[ \] Dado que... cuando... entonces... \#\# Notas técnicas (dependencias, restricciones técnicas, etc.) \#\# Definition of Done \- \[ \] Código revisado (mínimo 1 aprobación) \- \[ \] Tests unitarios pasando en CI \- \[ \] PR mergeado con referencia: Closes \#N \- \[ \] Issue cerrado automáticamente |
| :---- |

### **Labels y Milestones**

| Elemento | Uso en Scrum |
| :---- | :---- |
| Labels de tipo | feature, bug, tech-debt, research (que tipo de trabajo es) |
| Labels de prioridad | P0 (critico), P1 (alto), P2 (medio), P3 (bajo) |
| Labels de tamaño | S (menos de 1 dia), M (1-2 dias), L (3+ dias), XL (dividir) |
| Milestones | Cada Milestone \= un Sprint. Título: “Sprint 1” con fecha de cierre \= ultimo dia del Sprint |

### **Pull Requests como parte del Definition of Done**

El PR no es solo un mecanismo técnico: es el artefacto que hace visible el trabajo del equipo y garantiza la calidad del Increment.

* **Branch naming:** feature/US-12-login-oauth, bugfix/US-31-token-expiry, refactor/US-05-db-layer  
* **Título del PR:** feat: implementar recuperación de contraseña vía email (\#12)  
* **Descripción:** que se hizo, por qué, cómo probar, screenshot si aplica, y al final: Closes \#12 (cierra el Issue automáticamente al mergear).  
* Mínimo 1 revisión aprobada antes de mergear a main. Sin excepciones, aunque el equipo sea de 2 personas.  
* Usar Conventional Commits: feat:, fix:, docs:, refactor:, test:, chore: Al final del Sprint, el historial de commits cuenta la historia del Increment.

### **GitHub Discussions (y alternativas) para Retrospectivas asíncronas**

La Retrospectiva es la ceremonia más importante de Scrum. Hacer una capa de reflexión asíncrona antes de la reunión sincrónica mejora drásticamente la calidad de la conversación: cada persona llega con ideas pensadas, no improvisadas sobre la marcha.  
GitHub Discussions es una opción nativa si el repositorio ya está en GitHub. Pero si el equipo no tiene Discussions habilitado o prefiere herramientas más ligeras, existen alternativas igualmente efectivas.

| Herramienta | Cómo se usa | Ventaja |
| :---- | :---- | :---- |
| GitHub Discussions | Categoría “Retrospectivas” con template de 4Ls | Integrado con el repositorio, trazable |
| Google Forms \+ ChatGPT | Formulario anónimo con preguntas 4Ls; la IA sintetiza las respuestas en un resumen | Rápido, anónimo, sin registro adicional |
| Miro / Mural \+ IA | Tablero colaborativo con sticky notes; exportar a texto y usar IA para agrupar temas | Visual, ideal para equipos remotos |
| Documento compartido (Google Docs / Notion) | Cada persona escribe en una tabla con las 4 secciones; la IA resume los patrones | Simple, accesible para cualquier equipo |

| ACTIVIDAD  D —  Configurar el repositorio como entorno Scrum  Configurar el repositorio de su proyecto. Las Épicas identificadas en la Sección 1.4 son el punto de partida para los primeros Issues. Habilitar GitHub Projects en el repositorio. Crear un proyecto con las 5 columnas Scrum. Crear la plantilla de Issue para Historias de Usuario (.github/ISSUE\_TEMPLATE/). Configurar los Labels de tipo, prioridad y tamaño. Crear 2 Milestones: Sprint 1 y Sprint 2 con fechas reales del cuatrimestre. Crear un Issue por cada Épica del Brief (label: “epic”) y asignarlos al Product Backlog. Crear al menos 1 Historia de Usuario hija de la primera Épica usando la plantilla y asignarla al Sprint 1\. |
| :---- |

| ASYNC 1 | Actividad Asincrónica 1 |
| :---: | :---- |

Antes de la Sesión 2, completar las siguientes tareas en su repositorio. Tiempo estimado: 2 horas.

| ACTIVIDAD  —  Actividad Asincrónica 1: Repositorio Scrum completo Completar la configuración del tablero en GitHub Projects si no se terminó en clase. Redactar 5 Historias de Usuario del proyecto usando la plantilla de Issue con criterios de aceptación en Given/When/Then. Al menos 1 Historia por cada Épica del Brief. Crear los 2 Milestones (Sprint 1 y Sprint 2\) con fechas reales y asignar al menos 3 Issues al Sprint 1\. Mejorar el Product Brief generado en clase con contexto adicional (restricciones reales del proyecto, usuarios más definidos). Guardarlo como documento en el repositorio (docs/product-brief.md). Compartir el link del repositorio en el canal del curso antes de la Sesión 2\. |
| :---- |

### **Entregable**

Repositorio de GitHub con: tablero configurado, al menos 5 Issues con template completo, 2 milestones, y Issues asignados al Sprint 1\.

### **Criterio de evaluación**

* Las historias cumplen el criterio INVEST (especialmente Small y Testable).  
* Los criterios de aceptación son verificables (no ambiguos).  
* El tablero refleja el estado real del proyecto.

## **Referencias y recursos**

* Schwaber, K. & Sutherland, J. (2020). The Scrum Guide. scrumguides.org  
* Caroli, P. (2018). Lean Inception. Editora Caroli.  
* Scrum.org — “Do We Need to Rewrite Scrum in the Age of AI?” (2025)  
* Scrum.org — “AI Augmented Scrum Framework” (2026)  
* GitHub Docs — About GitHub Projects: docs.github.com  
* v0.dev (Vercel) — Generacion de componentes UI con IA: v0.dev  
* Bolt.new — Prototipado rapido de apps web con IA: bolt.new