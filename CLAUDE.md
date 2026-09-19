# CLAUDE.md

Francis DiTraglia's academic CV. One LaTeX source file, `DiTraglia-CV.tex`, using the `myres.cls` class in this repo.

## Build

```bash
xelatex DiTraglia-CV.tex
```

XeLaTeX is required because the fonts (XCharter, Inconsolata) are loaded with `fontspec`. The CV should stay at four pages. The compiled `DiTraglia-CV.pdf` is tracked in git; rebuild and commit it with every change to the source. The footer prints the build date.

## Keeping the website in sync

The website repo is `../fditraglia.github.io`. After rebuilding, copy `DiTraglia-CV.pdf` to `../fditraglia.github.io/pdf/DiTraglia-CV.pdf` and commit it there; the site serves that copy.

Papers are listed both here and in the website's `_data/papers.yml`, which generates the research page. The two are maintained separately, so any change to a paper (title, coauthors, journal, status, volume, pages) must be made in both. The two drift apart easily. Check published details against Crossref (`api.crossref.org/works/<DOI>`), not against memory.

## Conventions

Follow these when adding entries.

- **Coauthors**: full first names, in the published order, joined with "and" and an Oxford comma, never "&". Accents are written out (Garc\'{i}a-Jimeno, S\'{a}nchez-Becerra).
- **Titles**: the published title exactly, including punctuation. No comma between the title and "(with ...)".
- **Journal names**: the journal's registered name, including an ampersand where the journal uses one (*Journal of Business \& Economic Statistics*, *Journal of Banking \& Finance*, *Communications Earth \& Environment*). Note that *Communications Earth & Environment* is not *Nature Communications*.
- **Citation format**: `year, volume (issue), pp.\ first--last.` with an en dash. Journals that use article numbers instead of pages are written `year, volume:article` (for example `2023, 90:102783`). No months.
- **Date ranges**: closed up between single tokens (`2013--2019`, `2019--Present`, `July--December 2025`); spaced when either end is more than one word (`January 2025 -- December 2027`).
- **Places**: `City, ST` and `City, UK`.
- **Grants**: `Funder and scheme -- ``Title,'' dates`, with the comma inside the closing quotation marks.
- **Presentations**: one line per academic year, label ending in a colon. Do not move entries between years or add years without asking.
- **Refereeing list**: alphabetical.
- **Graduate advising**: entries separated by semicolons, most recent first among supervised students.
- Retired entries are commented out, not deleted.

Prose follows American spelling.
