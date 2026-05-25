# Flujo de trabajo y entrega

Este documento describe el proceso completo desde que terminas de traducir hasta que el capítulo está listo para publicar.

---

## Formato del archivo

Cada capítulo se entrega como un archivo `.md` con el siguiente convenio de nombre:

```
arc{arco:02d}_cap{capitulo:03d}_{slug}.md
```

Donde `{slug}` es el título del capítulo en minúsculas, con palabras separadas por guiones bajos y sin tildes ni caracteres especiales.

**Ejemplos correctos:**

```
arc01_cap000_prologo.md
arc01_cap001_un_inservible_10_estriado.md
arc01_cap012_reencuentro_con_la_bruja.md
arc02_cap000_prologo.md
```

**Errores frecuentes:**

```
arc01_cap1_prologo.md        ← el número de capítulo necesita tres dígitos
arc01_cap001.md              ← falta el slug
arc01_cap001_Un_Inservible.md ← el slug debe ir en minúsculas
```

---

## Encabezado obligatorio

Todos los capítulos deben comenzar con este encabezado exacto, cambiando únicamente el número de arco, el título del arco, el número de capítulo y el título:

```markdown
# Re:Zero Kara Hajimeru Isekai Seikatsu
## Arco N — Título del arco
### Capítulo N: Título del capítulo

---

※ ※ ※ ※ ※ ※ ※ ※ ※ ※ ※
```

Para prólogos, epílogos e interludios, la tercera línea cambia:

```markdown
### Prólogo: Título del prólogo
### Epílogo: Título del epílogo
### Interludio: Título del interludio
```

El encabezado termina siempre con `---` seguido de la línea `※ ※ ※ ※ ※ ※ ※ ※ ※ ※ ※` con once símbolos. El capítulo también termina con esa misma línea de `※`.

---

## Normas de formato del archivo

- Bloques narrativos separados por línea en blanco, igual que el original japonés.
- Sin numeración de párrafos ni encabezados adicionales que no estén en el original.
- Sin notas del traductor en el cuerpo del texto. Si son imprescindibles, al final del archivo: `[N. del T.: …]`.
- No sustituyas caracteres por variantes similares (`-` en lugar de `――`, comillas rectas en lugar de `「」`, etc.).

---

## Bloque JSON para `chapters.json`

Al entregar un capítulo, incluye el bloque JSON listo para copiar en `chapters.json`. El usuario lo añade manualmente al final del array.

```json
{
  "id": "arc01_cap001",
  "arco": 1,
  "arcoTitulo": "Título del arco",
  "capitulo": 1,
  "tipo": "capitulo",
  "titulo": "Título traducido del capítulo",
  "archivo": "contenido/arc01_cap001_titulo_en_slug.md",
  "fecha": "YYYY-MM-DD",
  "resumen": "Una o dos frases de sinopsis del capítulo."
}
```

**Valores posibles para `tipo`:**

| Valor | Cuándo usarlo |
|---|---|
| `"prologo"` | Prólogo de un arco |
| `"epilogo"` | Epílogo de un arco |
| `"capitulo"` | Capítulo numerado |
| `"interludio"` | Interludio entre arcos o dentro de un arco |

**Reglas del campo `id`:** formato `arc##_cap###`, con dos dígitos para el arco y tres para el capítulo. El prólogo es `cap000`.

```
arc01_cap000   ← prólogo del arco 1
arc01_cap001   ← capítulo 1 del arco 1
arc02_cap000   ← prólogo del arco 2
arc02_cap012   ← capítulo 12 del arco 2
```

---

## Checklist de calidad

Repasa este checklist antes de entregar. Cada punto es una verificación independiente; no saltes ninguno.

### Glosario y nombres
- [ ] ¿Todos los términos 🔒 del glosario aparecen sin traducir?
- [ ] ¿Todos los términos 📝 usan la traducción establecida?
- [ ] ¿Los nombres propios están escritos correctamente? (sin «Beatriz», sin reordenar apellidos, etc.)

### Voces de personajes
- [ ] ¿Cada personaje suena como sí mismo?
- [ ] ¿Ram usa «Barusu» para Subaru en cada aparición?
- [ ] ¿Beatrice usa construcciones arcaicas?
- [ ] ¿Roswaal tiene tono teatral y alargamientos?

### Calidad de traducción
- [ ] ¿Hay calcos del japonés o del inglés que suenen artificiales en español?
- [ ] ¿Se han omitido o añadido contenidos respecto al original?

### Simbología visual
- [ ] ¿Los diálogos usan `「 」` y no rayas ni comillas españolas?
- [ ] ¿Los pensamientos y frases dramáticas usan `――`?
- [ ] ¿Las pausas son `……` y no `...`?
- [ ] ¿Los conceptos especiales usan `『 』`?
- [ ] ¿Los separadores de escena son `△▼△▼△▼△` y no `***` ni `———`?
- [ ] ¿Los separadores de sección `※ ※ ※` se han conservado intactos?

### Ritmo y narración
- [ ] ¿El ritmo de los párrafos de acción es ágil y no se han fusionado frases cortas?
- [ ] ¿Los cortes dramáticos y líneas aisladas se han preservado?
- [ ] ¿El tono del narrador es consistente con capítulos anteriores?

### Formato y estructura
- [ ] ¿El encabezado replica exactamente la plantilla establecida?
- [ ] ¿El nombre del archivo sigue el convenio correcto?
- [ ] ¿No hay numeración de párrafos ni encabezados añadidos?

---

## Propuestas al glosario

Al terminar cada capítulo, revisa si has tomado decisiones de traducción no cubiertas por el glosario: adaptaciones culturales, resoluciones de ambigüedad, expresiones recurrentes con traducción fijada en esa sesión, etc.

Si las hay, inclúyelas junto al bloque JSON con este formato:

| Término original | Traducción establecida | Notas |
|---|---|---|
| Término | Traducción | Contexto o justificación breve |

No incluyas decisiones puntuales que no vayan a repetirse ni variantes ya cubiertas por el glosario. El responsable del proyecto decidirá qué entradas incorpora.
