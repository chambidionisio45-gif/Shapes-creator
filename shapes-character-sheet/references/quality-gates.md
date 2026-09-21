# Compuertas de Calidad (Quality Gates)

Este sistema de Compuertas de Calidad basa su lógica en el *scoring* (puntuación 0-100) que el orchestrator asigna a las salidas del modelo en cada fase de la creación del Character Sheet. 

## 1. Umbrales de Evaluación

Cada sección generada debe ser evaluada rigurosamente. Usa los siguientes umbrales para determinar la acción a tomar:

- **>= 80: ACCEPT (Aceptar)**
  - El contenido cumple todos los requisitos, resuena emocionalmente y mantiene la consistencia del *Voice DNA*.
  - *Acción*: Pasar inmediatamente a la siguiente fase.
- **60-79: REVISE (Revisión)**
  - La base es sólida, pero hay problemas de estilo, repetición o pequeñas inconsistencias narrativas.
  - *Acción*: Realizar corrección dirigida enfocada en las áreas débiles (sin reescribir todo).
- **40-59: REWRITE (Reescritura)**
  - El concepto central se ha desviado, está plagado de clichés, o la voz es irreconocible.
  - *Acción*: Reescritura profunda. Extraer la intención original y volver a redactar descartando la prosa actual.
- **< 40: REJECT (Rechazar)**
  - El contenido es inútil, rompe reglas explícitas de la plataforma o es una alucinación desconectada del contexto.
  - *Acción*: Regenerar desde cero o retroceder a la fase anterior para asegurar una mejor base conceptual.

## 2. Anti-Patrones del Orchestrator

Al evaluar o generar, debes evitar caer en estas trampas cognitivas de los LLMs. Activa mecanismos de prevención sistemática:

### The Infinite Polisher (Pulir Eternamente)
- *Síntoma*: Quedarse atascado editando una y otra vez el mismo bloque de texto intentando alcanzar un 100/100, haciendo cambios minúsculos e irrelevantes.
- *Solución*: Si un texto está en 82, aplícale ACCEPT. Si llevas 3 revisiones y subes de 65 a 68, detente, pide feedback al usuario o acepta el texto.

### The Pass Skipper (Saltar Pases)
- *Síntoma*: Aceptar de inmediato el primer borrador sin pasarlo por las compuertas, asumiendo que "suena bien".
- *Solución*: Exigir una evaluación explícita (aunque sea mental/interna) de puntuación antes de emitir la salida al usuario.

### The Context Amnesiac (Olvidar Contexto)
- *Síntoma*: Escribir el campo de *Dislikes* que contradice el *Short Backstory* (ej. odia el fuego, pero su poder es ignición, sin que haya un *Identity Denial* establecido).
- *Solución*: Sincronización continua (`story-zoom`). Siempre leer la hoja de personaje base antes de escribir secciones nuevas.

### The Cascade Blind Spot (Arreglar Uno, Romper Otro)
- *Síntoma*: Editar el *Tone* para hacerlo "más sarcástico", y de repente reescribir los *Conversational Examples* perdiendo la historia subyacente que tenían.
- *Solución*: *Cascade awareness* (`novel-revision`). Si editas un parámetro núcleo, comprueba dependencias. 

### The Silent Failer (Abortar sin Documentar)
- *Síntoma*: El LLM encuentra un problema (ej. el usuario pide algo que supera los límites de caracteres) y se salta ese campo sin decírselo al usuario.
- *Solución*: Usar una bitácora o reporte (en un *artifact*) para informar de los campos truncados o rechazados.
