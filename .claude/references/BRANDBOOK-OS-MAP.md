# Brandbook OS — mapa del dashboard para el skill

Referencia para el skill que recibe el `visual-direction-en.md` que descarga cada
persona del dashboard (`index.html`) y construye su página a partir de él.

El documento de cada persona es distinto, pero todos salen del mismo molde. Este
archivo describe ese molde: qué bloques existen, qué decide cada uno, qué
respuestas son posibles, con qué texto exacto aparece cada una en el `.md` y cómo
se convierte todo eso en una página. Con esto el skill puede leer cualquier
documento, saber qué eligió la persona (y qué no) y no inventar lo que falta.

> Corresponde al build `20 Oct 2026 · 19:02` del dashboard (8 bloques). Si cambia
> una pregunta, una opción o su texto en `index.html`, hay que actualizar este
> archivo; las tablas de opciones de abajo se sacaron directamente del código.

---

## 1. Visión general

```
[00] Copy de la marca (opcional, archivos .md/.txt)
        │   qué dice la página y qué secciones tiene
        ▼
[01–08] Ocho bloques de preguntas
        │   cómo se ve y se comporta la página
        ▼
[Resultado] Selector de formato: From your copy · Scrolling landing · Single screen
        │
        ▼
visual-direction-en.md  ──►  skill  ──►  página construida
```

Tres capas de información, en este orden de autoridad:

1. **Copy de la marca (sección 00).** Manda sobre todo lo demás en *qué se dice*:
   palabras exactas, tono, nombres, qué secciones existen y en qué orden. Nunca se
   sustituye por texto de relleno.
2. **Respuestas de la persona (secciones 01–08).** Mandan en *cómo se ve*.
3. **System defaults** de cada sección. Se aplican tal cual salvo que una
   respuesta diga otra cosa. Nunca se improvisan.

Y una cuarta, más débil: las líneas **derivables** (`_Expressive only. Deduce it
from…_`), que el skill deduce de lo anterior y mantiene constantes, sin abrir una
dirección nueva.

| # | Título en el `.md` | Título en el dashboard | Qué decide en la página |
|---|---|---|---|
| 00 | `00. Brand copy and voice` | Your copy and branding | Contenido, voz, secciones, formato |
| 01 | `01. Visual Foundation` | The visual world | Carácter general y tono de todo lo demás |
| 02 | `02. Name & Typography` | Name and type | Nombre, fuentes, escala tipográfica |
| 03 | `03. Color System` | Colour | Paleta, proporción, tokens, botones |
| 04 | `04. Composition` | Page structure | Grid, alineación, densidad, aire |
| 05 | `05. Page Architecture` | Page architecture | Receta de secciones, header, hero, CTAs |
| 06 | `06. Illustration & Materiality` | Illustration & materials | Ilustración y textura de superficies |
| 07 | `07. Graphic Language` | Graphic elements | Formas, patrones, iconos, separadores |
| 08 | `08. Visual Restrictions` | What to avoid | Lo que la página nunca puede tener |
| 09 | `09. Page Format & Structure` | (selector en Resultado) | Landing con scroll o pantalla única; orden de partes |
| — | `Responsive — desktop and phone, non-negotiable` | — | Contrato móvil, siempre igual |
| — | `Instructions for AI` | — | Reglas de comportamiento, siempre igual |

---

## 2. Anatomía del `.md` que recibe el skill

El documento se monta siempre en este orden. Las secciones se separan con `---`.

```
# Visual Direction
_How the brand looks and behaves_

---
## 00. Brand copy and voice          ← solo si la persona subió copy
_Written by the brand, pasted as-is. It outranks every example…_
### <nombre-de-archivo-1>
<texto tal cual>
### <nombre-de-archivo-2>
…

---
## 01. Visual Foundation             ← secciones 01–08, ver reglas abajo
<respuestas>
**Alternation rules — non-negotiable**   ← solo en 05
<reglas> + patrón de acordeón (HTML + CSS)
_System defaults:_                       ← si la sección tiene defaults
- **Clave:** valor
_Expressive only. Deduce it from the decisions above…: A · B · C._   ← si tiene derivables

… 02 a 08 …

_No answers yet. Complete the blocks to build your Brandbook OS._  ← solo si no respondió nada

---
## 09. Page Format & Structure       ← siempre
---
## Still to define                   ← solo si respondió algo y quedan campos vacíos
---
## Responsive — desktop and phone, non-negotiable   ← siempre
---
## Instructions for AI               ← siempre
_About the system defaults marked in each section…_  ← si salió algún default
```

