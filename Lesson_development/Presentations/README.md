# Workshop slides: Interoperability in Climate and Atmospheric sciences

Quarto revealjs decks that share one theme.

| File | Deck |
|------|------|
| `00-intro.qmd` | Welcome and context |
| `01-introduction.qmd` | Introduction |
| `02-structural.qmd` | Structural interoperability |
| `03-semantic.qmd` | Semantic interoperability |
| `04-technical-protocols.qmd` | Technical interoperability II: Data access protocols |
| `05-technical-api.qmd` | Technical interoperability II: API |
| `06-cloud-native-layouts.qmd` | Cloud native layouts |

## Prerequisites
 
Rendering the slides locally requires:
 
- [Quarto](https://quarto.org/docs/get-started/)
- A recent web browser for previewing slides
 
Verify your installation:
 
```bash
quarto check
```

## Working on the slides

```bash
quarto preview 02-structural.qmd   # live preview of one deck
quarto render                      # build everything into _site/
```

* Shared options (theme, logo, size, transitions) live in `_quarto.yml`.
* Colours, boxes and layout helpers live in `styles.scss`.
* A new deck is a new `NN-name.qmd` with only a `title` and `subtitle` in its header.
  Add it to `index.qmd`.
* Images go in `images/<deck>/`; things used by several decks go in `images/shared/`.

## Automatic build

`.github/workflows/publish.yml` renders the whole project on every push.
The rendered site is attached to the run as the `slides` artifact.
On `main` it is also published to GitHub Pages
(Settings → Pages → Source: *GitHub Actions*).
