# <img src="assets/logo.png" width="48" height="48" align="absmiddle" alt=""> Re:Zero — Traducción al Español · GitHub Pages

Sitio estático para publicar la traducción capítulo a capítulo.

## Estructura

```
rezero-site/
├── index.html          ← Portada e índice de capítulos
├── lector.html         ← Página de lectura (universal)
├── chapters.json       ← Manifiesto: lista de todos los capítulos
├── favicon.png         ← Icono del sitio
├── _config.yml         ← Configuración mínima de GitHub Pages
└── contenido/
    └── arc01_cap00_prologo.md
    └── arc01_cap01.md   ← (futuros capítulos aquí)
    └── ...
```

---

## Cómo añadir un capítulo nuevo

### 1. Crea el archivo Markdown

Guarda el capítulo traducido en `contenido/` con este convenio de nombre:

```
arc{arco:02d}_cap{capitulo:02d}_{tipo}.md
```

Ejemplos:
- `arc01_cap01.md`
- `arc01_cap02.md`
- `arc02_cap00_prologo.md`

El archivo puede empezar directamente con el texto (sin repetir metadatos: el lector los toma del manifiesto).

### 2. Añade la entrada en `chapters.json`

```json
{
  "id": "arc01_cap01",
  "arco": 1,
  "arcoTitulo": "Un primer día tumultuoso",
  "capitulo": 1,
  "tipo": "normal",
  "titulo": "El título del capítulo",
  "archivo": "contenido/arc01_cap01.md",
  "fecha": "2026-05-10",
  "resumen": "Breve descripción opcional (aparece en el tooltip)."
}
```

**Valores posibles para `tipo`:**
- `"prologo"` — Prólogo
- `"epilogo"` — Epílogo
- `"normal"`  — Capítulo numerado (usa el campo `capitulo`)

El orden en el JSON es el orden de navegación (anterior/siguiente).

### 3. Sube los cambios

```bash
git add contenido/arc01_cap01.md chapters.json
git commit -m "Add: Arco 1 Cap. 1 — Título"
git push
```

GitHub Pages publica automáticamente en 1–2 minutos.

---

## Funcionalidades del lector

- **Control de tamaño de fuente** (A− / A+), persistente entre visitas
- **Barra de progreso** de lectura
- **Navegación por teclado**: ← → para capítulo anterior/siguiente
- **Separadores ※** detectados y renderizados automáticamente
- **Drop cap** en el primer párrafo de cada capítulo

---

## Formato del Markdown

El lector entiende Markdown estándar. Convenciones específicas del proyecto:

| Elemento | Cómo escribirlo en MD |
|---|---|
| Separador de sección | `---` (se renderiza como ※ ※ ※ …) |
| Diálogo hablado | `『texto』` (tal cual, Unicode) |
| Pensamiento / cita | `「texto」` (tal cual, Unicode) |
| Narrador — em dash | `―texto` (guión largo Unicode U+2015) |
| Énfasis | `*texto*` o `**texto**` |

No incluyas los encabezados H1/H2/H3 con el título del capítulo: el lector los genera desde `chapters.json`.