### Cuándo aparece o desaparece una sección 01–08

Una sección se escribe si tiene **al menos una respuesta** o si tiene **reglas o
defaults propios**. Por eso:

- **02, 03, 04, 05 y 07** aparecen siempre (tienen defaults o reglas). Si la
  persona no respondió nada en ellas, el cuerpo es:
  `_This block was left unanswered. Everything below is the system default and applies in full; do not invent an alternative._`
- **01, 06 y 08** no tienen defaults: si no se respondieron, **desaparecen del
  documento** y solo quedan nombradas en `Still to define`.

### `Still to define`

Lista los campos sin respuesta con la **pregunta y el bloque tal como se ven en el
dashboard**, no con las etiquetas del `.md`. Ejemplo:
`- What visual world do you want? (The visual world)`. La tabla de la sección 4
traduce cada pregunta a su campo.

---

## 3. Cómo leer una respuesta

Todas las respuestas se escriben en inglés aunque la interfaz esté en otro idioma.
Cada campo aparece como `**<Etiqueta>:** …` con una de estas formas:

| Forma en el `.md` | Campos |
|---|---|
| `**Label:** una frase` | Visual territory, Brand name, Primary typeface, Secondary typeface, Section archetypes |
| `**Visual tension:** a + b` | Visual tension |
| `**Label:** a, b and c.` | Keywords, Anti-keywords |
| `**Label:**` + filas `- **Fila:** frase` | Typographic settings, Function & proportion, Color rules, Composition, Illustration, Materiality, Graphic language, What to avoid |
| Bloque de paleta (ver 03) | Color palette |

Para saber **qué opción eligió** la persona, compara el texto con las tablas de la
sección 4. Hay cuatro casos:

1. **Coincide exactamente con una opción** → eligió esa opción del catálogo.
2. **No coincide con ninguna** → pulsó *Other* y lo escribió a mano. Trátalo como
   una decisión de la persona con el mismo peso que una opción; interprétalo, no
   lo corrijas hacia la opción más parecida.
3. **Coincide, pero lleva un añadido** → es una **nota** (*Anything to add?*). En
   campos de una línea va pegada con ` — <nota>`; en campos con filas va al final
   como `_Note: <nota>_`. La nota matiza la opción; si la contradice, gana la nota.
4. **El campo no aparece** → no respondió. Aplica el default de la sección si lo
   hay; si no, deduce sin inventar y dilo. Nunca rellenes con la opción por
   defecto del dashboard (columna *def*): eso es solo la sugerencia que ofrece el
   botón *Suggest one*.

**Filas sueltas.** En los campos con filas, cada fila es independiente y puede
faltar (p. ej. *What to avoid* exige 4 de 5). Una fila ausente = sin decisión en
esa fila, no "ninguna".

*Suggest one* no deja rastro: una opción sugerida y aceptada se lee igual que una
elegida.

---

## 4. Bloque por bloque

Columnas de las tablas: **id** (identificador interno de la opción), **en el
dashboard** (lo que ve la persona), **texto exacto en el `.md`**. *def* = opción
que propone *Suggest one*.

### 00. Brand copy and voice

- **Dónde:** zona *Your copy and branding* en la pantalla de inicio (roadmap).
- **Qué entra:** archivos `.md`, `.markdown` o `.txt`. Cada uno se pega como
  `### <nombre del archivo>` + su texto, sin tocar.
- **Para el skill:** es el contenido de la página. De aquí salen titulares,
  párrafos, nombres de productos, precios, preguntas frecuentes, el CTA principal
  y la decisión de formato si la persona no la fijó.
- **Si falta:** la sección 09 lo dice (`_No brand copy was attached…_`). El skill
  debe pedir el copy antes de construir; nunca usa placeholders.

---

