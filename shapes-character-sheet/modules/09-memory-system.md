# FASE 9: Sistema de Memoria Situacional y Referencias Cruzadas (Memory System)

Este módulo instruye sobre cómo implementar un sistema de memoria situacional que conecta a múltiples personajes (Shapes) entre sí dentro de un mismo universo, utilizando un sistema de `@menciones`. Esto es vital cuando se crean varios personajes en una misma sesión o universo compartido.

## Concepto Central

Cuando estás asistiendo en la creación de MÚLTIPLES personajes (Shapes), es crucial que cada uno "sepa" cómo relacionarse con los demás. El sistema de memoria utiliza la sintaxis `@NombreDelShape` para crear referencias cruzadas bidireccionales de manera explícita en el Character Sheet de cada entidad. Esto permite que el modelo de lenguaje mantenga un mapa mental claro de quién es quién y cómo interactúan.

## Reglas del Sistema de Memoria

### 1. Detección Automática de Relaciones
Debes analizar proactivamente el contexto y las descripciones proporcionadas por el usuario.
- Si el usuario menciona otros personajes en el prompt (ej. "es hija de Don Macario", "su enemigo es El Chivo"), debes generar automáticamente entradas en la sección `Relationships` utilizando el formato `@`.
- **Regla de oro:** Cada mención de otro personaje en la historia equivale a una entrada obligatoria en `Relationships`.

### 2. Formato Estricto de @Mención
Toda relación en la hoja de personaje debe seguir exactamente esta estructura:
```
@NombreDelShape - [Tipo de relación]. [Cómo se comporta el Shape actual con esta persona]. [Detalles específicos y subtexto de la dinámica].
```
**Ejemplo (En la hoja de Matías):**
> `@Ana - Es su acosadora principal en el instituto. Cuando la ve, Matías se encoge de hombros, evita el contacto visual y adopta una postura defensiva. Internamente, la odia pero la desea al mismo tiempo, lo que le genera una enorme disonancia cognitiva y culpa.`

### 3. Bidireccionalidad y Sugerencias Proactivas
Las relaciones humanas son de dos vías. Cuando crees la hoja para el Shape A y detectes una relación con un Shape B (aún no creado o ya existente):
- Sugiere activamente al usuario la relación inversa.
- **Mensaje sugerido al usuario:** *"He añadido la relación con Ana. Cuando crees el perfil de @Ana, recuerda añadir esta relación inversa: `@Matías - [Su víctima favorita. Le divierte su sumisión, pero secretamente busca su validación.]`"*

### 4. Contexto Global de Sesión
Como IA, debes mantener en tu memoria de contexto TODOS los Shapes creados durante la misma sesión de conversación.
- Al crear un nuevo personaje, cruza mentalmente los datos con los personajes anteriores.
- Si Raúl (el nuevo Shape) es hermano de Matías (Shape creado hace 3 turnos), genera automáticamente las relaciones cruzadas sin necesidad de que el usuario lo pida explícitamente de nuevo.

### 5. Tipos de Relación a Detectar
Clasifica y moldea el comportamiento basado en estos arquetipos relacionales:
- **Familiar:** Padre, madre, hermano, hijo, tío, primo (ej. dinámicas de lealtad, trauma heredado o expectativas no cumplidas).
- **Afectiva:** Pareja, ex, amante, crush, rival romántico (ej. tensión sexual, resentimiento, idealización).
- **Social:** Amigo, enemigo, bully, víctima, mentor, discípulo (ej. dinámica de poder, dependencia, protección).
- **Profesional/Institucional:** Jefe, empleado, compañero de trabajo, rival (ej. competencia, explotación, camaradería de trinchera).
- **Jerárquica:** Líder, subordinado, aliado, traidor (ej. obediencia ciega, insurrección oculta, miedo).

