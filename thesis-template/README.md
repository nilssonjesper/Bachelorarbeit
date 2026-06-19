# Thesis Template

Welcome to the **i2 thesis template**.
This readme will guide you towards the files you can find in this folder and how to use them.
Your main entry points will be the `main.tex` and all the tex-files you create in `/appendix` and `/chapters` as well as your literature references in `literature.bib`.
You may create your own macros in `macros.tex` to e.g. easily reuse and quickly change frequently appearing symbols.
You may also adapt the styling defined in `thesisstyle.sty` to your liking.

In general, you are free to customize the template to your liking (the template should give you a rough idea on how to structure a larger latex project and our stylistic requirements, i.e. citation style, fontsize etc.).
However, please consult your supervisor in advance before making any changes to the cover page (e.g., due to logo usage guidelines).

## Logo usage

To include the RWTH corporate logo on the title page, you must submit the required (signed) logo usage request to the ZPA.
For the current procedure and relevant forms, please refer to the official information at https://sc.informatik.rwth-aachen.de/de/antraege-und-formulare/ and https://www.rwth-aachen.de/go/id/hjxv.

## Makefile

Automates building the thesis PDF: runs LaTeX with `-recorder` (e.g., `pdflatex -recorder main.tex`) to track included files/graphics/bibliography, rebuilds only what changed, reruns LaTeX until references/TOC are stable, runs bibtex/index tools when needed, and can auto-generate graphics (e.g., from .gpi, .fig, .dot, .svg, .eps).
Usage: run `make` in the project folder to build the PDF (by default main.pdf); run `make show` to build and open it; run `make clean` to remove generated files.

`Variables.ini` ensures that `*.pdf` outputs remain after cleaning, whereas `Targets.ini` defines a make option that firstly runs `make` and then `make clean`:

    make build-clean