### 01. Visual Foundation — *The visual world*

Fija el carácter general. Todo lo demás debe leerse coherente con esto.
Sin defaults. Derivables: `Desired perception — see Brand Personality · Overall character`.

**Visual territory** — *What visual world do you want?* · una opción · def `warm-craft`

| id | en el dashboard | texto exacto en el `.md` |
|---|---|---|
| warm-craft | Warm and crafted | A warm, crafted world: natural materials, earth tones and the hand visible in the finish. |
| clean-minimal | Clean and minimal | A clean, minimal world: few elements, a lot of empty space and low contrast. |
| editorial | Editorial and elegant | An editorial world: typography with character, clear columns and the rhythm of a magazine. |
| bold-energy | Bold and energetic | A bold world: strong contrast, large scale and movement. |
| natural-organic | Natural and organic | A natural world: organic shapes, living matter and unpolished finishes. |
| precise-tech | Precise and technical | A precise world: strict grid, clean surfaces and a technical finish. |

**Visual tension** — *Which two qualities live together?* · un par · def `raw-precise`

Se escribe `a + b`. Opciones: `raw + precise` · `warm + sober` · `playful + serious` ·
`crafted + modern` · `minimal + expressive` · `classic + daring`.
Para el skill: la primera cualidad suele vivir en la materia (textura, imagen,
trazo) y la segunda en la estructura (grid, tipografía, márgenes).

**Keywords** — *Which three words describe it?* · exactamente 3 · def `warm, handmade, airy`
**Anti-keywords** — *And which three never?* · exactamente 3 · def `cool, technical, dense`

Ambos usan el mismo vocabulario de 16 palabras, en 8 pares opuestos. Lo que se
elige como keyword no se puede elegir como anti-keyword.

| par | significado (pista del dashboard) |
|---|---|
| warm / cool | Tonos tierra y luz cálida, cercano / azules y grises, calma y distancia |
| minimal / rich | Pocos elementos y mucho vacío / muchos detalles, capas y decoración |
| playful / serious | Formas sueltas y guiños / sobrio y contenido |
| handmade / precise | Se ve la mano, trazo irregular / todo medido y alineado |
| natural / technical | Materia viva: madera, papel, planta / grid, datos, acabado de laboratorio |
| soft / bold | Bordes redondeados, bajo contraste / contraste fuerte, elementos grandes |
| classic / modern | Referencias atemporales / actual y despejado |
| airy / dense | Márgenes generosos / mucha información junta y ordenada |

---

### 02. Name & Typography — *Name and type*

Derivable: `Typography to avoid — see What to avoid`.

**Brand name** — *What is your venture called?* · texto libre. Se usa tal cual, con
su ortografía y mayúsculas, en el wordmark del header, el `<title>` y el footer.

**Primary typeface** — *Which type sets the headings?* · def `serif`
**Secondary typeface** — *And the long text?* · def `sans`

Las dos preguntas comparten catálogo. El texto trae la familia, el stack y los
pesos: el skill carga esa familia (Google Fonts) y usa el stack como fallback.

| id | en el dashboard | texto exacto en el `.md` |
|---|---|---|
| serif | Elegant serif | \*\*Libre Caslon Text\*\* — an elegant serif with fine serifs and an editorial air. Stack: "Libre Caslon Text", Georgia, "Times New Roman", serif. Weights: 400, 400 italic, 700. Use this exact family; if unavailable, the first in the stack. |
| sans | Neutral sans | \*\*Inter\*\* — a neutral sans that never calls attention to itself. Stack: Inter, -apple-system, "Segoe UI", Helvetica, Arial, sans-serif. Weights: 400, 500, 600. Use this exact family; if unavailable, the first in the stack. |
| rounded | Friendly rounded | \*\*Nunito\*\* — a rounded sans with soft terminals and an approachable tone. Stack: Nunito, "Trebuchet MS", Verdana, sans-serif. Weights: 400, 600, 700. Use this exact family; if unavailable, the first in the stack. |
| mono | Technical mono | \*\*JetBrains Mono\*\* — a monospaced face with a technical character. Stack: "JetBrains Mono", ui-monospace, Menlo, Consolas, monospace. Weights: 400, 500, 700. Use this exact family; if unavailable, the first in the stack. |

