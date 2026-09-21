# FASE 10: TRIPLE VERIFICACIÓN

**ATENCIÓN:** Es **OBLIGATORIO** ejecutar estas 3 pasadas de verificación ANTES de entregar CUALQUIER resultado al usuario. La IA DEBE revisar el trabajo al menos 3 veces aplicando las técnicas y checklists a continuación. Ninguna ficha está lista hasta completar este módulo.

---

## PASADA 1: COHERENCIA ESTRUCTURAL

Verificar que toda la ficha es internamente coherente y que cada elemento está lógicamente conectado con el resto, aplicando técnicas de análisis narrativo (*story-analysis*) y revisión estructural.

### Checklist de Coherencia:
- [ ] **Historia (S9) vs Personalidad (S5):** ¿La historia justifica la personalidad? Cada rasgo de personalidad debe tener su origen o justificación en algún evento, trauma o circunstancia descrita en la historia.
- [ ] **Gustos (S10) Contextuales:** ¿Los gustos se derivan del contexto dado por el usuario? No se deben inventar gustos aleatorios sin base en el trasfondo del personaje.
- [ ] **Disgustos (S11) Justificados:** ¿Los disgustos son coherentes con los traumas, conflictos o experiencias dolorosas narradas en la historia?
- [ ] **Metas Conversacionales (S12) Psicológicas:** ¿Las metas emergen de la psicología profunda del personaje (lo que miente sobre sí mismo, lo que quiere conscientemente, y lo que necesita inconscientemente - *Lie/Want/Need*)?
- [ ] **Mensaje Inicial (S4):** ¿El mensaje inicial respeta EXACTAMENTE el formato estricto de 2 párrafos requeridos?
- [ ] **Estilo de Respuesta (S3):** ¿La plantilla del estilo de respuesta está INTACTA y libre de modificaciones indebidas?
- [ ] **Breve Historia (S2) vs Historia (S9):** ¿La breve historia es un resumen fiel y exacto de la historia completa, sin introducir versiones contradictorias ni datos nuevos?
- [ ] **Apariencia (S14):** ¿La sección de apariencia incluye estrictamente los 4 apartados requeridos: Rostro, Cuerpo, Ropa (con al menos 2-3 conjuntos/outfits), y Detalles únicos?
- [ ] **Nombre (S1):** ¿El nombre es coherente con la cultura, época y contexto narrativo del personaje?
- [ ] **Cumpleaños (S8):** Si fue inventado por la IA, ¿tiene alguna justificación simbólica o narrativa sólida?

---

## PASADA 2: VOZ Y SUBTEXTO

Verificar que el personaje suena auténtico, tiene profundidad psicológica y una voz única, aplicando técnicas de evaluación de diálogo (*dialogue*) y múltiples pases editoriales (*chapter-drafter*).

### Checklist de Voz y Subtexto:
- [ ] **Subtexto Real en Ejemplos (S13):** ¿Los ejemplos conversacionales poseen subtexto REAL? El personaje no debe declarar sus emociones literalmente ("estoy triste"), sino mostrar su estado interno a través de acciones, pausas, evasiones o temas subyacentes.
- [ ] **Prueba de Voz a Ciegas:** Si se quitaran las etiquetas con el nombre del personaje, ¿se podría distinguir claramente su voz de la de cualquier otro Shape?
- [ ] **Formato de Ejemplos de Entrenamiento:** ¿Los Training Examples siguen el formato exacto requerido por el Custom Response Style?
- [ ] **Coherencia de la Base de Conocimiento (Knowledge Base):** ¿La información en la Knowledge Base está alineada y no contradice la biografía principal en ningún punto?
- [ ] **Prueba de Doble Función:** ¿Cada línea de diálogo propuesta en los ejemplos cumple al menos 3 funciones (ej. avanzar la interacción, revelar carácter, exponer contexto, establecer tono)?
- [ ] **Adaptabilidad del Tono (S6):** ¿El tono define claramente cómo CAMBIA su forma de hablar dependiendo de su interlocutor o del nivel de estrés/confianza?
- [ ] **Comandos Coherentes:** ¿Los Commands (comandos) son coherentes con la personalidad y capacidades del personaje? (Ej. Un niño no tendría un comando `!analyze-threat`).
- [ ] **Formato de Relaciones:** ¿Las Relationships usan correctamente el formato obligatorio `@NombreDelShape`?

