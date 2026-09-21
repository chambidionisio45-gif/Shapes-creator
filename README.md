# Shapes Character Sheet v2.0

Una "Super-Skill Orquestadora" diseñada para la creación completa, profunda y estructurada de personajes (Shapes) para [shapes.inc](https://talk.shapes.inc/) y adaptada con un enfoque nativo para [LM Studio](https://lmstudio.ai/).

Este repositorio contiene las instrucciones, flujos de trabajo (11 fases) y reglas fundamentales que permiten a un agente de IA transformar imágenes de referencia y texto de contexto en una **Ficha de Personaje Completa** lista para ser utilizada.

## 🌟 Características Principales

- **Sin Límites de Caracteres**: Generación detallada de todas las secciones sin recortes de información (el antiguo límite de 3000 caracteres ha sido eliminado).
- **Formato Dual**: Optimizado tanto para generar las 14 secciones del formulario de Shapes.inc como para un *System Prompt* unificado en LM Studio.
- **Knowledge Base Expandida**: Generación de conocimientos generales, comandos (`!comando`), relaciones cruzadas (`@mención`) y tipos personalizados (*Custom Types*).
- **Training Examples**: Creación de situaciones de entrenamiento conversacional (mínimo 3 situaciones variadas: casual, emocional y de acción/rol) siguiendo estrictamente el formato de respuesta del bot de dos párrafos.
- **Sistema de Memoria Inter-Personajes**: Vinculación de personajes mediante menciones (`@Personaje`), creando una red de memoria compartida, asimetrías de información y relaciones bidireccionales.
- **Triple Verificación**: Un sistema de control de calidad de 3 pasadas obligatorio antes de la entrega para asegurar coherencia estructural, tono de voz y evitar alucinaciones.
- **Sugerencias Interactivas**: Un menú post-generación al final del proceso para expandir la base de conocimientos, agregar comandos, editar secciones específicas, generar más interacciones o interconectar personajes.

## 🗂️ Estructura del Repositorio

El repositorio está organizado de la siguiente manera:

- `SKILL.md`: El archivo principal (orquestador). Contiene las reglas maestras, la explicación del flujo general de las 11 fases y las consideraciones previas. Es el punto de entrada para comprender y ejecutar la skill.
- `modules/`: Contiene el detalle exhaustivo de cada una de las 11 fases del proceso creativo. Cada archivo define las instrucciones y las *skills* integradas necesarias para completar esa fase.
  - `01-context-gathering.md`: Fase 1 (Reunir contexto e imágenes).
  - `02-anti-cliche-filter.md`: Fase 2 (Prevención de personajes genéricos usando métricas de distancia).
  - `03-psychological-core.md`: Fase 3 (Creación del arco: mentira, deseo, herida y necesidad).
  - `04-worldbuilding-check.md`: Fase 4 (Auditoría del mundo en caso de sci-fi/fantasía/histórico).
  - `05-voice-dna.md`: Fase 5 (Construcción del estilo de diálogo, registro y subtexto).
  - `06-section-generator.md`: Fase 6 (Generación de las 14 secciones principales del formulario).
  - `07-knowledge-base.md`: Fase 7 (Elaboración de la base de conocimientos y comandos).
  - `08-training-examples.md`: Fase 8 (Ejemplos conversacionales y de entrenamiento).
  - `09-memory-system.md`: Fase 9 (Gestión de relaciones cruzadas y memoria de sesión).
  - `10-triple-verification.md`: Fase 10 (Verificación obligatoria de calidad).
  - `11-post-generation.md`: Fase 11 (Entrega final, formato de salida y menú de sugerencias).
- `references/`: Documentación de soporte para el orquestador, definiendo estándares e índices.
  - `integration-index.md`: Índice de las 53 sub-skills literarias y de rol integradas en el flujo.
  - `quality-gates.md`: Explicación del sistema de compuertas de calidad (Scoring) para aceptar, revisar, reescribir o rechazar generaciones.
  - `shapes-field-map.md`: Mapeo de los campos específicos de Shapes.inc.

## ⚙️ Cómo Funciona (El Flujo de 11 Fases)

La creación de un personaje no ocurre de golpe; sigue un flujo narrativo y analítico secuencial muy estricto:

1. **Contexto**: Se analiza todo lo provisto por el usuario (texto e imágenes). Se hacen preguntas iniciales si falta información clave (por ejemplo, la edad obligatoria).
2. **Filtro Anti-Cliché**: Se asegura de que el personaje sea único, ortogonal a los tropos genéricos y narrativamente profundo.
3. **Psicología**: Se define su mundo interno: el trauma, la necesidad real y las justificaciones psicológicas.
4. **Mundo**: (Solo para ficción) Se evalúa cómo el mundo o universo afecta al personaje de manera sistémica.
5. **Voz**: Se define *cómo* habla, su nivel de formalidad y la diferencia entre lo que dice y lo que siente (subtexto).
6. **Las 14 Secciones**: Se redactan de manera estructurada (empezando por la apariencia visual y fluyendo hacia la historia).
7. **Conocimientos**: Se añaden datos extra, comandos que el bot puede ejecutar y *custom types*.
8. **Entrenamiento**: Se redactan los ejemplos de interacción base.
9. **Memoria**: Se conecta con otros Shapes si fueron mencionados en la sesión.
10. **Triple Verificación**: Control de calidad (Coherencia Estructural, Voz/Subtexto y Anti-Alucinación). Si algo falla, se aplica corrección en cascada.
11. **Entrega**: Se presenta el resultado al usuario mediante bloques de código fáciles de copiar, junto a un menú interactivo para iterar y mejorar la ficha.