**Typographic settings** — *How is the text set?* · 3 filas, todas obligatorias

| fila | id | en el dashboard | texto exacto en el `.md` |
|---|---|---|---|
| Case | sentence *(def)* | Sentence case | Sentence case at every level; never all-caps headlines. |
| Case | caps-titles | Caps for titles | All caps reserved for headlines; everything else in sentence case. |
| Weight | light | Light | Light weights only; never bold. |
| Weight | normal *(def)* | Regular | Regular and medium weights; no bold. |
| Weight | bold | Bold | Heavy weights for presence; body copy stays regular. |
| Hierarchy | two | 2 levels | Two levels per layout: title and body. |
| Hierarchy | three *(def)* | 3 levels | Three levels per layout: title, subtitle and body. |
| Hierarchy | four | 4 levels | Four levels per layout: title, subtitle, body and caption. |

**System defaults (siempre en el `.md`):** Type scale (7 pasos con `clamp()`), H1,
H2, H3, Body, Lead paragraph, Caption and label, Display usage, Tracking, Leading,
Italics. Son los valores numéricos de la tipografía; las respuestas de arriba
eligen familia, caja, peso y niveles, y los defaults ponen los tamaños.

---

### 03. Color System — *Colour*

**Color palette** — *The brand colours* · 5 tonos obligatorios · def `warm-earth`

La persona parte de una paleta y puede ajustar cada tono y ponerle nombre. En el
`.md` no aparece el nombre de la paleta de partida, solo los 5 tonos finales:

```
**Color palette:**
- **Primary — <nombre opcional>**
  - HEX: #RRGGBB
  - RGB: r, g, b
  - CMYK: c, m, y, k
  - Approximate tone: <tono aproximado>
- **Neutral …**  - **Accent 01 …**  - **Accent 02 …**  - **Accent 03 …**

_Tones are a reference approximation, not official Pantone® codes._
```

Paletas de partida (orden: Primary · Neutral · Accent 01 · Accent 02 · Accent 03):

| id | en el dashboard | HEX |
|---|---|---|
| warm-earth | Warm earth | #A9431E #E6DCC6 #2D2926 #C98A5E #7A9B8E |
| ink-cream | Ink and cream | #8C2936 #F4EFE6 #1F1D1B #B08968 #5E6B62 |
| forest | Forest | #2F4F3E #EDE8DA #1C1A17 #A8763E #C2CBB4 |
| sea | Coast | #1F4E6B #F0EBE1 #17212A #D9A441 #8FB8C9 |
| mono | Monochrome | #2B2B2B #F2F2F0 #0E0E0E #8A8A88 #C4453A |
| bright | Bright | #E2452F #FBF7F2 #161616 #F2B705 #2B6CB0 |
| night | Night | #D4A537 #15181B #F0EDE6 #6E7B82 #9C5F3C |
| dusty | Dusty rose | #B5798A #F7F0EF #33272A #D9B8A8 #7E8F87 |
| citrus | Yellow and ink | #F0B323 #FAF8F3 #16161A #7A6B4F #C24A2E |

Si los 5 HEX coinciden con una fila, la persona aceptó esa paleta sin tocarla.
Ojo con **Night**: el Neutral es oscuro, así que la página es de fondo oscuro.

Justo después de la paleta el dashboard **calcula** y escribe dos bloques que el
skill usa directamente como tokens CSS (no hay que recalcularlos):

- `**Interface surfaces — computed from the palette**`: Page background, Raised
  surface, Inverted band (= Accent 01), Border and divider, cada uno con su color
  de texto y su ratio de contraste.
- `**Buttons and calls to action — computed from the palette**`: botón primario
  (fondo Primary, hover, active, focus ring en Accent 01, disabled), botón
  secundario (outline), text link, tamaño (48px, padding 16/24, target 44×44),
  label, radius y la regla de un primario por viewport.

**Function & proportion** — *How much of each colour shows?* · una opción que llena 5 filas · def `60-30-10`

Filas: Primary · Neutral · Accent 01 · Accent 02 · Accent 03.

