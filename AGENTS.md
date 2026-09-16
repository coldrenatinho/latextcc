# Repository Guidelines

## Project Structure & Module Organization

This repository contains the LaTeX source for the Estoque Fácil TCC, not the application code. `projeto.tex` is the entry point and includes `cap1.tex` through `cap4.tex`, front matter, and `TCC.bib`. Put diagrams and image assets in `figs/`; keep editable TikZ diagrams as `.tex` files there. `test/cap1-teste.tex` is a draft document, not an automated test suite. The `Acompannhamento TCC/` directory contains orientation material. Generated files belong in `.latex-build/` and should not be committed.

## Build, Test, and Development Commands

Build from the repository root with a TeX Live installation that provides `pdflatex`, BibTeX, abnTeX2, and TikZ:

```sh
mkdir -p .latex-build
pdflatex -interaction=nonstopmode -halt-on-error -output-directory=.latex-build projeto.tex
(cd .latex-build && BIBINPUTS=..: bibtex projeto)
pdflatex -interaction=nonstopmode -halt-on-error -output-directory=.latex-build projeto.tex
pdflatex -interaction=nonstopmode -halt-on-error -output-directory=.latex-build projeto.tex
```

The extra LaTeX passes resolve citations, figure numbers, and cross-references. Review `.latex-build/projeto.pdf`; `git diff --check` catches whitespace errors. There is no configured CI or automated testing framework for this document.

## Writing Style & Naming Conventions

Write academic prose in Brazilian Portuguese and preserve the existing abnTeX2 structure. Use one chapter per `capN.tex`, descriptive labels such as `\label{fig:uml-operacao}`, and cite sources with `\cite{...}` or `\citeonline{...}` using keys from `TCC.bib`. Indent nested LaTeX environments consistently with four spaces. Keep diagrams readable at the document's text width; avoid hard-coded claims that the source code or market offerings are current without a dated reference.

## Verification Guidelines

After changing text, figures, or bibliography, compile the complete document. Check the log for errors, undefined references, and overfull boxes; inspect changed PDF pages visually, especially tables and diagrams. Do not treat a successful compile as proof that a research claim is supported.

## Commit & Pull Request Guidelines

The short Git history uses concise Portuguese, action-oriented subjects (for example, `Ajusta capítulo e configuração de compilação`); no formal prefix convention is established. Keep commits focused. In a pull request, describe the chapters or assets changed, identify new or corrected references, note compilation results, and include PDF page screenshots when layout changed. Do not add auxiliary LaTeX files or generated PDFs to commits.
