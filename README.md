# PKU SEE Beamer Template

A clean 16:9 Beamer presentation template for academic talks, with PKU SEE branding, a title page, outline page, compact footer, and acknowledgements slide.

## Features

- 16:9 presentation layout.
- PKU and SEE logo title page.
- Minimal frame title rule and compact footer.
- Built-in outline and acknowledgements frames.
- Shared theme package in `pku_beamer.sty`.
- Example slides for bullets, equations, blocks, and tables.
- XeLaTeX-friendly Chinese font setup.

## Files

- `document.tex`: main presentation file. Edit title, author, institute, date, sections, and slides here.
- `pku_beamer.sty`: visual template package. It controls fonts, colors, title page, footer, blocks, tables, listings, and helper commands.
- `logo/`: required logo assets.
- `docs/preview.png`: screenshot used in this README.
- `LaTeX.bib`: optional bibliography file.

## Requirements

- TeX Live or MacTeX.
- XeLaTeX.
- `latexmk`.

## Compile

```bash
latexmk -xelatex -outdir=build document.tex
```

The generated PDF will be placed in `build/document.pdf`.

Generated files under `build/` are ignored by `.gitignore`.

## Quick Start

Edit the metadata in `document.tex`:

```tex
\title[Short Title]{Presentation Title}
\subtitle{Presentation Subtitle}
\author[Author Name]{Author Name}
\institute[PKU SEE]{School of Environment and Energy, Peking University}
\date{\today}
```

Then replace the example frames with your own content.

## Common Commands

- `\PKUTitlePage`: insert the formal title page.
- `\PKUOutlineFrame`: insert the table of contents.
- `\PKUHighlight{...}`: highlight important keywords with the template color.
- `\PKUAcknowledgementsFrame`: insert the final acknowledgements page.
- `\PKUEnableSectionPages`: optional command for inserting a divider page at each section.

## Aspect Ratio

The template currently uses standard widescreen mode:

```tex
\documentclass[aspectratio=169]{beamer}
```

For MacBook-native full-screen preview, you can switch to `aspectratio=1610`.

## License

Template source files are released under the MIT License. See `LICENSE`.