| id | en el dashboard | Primary | Neutral | Accent 01 |
|---|---|---|---|---|
| 60-30-10 | 60 / 30 / 10 | Anchors the brand and appears in every piece — 30% | The default ground for long text — 60% | Marks a single moment per piece — 10% |
| primary-led | Primary-led | Anchors the brand and takes most of the piece — 60% | Gives relief and carries the text — 30% | Marks a single moment per piece — 10% |
| quiet | Almost all neutral | Appears in counted moments, which is why it lands — 15% | Dominates almost the whole piece — 80% | A single hit of colour per piece — 5% |
| balanced | Balanced | Shares the space evenly with the neutral — 45% | Shares the space evenly with the primary — 45% | Marks a single moment per piece — 10% |

En las cuatro opciones Accent 02 = `Packaging and seasonal work only — very occasional`
y Accent 03 = `Data, states and fine detail only — very occasional`.
Para el skill: los porcentajes son de superficie visible en la página (fondos de
sección, bandas, botones), no de cantidad de elementos.

**Color rules** — *How do they combine?* · 3 filas

| fila | id | en el dashboard | texto exacto en el `.md` |
|---|---|---|---|
| Dominant combinations | primary-on-neutral *(def)* | Primary on neutral | The primary colour on the neutral, with a single accent. |
| Dominant combinations | neutral-on-primary | Neutral on primary | The neutral on the primary colour, which becomes the ground. |
| Dominant combinations | accent-lead | Accent leads | The accent as protagonist, reserved for occasional pieces. |
| Contrast rules | high *(def)* | Always high | Text always at high contrast against its ground, never below 4.5:1. |
| Contrast rules | soft | Soft, except for text | Soft contrast between surfaces, but text never drops below 4.5:1. |
| Combinations to avoid | two-accents *(def)* | Two accents together | Never two accents in the same layout, nor accent on accent. |
| Combinations to avoid | colour-on-photo | Colour over photo | Never colour blocks over photography without a calm area beneath. |
| Combinations to avoid | pure-black | Pure black | Never pure black: always the dark neutral from the palette. |

**System defaults:** Secondary combinations — neutral on neutral, separated by a primary hairline.

---

### 04. Composition — *Page structure*

**Composition** — *How is the page ordered?* · 5 filas, mínimo 4

| fila | id | en el dashboard | texto exacto en el `.md` |
|---|---|---|---|
| Grid | six | 6 columns | A 6-column grid: few divisions and wide blocks. |
| Grid | twelve *(def)* | 12 columns | A 12-column grid; content blocks span 2, 3, 4 or 6 columns. |
| Grid | free | No grid | A free composition with no fixed module, but every edge still lands on a 12-column base. |
| Alignment | left *(def)* | Left | Left-aligned by default; centring is a deliberate exception. |
| Alignment | centered | Centred | Centred alignment for display elements only; body copy always stays left-aligned. |
| Alignment | justified | Justified | Justified text in short blocks only; never for long copy, where the browser opens rivers. |
| Symmetry / asymmetry | sym | Symmetrical | A symmetrical composition: weight spread evenly on both sides. |
| Symmetry / asymmetry | asym *(def)* | Asymmetrical | An asymmetrical composition, with the weight loaded to one side. |
| Density | low *(def)* | Low | Low density: a single idea per screen or page. |
| Density | medium | Medium | Medium density: two or three blocks per piece, with air between them. |
| Density | high | High | High density: a lot of information together, always well ordered. |
| White space | tight | Tight | Tight air: narrow margins and elements close together. |
| White space | generous *(def)* | Generous | Generous air: at least a third of every layout is left empty. |
| White space | extreme | A lot | Emptiness is the main element: more than half the layout breathes. |

**System defaults (siempre):** Columns (12/6/4), Column spans, Measure (60–75
caracteres), Margins (24/48/80px, max 1280px), Rhythm (24/64/128px), Scale de
espaciado, Breakpoints (390/768/1280/1600), Responsive behaviour, Layers (plano,
sin sombras), Blocks, Dividers, Image/text relationship (splits 7/5, 8/4, 9/3,
nunca 6/6).

---

### 05. Page Architecture — *Page architecture*

