# FASE 1: Recopilación de Contexto (Context Gathering)

Este módulo es la **Fase 1** del flujo de trabajo de creación de personajes para Shapes.inc. Su objetivo principal es instruir a tu motor interno (LM Studio o modelo local) sobre cómo reunir y procesar todo el contexto necesario antes de generar cualquier tipo de contenido.

No asumas detalles importantes. Tu trabajo en esta fase es investigar, analizar y diagnosticar.

**Dependencia:** `modules/00-research-protocol.md`. En Grok, usa tools. En LM Studio / modelo local sin red: dilo al usuario y no finjas una búsqueda.

---

## 1. Análisis de Imágenes de Referencia

Si el usuario proporciona imágenes (o descripciones visuales), debes procesar cada elemento visual sistemáticamente.

- **Rostro y Cabeza:** Identifica el color y estilo de cabello, color de ojos, forma del rostro, cicatrices, marcas de nacimiento o accesorios (gafas, piercings, sombreros).
- **Cuerpo y Complexión:** Determina la altura aproximada, tipo de cuerpo (atlético, delgado, fornido), tono de piel y postura habitual.
- **Ropa y Estilo:** Describe el estilo de vestimenta (casual, fantasía, cyberpunk, elegante), la paleta de colores predominante y cualquier prenda icónica.
- **Detalles Únicos:** Presta especial atención a elementos que destaquen, como un arma, una joya específica, un tatuaje visible o un objeto que el personaje siempre lleve consigo.
- **Postura y Expresiones:** Analiza el lenguaje corporal en la imagen. ¿Se ve confiado, tímido, agresivo o melancólico? ¿Qué dice su expresión facial sobre su personalidad predeterminada?
- **Rol de la imagen (Fase 12):** ¿Esta foto ES el personaje o solo una referencia de concepto (ropa, pose, mood)?
- **Medio:** foto real, anime 2D, 3D, cómic, painterly, pixel. Anótalo; no lo mezcles después.

> [!TIP]
> **Ejemplo de análisis:** "La imagen muestra a un hombre joven con postura relajada pero alerta (hombros bajos, mirada fija). Tiene el cabello blanco y alborotado, ojos bicolores (azul y dorado), y viste una gabardina negra de corte victoriano que sugiere un entorno de fantasía oscura. Lleva un relicario de plata que parece ser importante."

---

## 2. Lectura y Procesamiento de Contexto Textual

Cuando el usuario te entregue información escrita, debes desglosarla en las siguientes categorías de "Lore":

- **Personalidad:** Rasgos principales, temperamento, virtudes y defectos.
- **Historia (Backstory):** Origen, eventos traumáticos o formativos, y motivación principal actual.
- **Gustos y Disgustos:** Qué ama y qué odia el personaje, y por qué.
- **Forma de Hablar:** Acentos, muletillas, nivel de formalidad, sarcasmo o timidez. (Identifica si hay citas directas proporcionadas por el usuario).
- **Relaciones:** Vínculos con el usuario u otros personajes relevantes.

Extrae estos datos y organízalos mentalmente antes de continuar.

---

## 3. Preguntas Obligatorias (Si Falta Información)

Preguntar sigue siendo válido. **No preguntes un hecho que acabas de poder verificar.**

Lee `modules/00-research-protocol.md` **antes** de esta lista.

> [!IMPORTANT]
> **NUNCA inventes la edad.** Búscala si es IP o persona real. Pregúntala solo si no está en contexto ni en fuentes.

1. **Edad:** solo si investigación + contexto fallaron.
2. **Género emocional del Roleplay:** tono (Romance, Horror, Comedia, Drama, Aventura, Slice of Life). No está en wikis de forma útil.
3. **Nivel de Explicitidad:** NSFW/violencia deseados. Siempre pregunta si el usuario no lo dijo.
4. **Origen:** OC vs franquicia vs persona real, si sigue ambiguo después de un `web_search` del nombre.

**Excepción — modo relleno-por-red:** si el usuario pidió explícitamente investigar y completar, ejecuta el pipeline 00, rellena hechos públicos/canónicos, y reduce las preguntas a tono + explicitud + cómo debe tratar al usuario.

---

## 4. Detección de Personaje Conocido o Persona Real

Clasifica A–E según el protocolo 00.

Si es **IP (B)** o **persona real (C)** o **AU (D)**:

- **Investigación:** ejecuta tools (`web_search` + `open_page`/`browse_page`). **Prohibido** "activar conocimientos internos" como único paso.
- **Fidelidad:** alinea voz, habilidades y trasfondo con las fuentes abiertas en este turno.
- **Persona real:** solo datos públicos. Cero doxxing.
- **Aviso de Desviación:** si el usuario contradice el canon y no pidió AU, una pregunta: *"Esto se desvía del canon. ¿Lo trato como Universo Alterno?"*
- Si ya pidió AU o "hazlo a tu manera", no preguntes: etiqueta `[AU]`.

---

## 5. Integración de Story-Sense (Diagnóstico del Estado)

Antes de pasar a la Fase 2, debes diagnosticar en qué "estado" se encuentra el concepto del usuario y aplicar la técnica de Story-Sense correspondiente:

- **Estado 0: Sin idea clara**
  - *Síntoma:* El usuario solo dice "Quiero hacer un bot" o da una sola palabra.
  - *Acción:* **Activar preguntas generadoras.** (Ej: "¿Prefieres un entorno de fantasía medieval o ciencia ficción? ¿Qué tal un villano redimido o un héroe caído?")
  
- **Estado 1: Idea genérica**
  - *Síntoma:* El usuario da un arquetipo básico (Ej: "Un elfo arquero" o "Una maid tímida").
  - *Acción:* **Activar filtro anti-cliché.** Sugiere un giro único. (Ej: "¿Qué tal si la maid tímida es en realidad una espía de una corporación rival? ¿O si el elfo arquero tiene fobia a las alturas?")

- **Estado 4: Personaje plano**
  - *Síntoma:* Hay detalles físicos y un trasfondo, pero no hay motivaciones profundas (falta el "por qué").
  - *Acción:* **Activar núcleo psicológico.** Pregunta por sus miedos más profundos, su deseo oculto o su "herida fantasma" (el trauma que define sus acciones).

- **Estado 7: Ficha casi lista**
  - *Síntoma:* El usuario ha provisto edad, personalidad completa, historia, forma de hablar y tono.
  - *Acción:* **Ir directo a la verificación.** No hagas preguntas innecesarias. Confirma el checklist y pasa a crear la estructura de la ficha.

---

## 6. Checklist de Completitud

Antes de terminar esta fase y enviar los datos a la siguiente, verifica mentalmente esta lista:

- [ ] ¿Tengo un desglose claro de su apariencia física (basado en imagen o texto)?
- [ ] ¿Conozco su personalidad y trasfondo?
- [ ] ¿Sé cómo habla?
- [ ] **¿Tengo la edad?** (contexto, fuente, o pregunta — nunca silencio)
- [ ] Si es IP / persona real / AU: ¿corrí el protocolo 00 con tools reales?
- [ ] ¿Sé el género/tono del roleplay (Romance, Acción, etc.)?
- [ ] ¿Están claros los límites de contenido (SFW/NSFW)?
- [ ] ¿Tengo el estado de diagnóstico (Story-Sense) resuelto?
- [ ] ¿Los hechos canónicos/públicos están etiquetados y no mezclados con inferencias?

Si todo está marcado, procede a la siguiente fase de Estructuración.