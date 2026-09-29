# Shapes-creator v3

Este repositorio contiene la versión 3 de la skill `character-creator-shapes-pro`, una super-skill orquestadora para la creación completa de personajes ("shapes") en https://talk.shapes.inc/ y adaptada con enfoque nativo para LM Studio.

Genera las 14 secciones del formulario principal (shapes) o un System Prompt unificado (LM Studio) + Knowledge Base expandida + Training Examples + sistema de memoria situacional con @menciones entre personajes.

## Indicaciones de la Skill
Esta es una skill orquestadora que se compone de 14 módulos de procesamiento secuencial.

### Reglas Fundamentales
- NO hay límite de caracteres en ninguna sección.
- NO se recorta información para encajar en un límite.
- SIEMPRE verificar 3 veces antes de entregar.
- SIEMPRE incluir sugerencias post-generación.

### Flujo de Trabajo (11 Fases)
- **PROTO 00**: Investigación / tools (`00-research-protocol.md`)
- **FASE 1**: Reunir Contexto (`01-context-gathering.md`)
- **FASE 2**: Filtro Anti-Cliché (`02-anti-cliche-filter.md`)
- **FASE 3**: Núcleo Psicológico (`03-psychological-core.md`)
- **FASE 4**: Auditoría de Mundo (`04-worldbuilding-check.md`)
- **FASE 5**: ADN Verbal (`05-voice-dna.md`)
- **FASE 6**: Generar 14 Secciones (`06-section-generator.md`)
- **FASE 7**: Knowledge Base (`07-knowledge-base.md`)
- **FASE 8**: Training Examples (`08-training-examples.md`)
- **FASE 9**: Sistema de Memoria (`09-memory-system.md`)
- **FASE 10**: Triple Verificación (`10-triple-verification.md`)
- **FASE 11**: Entrega + Sugerencias (`11-post-generation.md`)
- **FASE 12**: 2 imágenes de referencia (`12-reference-images.md`)

Todo este proceso está diseñado para entregar una ficha lista, profunda y libre de clichés.