**Section archetypes** — *Which kinds of section will the page have?* · una opción · def `editorial`

Es la **receta** de la página: la secuencia de secciones y cómo es el hero.

| id | en el dashboard | texto exacto en el `.md` |
|---|---|---|
| editorial | Editorial | Editorial recipe. Run: split hero, text on 7 columns and image on 5 · full-colour band with a single line · two or three text sections on 7 columns with a subhead · colour closing. Hero: eyebrow, H1 on 7 columns, lead of two lines, one primary button; image on 5 columns, full-bleed to the right edge. |
| alternating | Alternating | Alternating recipe. Run: split hero · three or four image-and-text rows flipping side each time, image on 5 columns and text on 6 with one column of air · colour closing. Hero: eyebrow, H1 on 6 columns, lead, one primary button; image on 5 columns with one column of air between them. |
| grid | Grid | Grid recipe. Run: editorial hero · a grid of three or four equal pieces, each on 3 or 4 columns · one featured piece at double width · figures band · colour closing. Hero: H1 on 9 columns with the lead below on 6, one primary button, no image — the grid underneath carries the weight. |
| cinematic | Cinematic | Cinematic recipe. Run: full-bleed full-height image with the headline over it and a contrast layer · text sections on 6 columns between images · one display-size quote over solid colour · colour closing. Hero: full-bleed image at 80svh with a contrast layer, H1 and one primary button centred over it; this is the one centred moment allowed. |

**Alternation rules — non-negotiable (siempre):** ningún arquetipo se repite en dos
secciones seguidas; como máximo una sección centrada; entre dos secciones seguidas
cambian al menos dos de (fondo, alineación, nº de columnas, densidad); un punto
focal por sección; al menos 3 cambios de superficie en páginas de 6+ secciones;
el cuerpo nunca va centrado; ningún bloque de texto ocupa menos de 5 de 12
columnas.

Después de las reglas viene siempre el **patrón de acordeón** (HTML + CSS listos
para pegar). Se usa en cualquier sitio donde el copy ofrezca opciones plegables:
FAQ, planes, pasos.

**System defaults (siempre):** Header, Hero, Hero on mobile, Calls to action,
Section heads.

---

### 06. Illustration & Materiality — *Illustration & materials*

Sin defaults. Derivables: `Shape language · Illustration colour treatment · Grain · Surfaces · Physical references`.

**Illustration** — *Is there illustration?* · una opción que llena 3 filas · def `line`

Filas: Style · Line quality · Level of detail.

| id | en el dashboard | Style | Line quality | Level of detail |
|---|---|---|---|---|
| none | None | No illustration: the system relies on composition and material. | — | — |
| line | Line | Line drawing, reserved for what an image would not explain. | A single stroke weight, slightly irregular. | Suggestive; no shading or volume. |
| flat | Flat | Flat illustration built from colour shapes, with no outline. | No line: the shape defines the drawing. | Simple shapes; little internal detail. |
| hand | Hand-drawn | Hand-drawn illustration, with a loose and visible stroke. | An irregular stroke with varying pressure. | Medium detail; imperfection is welcome. |

Con `none` las filas 2 y 3 llevan `—`: el skill no dibuja SVGs ilustrativos.

**Materiality** — *Do surfaces look flat or textured?* · una opción que llena 2 filas · def `matte`

Filas: Paper · Texture.

| id | en el dashboard | Paper | Texture |
|---|---|---|---|
| matte | Matte | Uncoated paper, warm in tone. | A matte finish throughout; no varnish or lamination. |
| gloss | Gloss | Glossy coated paper. | A finish with controlled shine and reflection. |
| textured | Textured | Paper with visible grain and body. | Texture you can feel; relief and material. |

Para el skill (web): `matte` = superficies planas sin brillo; `gloss` = superficies
lisas con algún reflejo sutil; `textured` = grano o ruido sutil en fondos
(SVG/CSS), nunca imágenes de stock de papel.

---

### 07. Graphic Language — *Graphic elements*

**Graphic language** — *Which elements repeat across the site?* · 4 filas, mínimo 3