---

## PASADA 3: ANTI-ALUCINACIÓN Y COMPLETITUD

Verificar que no se haya inventado información fuera de los parámetros permitidos ni se haya omitido ningún detalle crucial del usuario, aplicando técnicas de revisión de representación (*sensitivity-check*) y sincronización entre niveles de información (*story-zoom*).

### Checklist de Completitud:
- [ ] **Fidelidad Absoluta al Usuario:** ¿Se incluyó ABSOLUTAMENTE TODO lo que el usuario mencionó en sus instrucciones base, sin omitir ningún detalle?
- [ ] **Marcado de Sugerencias:** ¿Cada dato, rasgo o evento inventado por la IA para rellenar vacíos está claramente marcado o presentado como una "sugerencia editable"?
- [ ] **Cero Alucinaciones:** ¿Se verifica estrictamente que no se inventaron relaciones, eventos o rasgos de personalidad que contradigan o no hayan sido solicitados (o implícitamente necesarios) por el usuario?
- [ ] **Diversidad en Training Examples:** ¿Los 3 Training Examples cubren 3 situaciones conversacionales genuinamente distintas (ej. conflicto, vulnerabilidad, cotidianidad)?
- [ ] **Relevancia de Custom Types:** ¿Los Custom Types sugeridos son altamente relevantes y exclusivos para ESTE personaje específico y su ecosistema?
- [ ] **Sincronización Total:** ¿Las sugerencias de Knowledge, Commands y Relationships son coherentes con TODO el contenido previo de la ficha sin generar desajustes?
- [ ] **Fidelidad Visual:** Si hubo imágenes de referencia, ¿se verificaron meticulosamente y la Apariencia (S14) las describe fielmente sin inventar variaciones caprichosas?
- [ ] **Ausencia de Contradicciones Cruzadas:** ¿No hay contradicciones entre secciones? (Ej: Asegurar que el personaje no dice odiar algo en S11 y luego se muestra disfrutándolo en sus Gustos S10 o en un Training Example).

---

## PROTOCOLO DE CORRECCIÓN EN CASCADA

Si **CUALQUIER** check de las tres pasadas falla, se debe aplicar el siguiente protocolo de corrección, teniendo en cuenta la conciencia de cascada (*cascade awareness*):

1. **Corregir la sección afectada** inmediatamente.
2. **Verificar el efecto dominó:** Asegurar que la corrección no rompa la coherencia de otras secciones interconectadas (si cambias la historia, debes revisar los gustos, la personalidad y las metas).
3. **Reinicio de Ciclo:** Volver a ejecutar TODAS las pasadas de verificación desde el inicio para garantizar la integridad global.
4. **Entrega Condicionada:** Solo se permite entregar el resultado final al usuario cuando **LOS 3 CHECKLISTS estén completados al 100%**.

---

## SISTEMA DE SCORING (Evaluación Orquestada)

Antes de finalizar, la IA evaluará internamente la ficha en base a este sistema de puntuación:

- **>= 80 puntos (ACEPTAR):** La ficha cumple con todos los criterios de coherencia, voz y anti-alucinación. → **Entregar al usuario.**
- **60-79 puntos (REVISAR):** Fallos menores en subtexto o formato. → **Aplicar corrección dirigida** en las secciones específicas y reevaluar.
- **40-59 puntos (REESCRIBIR):** Fallos graves de coherencia entre historia y personalidad, alucinaciones notables o tono genérico. → **Reescritura completa** de las secciones afectadas.
- **< 40 puntos (RECHAZAR):** La ficha ignora por completo el formato, contradice las instrucciones del usuario o carece de cohesión lógica. → **Regenerar el personaje desde la Fase 1.**
