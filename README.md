# <img src="assets/favicon.png" width="36" height="36" align="absmiddle" alt=""> Re:Zero — Traducción al Español · GitHub Pages

Sitio estático con la traducción al español de la web novel *Re:Zero Kara Hajimeru Isekai Seikatsu* de Tappei Nagatsuki, publicada capítulo a capítulo.

---

## El lector

La web incluye un lector con las siguientes funcionalidades:

- **Control de tamaño de fuente** (A− / A+), persistente entre visitas
- **Tema oscuro / claro** (botón ☀/🌙), persistente entre visitas
- **Barra de progreso** de lectura
- **Navegación por teclado**: ← → para capítulo anterior/siguiente
- **Separadores `※`** detectados y renderizados automáticamente
- **Drop cap** en el primer párrafo de cada capítulo

---

## Estructura del repositorio

```
re-zero/
├── index.html              ← Portada e índice de capítulos
├── lector.html             ← Página de lectura (universal)
├── chapters.json           ← Manifiesto: lista de todos los capítulos
├── assets/
│   ├── favicon.png
│   └── logo.png
├── contenido/              ← Archivos Markdown de cada capítulo
│   ├── arc01_cap000_prologo.md
│   ├── arc01_cap001_un_inservible_10_estriado.md
│   └── ...
└── docs/                   ← Documentación del proyecto
    ├── README.md
    ├── guia-colaboradores.md
    ├── glosario.md
    ├── voces-personajes.md
    ├── simbologia.md
    ├── flujo-trabajo.md
    └── fuentes-consulta.md
```

---

## Cómo añadir un capítulo nuevo

### 1. Crea el archivo Markdown

Guarda el capítulo traducido en `contenido/` con este convenio de nombre:

```
arc{arco:02d}_cap{capitulo:03d}_{slug}.md
```

Ejemplos:
- `arc01_cap001_un_inservible_10_estriado.md`
- `arc01_cap002_no_te_pases_de_listo.md`
- `arc02_cap000_prologo.md`

El archivo debe comenzar con el encabezado estándar del proyecto:

```markdown
# Re:Zero Kara Hajimeru Isekai Seikatsu
## Arco N — Título del arco
### Capítulo N: Título del capítulo

---

※ ※ ※ ※ ※ ※ ※ ※ ※ ※ ※
```

Consulta [`docs/flujo-trabajo.md`](docs/flujo-trabajo.md) para el formato completo.

### 2. Añade la entrada en `chapters.json`

```json
{
  "id": "arc01_cap001",
  "arco": 1,
  "arcoTitulo": "Un primer día tumultuoso",
  "capitulo": 1,
  "tipo": "capitulo",
  "titulo": "Un inservible 10 estriado",
  "archivo": "contenido/arc01_cap001_un_inservible_10_estriado.md",
  "fecha": "2026-05-07",
  "resumen": "Breve descripción opcional."
}
```

**Valores posibles para `tipo`:** `"prologo"`, `"epilogo"`, `"capitulo"`, `"interludio"`.

El orden en el JSON determina la navegación anterior/siguiente en el lector.

### 3. Sube los cambios

```bash
git add contenido/arc01_cap001_titulo.md chapters.json
git commit -m "Add: Arco 1, Cap. 1 — Un inservible 10 estriado"
git push
```

GitHub Pages publica automáticamente en 1–2 minutos.

---

## Colaborar

Si quieres contribuir al proyecto —traducción, revisión o correcciones— abre un [issue en este repositorio](../../issues) para ponerte en contacto. Indica en qué te gustaría ayudar y tu nivel con el japonés y/o el inglés.

La documentación completa para traductores está en [`docs/`](docs/), incluyendo el glosario normativo, las voces de los personajes y el flujo de entrega.