| fila | id | en el dashboard | texto exacto en el `.md` |
|---|---|---|---|
| Shapes | rounded *(def)* | Rounded | Shapes with rounded corners and soft transitions. |
| Shapes | straight | Straight | Straight shapes with clean angles and no rounding. |
| Shapes | organic | Organic | Organic shapes with irregular contours, never geometric. |
| Patterns | none *(def)* | No patterns | No patterns; surfaces stay flat. |
| Patterns | subtle | Subtle | Subtle patterns, barely perceptible, as a background layer. |
| Patterns | strong | Leading | Leading patterns: the pattern can be the whole piece. |
| Icons | line *(def)* | Line | Line icons at a single weight, matched to the body text. |
| Icons | filled | Filled | Solid, filled icons with no outline. |
| Icons | noicons | None | No icons: information is resolved with words. |
| Separators | hairline *(def)* | Hairline | Hairline separators in a neutral tone, with air around them. |
| Separators | space | Space only | No rules: sections separate by a change of surface or by a larger step of the spacing scale, never by uniform padding. |
| Separators | block | Colour blocks | Colour blocks separate sections, with no need for lines. |

*Shapes* fija el `border-radius` de toda la página (los botones de 03 dicen
"the value chosen in Graphic elements").

**System defaults (siempre):** Frames, Borders, Graphic devices, Repeated motifs.

---

### 08. Visual Restrictions — *What to avoid*

Sin defaults. Si no se respondió, desaparece del documento.

**What to avoid** — *What do you never want to see?* · 5 filas, mínimo 4. Cada fila
es una prohibición: el skill comprueba la página final contra todas.

| fila | id | en el dashboard | texto exacto en el `.md` |
|---|---|---|---|
| Styles to avoid | corporate *(def)* | Corporate vector | Flat corporate vector, gradients, 3D renders and glows. |
| Styles to avoid | retro | Retro nostalgia | Off-the-shelf retro nostalgia and borrowed vintage nods. |
| Styles to avoid | maximal | Maximalism | Maximalism with no hierarchy: everything full and nothing leading. |
| Colors to avoid | neon *(def)* | Neon and fluorescent | Neons, fluorescents and saturations that shout. |
| Colors to avoid | cold | Cold blues | Cold technology blues and greys with no temperature. |
| Colors to avoid | pastel | Pastels | Washed-out pastels that drain character. |
| Typography to avoid | display *(def)* | Decorative display | Decorative display faces, scripts and anything wearing a costume. |
| Typography to avoid | allcaps | All-caps headlines | All-caps headlines and exaggerated tracking. |
| Typography to avoid | many | Too many families | More than two typefaces in the same piece. |
| Composition to avoid | cards *(def)* | Stacked cards | Stacked cards with drop shadows, the default grid of any template. |
| Composition to avoid | centered | Everything centred | Centred symmetry out of habit, with no reason behind it. |
| Composition to avoid | crowded | No margins | Layouts with no margin, elements touching one another. |
| Generic / stock aesthetics to avoid | stock *(def)* | Anything from a stock library | Anything recognisable as a stock library image. |
| Generic / stock aesthetics to avoid | ai-look | Generic AI look | The default AI look: plastic sheen, odd symmetry and meaningless detail. |

---

### 09. Page Format & Structure — selector en la pantalla de Resultado

No es una pregunta de la roadmap: es un selector de tres opciones encima del
documento. Cambia el párrafo de introducción y el punto 1 de la sección 09.

| Opción en el dashboard | Cómo se reconoce en el `.md` | Qué hace el skill |
|---|---|---|
| From your copy *(por defecto)* | El punto 1 empieza `**1. Format — scrolling landing or single screen.**` | Decide el formato leyendo el copy: más de un punto o >150 palabras → landing con scroll; un solo mensaje de ≤60 palabras → pantalla única. En duda, scroll. |
| Scrolling landing | `**1. Format — scrolling landing, chosen by the brand.**` | Landing con scroll aunque el copy sea corto (menos secciones, no otro formato). |
| Single screen | `**1. Format — single screen, chosen by the brand.**` | Todo en 100svh desde 768px, solo el hero de 05, sin menú. |

