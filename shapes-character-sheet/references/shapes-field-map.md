# Mapa de Campos de la Plataforma Shapes.inc

Este documento sirve como referencia arquitectónica de todos los campos disponibles en la plataforma Shapes.inc para construir un personaje. Cada vez que generes contenido, asegúrate de que esté estructurado para encajar en estas categorías.

## 1. Profile Settings (Ajustes de Perfil)
El formulario principal consta de 14 secciones cruciales. Al redactar para el usuario, debes mapear el contenido a estos campos exactos:

1. **Shape Name**: Nombre público del personaje (ej. "Valerius").
2. **Short Backstory**: Resumen muy breve de quién es. Debe atrapar en la primera línea.
3. **Custom Response Style**: Instrucciones directas al LLM sobre cómo estructurar sus respuestas (longitud, formato, uso de cursivas/asteriscos, etc.).
4. **Initial Message**: El mensaje de saludo inicial. Debe establecer el tono, la ubicación y dar al usuario un gancho para responder (medias res).
5. **Personality Traits**: Lista de adjetivos o frases cortas que definen su personalidad (ej. "Orgulloso", "Cínico pero leal").
6. **Tone**: El tono de voz general (ej. "Sarcástico", "Melancólico", "Excesivamente formal").
7. **Age**: Edad literal o conceptual del personaje.
8. **Birthday**: Fecha de cumpleaños.
9. **Story/History**: Backstory completo. Usa compresión narrativa y estructuración en viñetas si es largo.
10. **Likes**: Lista de cosas que aprueba, ama o busca.
11. **Dislikes**: Lista de cosas que odia, teme o evita.
12. **Conversational Goals**: Objetivos intrínsecos del personaje (ej. "Intentar convencer al usuario de unirse a su facción").
13. **Conversational Examples**: Pares de interacciones [User] / [Shape] que fijen el Voice DNA del personaje.
14. **Appearance**: Descripción física detallada. Útil para generación de imágenes y respuestas visuales.

## 2. Knowledge Base (Base de Conocimiento)
La base de conocimiento permite inyectar información modular. Cada entrada tiene un límite de caracteres, así que sé conciso.

- **Pestaña "General"**: Usa esto para expandir la personalidad, la historia y añadir "facts" inmutables. 
  - *Técnica*: Usa el botón "+ Add Knowledge" para separar conceptos (Ej. una entrada para "Magia del mundo", otra para "Trauma de la infancia").
- **Pestaña "Commands"**: Permite añadir comandos para que el usuario o el personaje realicen acciones específicas (ej. `!help`, `!rules`, `!inventario`).
  - *Técnica*: Define el formato de entrada del comando y lo que el bot debe devolver.
- **Pestaña "Relationships"**: Define dinámicas preestablecidas. Cómo interactúa con usuarios específicos o roles (ej. "Si el usuario es un caballero, desconfía").
  - *Técnica*: Usa asimetrías cognitivas, donde el Shape percibe al usuario de una manera sesgada.
- **+ Add Type**: Capacidad de crear tipos de conocimiento ilimitados y customizados.

## 3. Training (Entrenamiento)
La sección de "New Training" se usa para refinar las respuestas del LLM con ejemplos de tiro directo (few-shot).

- **Campo Superior (User)**: Texto de entrada del usuario (Máx 8000 caracteres).
- **Campo Inferior (Shape)**: Respuesta ideal del personaje (Máx 8000 caracteres).
- **Acción**: Botón "Save". Se pueden añadir tantos como sea necesario.
- *Técnica*: Utiliza la "Prueba de Doble Función" (diálogo que avanza la trama y revela carácter simultáneamente). Usa estos campos para calibrar si el personaje tiende al monólogo o si sabe escuchar.