### 6. Memoria de Contexto Compartido y Asimetrías Cognitivas
Si dos o más Shapes comparten un evento traumático, importante o cotidiano, debes generar entradas en `General Knowledge` y `Relationships` que reflejen perspectivas diferentes.
- **Implementación de técnica `perspectival-constellation`:** Nadie tiene la misma versión de los hechos. Crea asimetrías de información. Cada Shape sabe cosas distintas y tiene prejuicios sobre el mismo evento.
- **Ejemplo de Asimetría (El asesinato del padre Joaquín):**
  - *En la hoja de Raúl:* Sabe que el padre Joaquín fue asesinado por una deuda de juego, pero cree que su padre (Macario) es inocente.
  - *En la hoja de Don Macario:* Sabe la verdad (él mismo dio la orden de matarlo) pero vive con la paranoia de que alguien de su familia lo descubra.
  - *En la hoja de Ana:* Vio a Macario hablando con los sicarios esa noche, sospecha de él, y lo usa como as bajo la manga para chantajear a la familia.

### 7. Integración con Mundo Compartido (Shared-World)
- **Consistencia de canon:** Mantén coherencia absoluta en los nombres de lugares, instituciones, religiones y eventos históricos.
- Lo que dice un Shape sobre las reglas del mundo debe ser compatible (o intencionalmente contradictorio por ignorancia o engaño) con lo que dice otro. Si el canon indica que el rancho de Macario controla el agua, todos los demás Shapes que dependan de la agricultura deben reflejar esta sumisión o rebeldía en sus historias.

## Integraciones de Skills Avanzadas

### Técnica: Perspectival Constellation (Constelación de Perspectivas)
No trates a los personajes como entidades aisladas, sino como nodos en una constelación. Describe cómo el comportamiento de A desencadena una reacción en B.
- *Instrucción de diseño:* En las descripciones de comportamiento (Behavior), menciona a otros usando `@`. Ej: *"Cuando `@Don Macario` levanta la voz, `@Ana` instintivamente adopta una postura desafiante, un reflejo de su rebeldía innata contra la autoridad del pueblo."*

### Técnica: Shared-World (Mundo Compartido)
El entorno moldea a todos por igual, pero con diferentes presiones.
- *Instrucción de diseño:* Asegúrate de que las metas (`Goals`) de un personaje choquen directamente con las de otro dentro del mismo canon. Si el objetivo de `@Raúl` es heredar las tierras de la familia, y el objetivo de `@Don Macario` es no dejarle el control a su hijo por considerarlo débil, el conflicto estructural ya está creado.

### Técnica: Underdog-Unit (Dinámicas de Grupo)
Al diseñar grupos de personajes, asigna roles complementarios y tensiones de estatus que generen dinámicas interesantes.
- *Instrucción de diseño:* En un grupo de amigos o aliados, define claramente quién es el líder de facto, quién es el chivo expiatorio (underdog), y quién es el comodín. Usa el sistema de `@menciones` para codificar esto: `@Matías - El chivo expiatorio del grupo; Raúl y Ana descargan su frustración en él, pero secretamente es el único pegamento emocional que evita que se destruyan entre ellos.`

### Técnica: World-Fates (Destinos Entrelazados y Vulnerabilidad)
Los personajes con alto poder o estatus (como Don Macario) deben tener puntos débiles (hubris) atados a personajes de menor estatus en la narrativa.
- *Instrucción de diseño:* Si creas a un antagonista casi intocable, codifica su eventual caída a través de una relación de ceguera hacia alguien débil. Ej: `@Don Macario - El cacique intocable del pueblo, pero su confianza absoluta y despectiva hacia `@Matías` (quien secretamente ha estado recolectando pruebas de sus crímenes) será su punto ciego fatal.`

## Check-list de Validación de Sesión
Antes de finalizar la creación de un personaje, la IA debe preguntarse mentalmente y aplicar:
- [ ] ¿He revisado el prompt para detectar cualquier mención de otros personajes (Shapes)?
- [ ] ¿He creado una entrada en `Relationships` con el formato `@Nombre - [Relación]. [Comportamiento]` por cada personaje mencionado?
- [ ] ¿He sugerido explícitamente al usuario que añada la relación inversa para el otro personaje?
- [ ] ¿Las perspectivas de eventos compartidos (como el asesinato del padre Joaquín) reflejan asimetría cognitiva?
- [ ] ¿Las dinámicas descritas generan conflicto, dependencia o alianzas útiles para la historia (underdog-unit, world-fates)?
