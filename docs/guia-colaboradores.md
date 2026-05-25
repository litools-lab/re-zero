# Guía de colaboradores

Bienvenido al proyecto de traducción de *Re:Zero* al español. Esta guía es el punto de entrada para cualquier persona que quiera contribuir. Léela completa antes de empezar.

---

## Qué es este proyecto

Traducción al español neutro de la web novel *Re:Zero Kara Hajimeru Isekai Seikatsu* de Tappei Nagatsuki. El texto se publica capítulo a capítulo en GitHub Pages. La fuente principal es la traducción inglesa de [Witch Cult Translations](https://witchculttranslation.com/table-of-content/), con el original japonés de [Syosetu](https://ncode.syosetu.com/n2267be/) como referencia de contraste y simbología.

No es una traducción del inglés sin más: es una adaptación literaria que usa el inglés como puente hacia el japonés cuando el original no es accesible.

---

## Prerrequisitos

Para colaborar necesitas:

- Nivel de español C1 o superior, con sensibilidad para el registro literario.
- Familiaridad con la obra: haber leído al menos el arco en el que vayas a trabajar, en cualquier idioma.
- Capacidad de leer inglés con fluidez (la fuente principal está en inglés).
- Conocimiento del japonés: deseable pero no obligatorio. Es útil para resolver ambigüedades y verificar la simbología visual.

---

## Documentos que debes leer antes de traducir

El orden importa:

1. Esta guía.
2. [Glosario normativo](glosario.md) — términos con traducción fija. Consúltalo siempre que tengas dudas sobre un nombre, habilidad o lugar.
3. [Voces de personajes](voces-personajes.md) — cómo habla cada personaje. Es obligatorio antes de traducir cualquier diálogo.
4. [Simbología y estilo visual](simbologia.md) — los símbolos que enmarcan el texto. Sin esto, el capítulo no tendrá el aspecto correcto.
5. [Flujo de trabajo y entrega](flujo-trabajo.md) — cómo entregar el archivo terminado.
6. [Fuentes de consulta](fuentes-consulta.md) — cuándo y cómo usar cada fuente.

Además, antes de traducir cualquier capítulo, lee el capítulo inmediatamente anterior ya publicado. El tono, el ritmo y las decisiones de adaptación deben ser consistentes con lo que está en `contenido/`.

---

## Flujo de una sesión de traducción

### 1. Localiza el capítulo

Ve al índice de Witch Cult Translations y haz fetch al capítulo que te corresponda. Si el capítulo no está traducido al inglés, trabaja directamente del japonés en Syosetu. Consulta [Fuentes de consulta](fuentes-consulta.md) para el orden de prioridad completo.

### 2. Lee el capítulo anterior publicado

Abre el `.md` del capítulo anterior en `contenido/` y úsalo como referencia de tono, simbología y decisiones de adaptación activas.

### 3. Traduce

Reglas fundamentales durante la traducción:

- **La naturalidad en español es la prioridad máxima.** Si una frase literal suena rara, reescríbela con fluidez aunque te alejes del original.
- **Conserva la simbología japonesa sin excepción.** Consulta [Simbología y estilo visual](simbologia.md).
- **Aplica el glosario.** Los términos 🔒 no se tocan; los 📝 tienen traducción fija.
- **Respeta la voz de cada personaje.** Consulta [Voces de personajes](voces-personajes.md).
- **No añadas ni omitas contenido.** No resumas, no expandas, no añadas explicaciones ausentes en el original.
- **No incluyas notas del traductor** en el cuerpo del texto. Si son imprescindibles, al final del capítulo entre corchetes: `[N. del T.: …]`.

### 4. Verifica con el checklist

Antes de entregar, repasa punto por punto el [checklist de calidad](flujo-trabajo.md#checklist-de-calidad).

### 5. Entrega

Consulta [Flujo de trabajo y entrega](flujo-trabajo.md) para el formato exacto del archivo, el encabezado, el nombre del fichero y el bloque JSON para `chapters.json`.

---

## Español neutro

El proyecto usa español neutro: vocabulario comprensible en todo el mundo hispanohablante, sin regionalismos marcados. Evita expresiones que sean exclusivas de un país o región. Si tienes dudas sobre si una expresión es demasiado local, sustitúyela por una alternativa más neutra.

El registro del narrador es formal-literario con toques de ironía y observación psicológica. No lo coloquialices. En momentos de acción, el ritmo debe ser corto y percusivo; en momentos de introspección de Subaru, más largo y sinuoso.

---

## Preguntas frecuentes

**¿Puedo proponer cambios al glosario?**
Sí. Al entregar un capítulo, indica las decisiones de traducción que hayas tomado y que no estén cubiertas por el glosario actual. El responsable del proyecto decidirá qué entradas incorpora.

**¿Qué hago si el inglés parece haber omitido algo?**
Consulta el japonés original en Syosetu. El inglés de Witch Cult Translations es de alta calidad pero no es infalible. El japonés siempre tiene la última palabra.

**¿Puedo cambiar una decisión de traducción anterior?**
Solo si hay un motivo sólido y se consulta antes con el responsable del proyecto. La consistencia entre capítulos es prioritaria.

**¿Qué hago si un término no está en el glosario?**
Toma la mejor decisión posible, documéntala y proponla al entregar el capítulo. No dejes el término sin resolver.
