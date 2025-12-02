# ABMM06: Kvantitativa metoder

Kursmaterial för ABMM06, en kurs om kvantitativa metoder med fokus på enkäter och digitala metoder för ALM-studenter vid Lunds universitet.

## Författare

- **Mathias Johansson**, Lunds universitet
- **Kristofer Söderström**, Lunds universitet

## Generera PDFs

Alla sidor (slides, lektioner, dashboards) kan exporteras som PDF-filer för nedladdning och offline-läsning.

### Generera PDF för en specifik sida

För att generera en PDF för en specifik sida, använd `quarto render` med `--to pdf`:

```bash
# Generera PDF för en presentation
quarto render slides/beskrivande-statistik.qmd --to pdf

# Generera PDF för en lektion
quarto render lessons/fragettyper.qmd --to pdf

# Generera PDF för en dashboard (obs: interaktiva element fungerar inte i PDF)
quarto render dashboards/datatyper-viz.qmd --to pdf
```

### Generera PDFs för alla filer

För att generera PDFs för alla slides:

```bash
for file in slides/*.qmd; do
  quarto render "$file" --to pdf
done
```

För att generera PDFs för alla lektioner:

```bash
for file in lessons/*.qmd; do
  quarto render "$file" --to pdf
done
```

### Var hittar jag PDF-filerna?

PDF-filerna genereras i `_site/`-katalogen med samma struktur som källfilerna:
- `_site/slides/*.pdf`
- `_site/lessons/*.pdf`
- `_site/dashboards/*.pdf`

## Citera materialet

Alla sidor innehåller citationsmetadata enligt akademisk standard. Du kan citera detta material enligt följande format:

**Licens:** Detta material är publicerat under [CC-BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) licens.

### För hela kursen:

```
Johansson, M., & Söderström, K. (2025). ABMM06: Kvantitativa metoder.
Lunds universitet. https://mathjoha.github.io/abmm06
Licens: CC-BY-NC 4.0
```

### För enskilda presentationer/lektioner:

```
Johansson, M., & Söderström, K. (2025). Beskrivande statistik.
I ABMM06: Kvantitativa metoder. Lunds universitet.
https://mathjoha.github.io/abmm06/slides/beskrivande-statistik.html
Licens: CC-BY-NC 4.0
```

### BibTeX-format

```bibtex
@misc{abmm06,
  author = {Johansson, Mathias and Söderström, Kristofer},
  title = {ABMM06: Kvantitativa metoder},
  year = {2025},
  publisher = {Lunds universitet},
  url = {https://mathjoha.github.io/abmm06},
  note = {Licens: CC-BY-NC 4.0}
}
```

För specifika sidor, lägg till fälten `chapter` eller `note`:

```bibtex
@misc{abmm06_beskrivande,
  author = {Johansson, Mathias and Söderström, Kristofer},
  title = {Beskrivande statistik},
  year = {2025},
  publisher = {Lunds universitet},
  note = {Del av ABMM06: Kvantitativa metoder. Licens: CC-BY-NC 4.0},
  url = {https://mathjoha.github.io/abmm06/slides/beskrivande-statistik.html}
}
```

## Bygga webbplatsen

```bash
# Förhandsgranska med live reload
quarto preview

# Bygga hela webbplatsen
quarto render
```

## Projektstruktur

- `slides/` - RevealJS presentationer
- `lessons/` - Fördjupande lektioner
- `dashboards/` - Interaktiva verktyg med Observable JS
- `_site/` - Genererade HTML- och PDF-filer (ignoreras i git)
- `_quarto.yml` - Huvudkonfiguration
- `CLAUDE.md` - Vägledning för AI-assistent

## Licens

Detta material är licensierat under [Creative Commons Attribution-NonCommercial 4.0 International License (CC-BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/).

**Detta innebär att du får:**
- Dela och kopiera materialet i vilket format eller medium som helst
- Bearbeta och bygga vidare på materialet

**Under följande villkor:**
- **Erkännande (Attribution):** Du måste ge lämpligt erkännande, ange en länk till licensen och ange om ändringar har gjorts
- **Icke-kommersiell (NonCommercial):** Du får inte använda materialet för kommersiella ändamål

Materialet är framtaget för ABMM06-kursen vid Lunds universitet.