Los puntos 2–4 son siempre iguales: **2. Goal** (una sola acción primaria, sacada
del copy), **3. Order of parts** (una sección por bloque de copy; si el copy no da
orden: hero → oferta → detalles → prueba → precios → preguntas → cierre → footer;
nunca inventar testimonios, cifras, clientes ni precios) y **4. Navigation**
(header con anclas si hay 4+ secciones).

Cierra con la instrucción de salida: **abrir la respuesta con la estructura como
lista numerada** (formato, objetivo y acción primaria, y por cada sección: nombre,
arquetipo, fondo y primeras palabras del copy) y luego construir la página.

---

### Secciones fijas: Responsive e Instructions for AI

Son idénticas en todos los documentos; el skill las obedece, no las interpreta.

- **Responsive — desktop and phone, non-negotiable:** mobile-first, viewport meta,
  sin anchos fijos, traducción de spans a tablet y móvil, splits que se apilan
  (imagen primero), tipografía con `clamp()` y mínimo 16px en móvil, targets de
  44×44px, `svh` en bloques de altura completa, sin scroll horizontal, safe-area
  en elementos fijos. Incluye un CSS base y un checklist a 360/390/768/1280/1600px.
- **Instructions for AI:** priorizar distintividad, coherencia estratégica,
  carácter, relevancia emocional y contexto; no inventar atributos; deducir lo
  derivable sin abrir direcciones nuevas; preguntar cuando falte algo que cambie
  el resultado; toda página funciona en móvil. *"The goal is not to reproduce the
  answers. The goal is to translate them into coherent brand decisions."*

---

## 5. De las respuestas a la página

Cómo encaja cada bloque al construir:

| Decisión de la página | Sale de |
|---|---|
| Qué secciones hay, en qué orden, con qué texto | 00 (copy) + 09 punto 3 |
| Landing con scroll o pantalla única | Selector de 09, o el copy si es *From your copy* |
| Acción primaria (texto del botón) | 00 + 09 punto 2 |
| Secuencia de secciones y forma del hero | 05 Section archetypes + Alternation rules |
| Header, CTAs, cabeceras de sección | 05 defaults |
| Grid, alineación, densidad, aire | 04 respuestas + defaults |
| Fuentes y escala | 02 respuestas + defaults |
| Variables CSS de color, fondos y botones | 03 paleta + bloques calculados |
| Qué color domina cada sección | 03 Function & proportion + Color rules |
| `border-radius`, iconos, separadores, patrones | 07 |
| Textura de fondos, ilustraciones SVG | 06 |
| Tono general cuando algo queda abierto | 01 (territory, tension, keywords) |
| Revisión final: qué no puede aparecer | 08 + Anti-keywords de 01 |
| Comportamiento en móvil | Responsive (fijo) |

**Orden de trabajo recomendado para el skill**

1. Leer 00. Si no hay copy, pedirlo y parar.
2. Leer 09: fijar formato, acción primaria y lista de secciones.
3. Asignar a cada sección un arquetipo de la receta de 05 respetando las
   Alternation rules, y un fondo según la proporción de 03.
4. Escribir la estructura como lista numerada (lo exige 09).
5. Montar tokens: color (03), tipografía (02), espaciado y grid (04), radius (07).
6. Construir mobile-first siguiendo Responsive.
7. Revisar contra 08, Anti-keywords y el checklist de Responsive antes de entregar.

---

## 6. Ejemplo mínimo de cómo llega un campo

```markdown
## 04. Composition

**Composition:**
- **Grid:** A 12-column grid; content blocks span 2, 3, 4 or 6 columns.
- **Alignment:** Left-aligned by default; centring is a deliberate exception.
- **Density:** Medium density: two or three blocks per piece, with air between them.
- **White space:** Generous air: at least a third of every layout is left empty.

_Note: que se sienta lento, como una revista_
```

Lectura: Grid = `twelve`, Alignment = `left`, Density = `medium`, White space =
`generous`; falta *Symmetry / asymmetry* → sin decisión en esa fila, usar los
defaults de la sección (splits asimétricos 7/5, 8/4, 9/3); la nota matiza todo el
campo. Si la persona hubiera pulsado *Other*, las filas traerían su propio texto,
que no coincide con ninguna fila de las tablas.
