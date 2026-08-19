# Estrutura do projeto LaTeX

O arquivo principal do trabalho é `projeto.tex`.

- Os capítulos e elementos pré/pós-textuais ficam na raiz porque são incluídos
  por `\input` e `\include`.
- As imagens ficam em `figs/`.
- As referências ficam em `TCC.bib`.
- A pasta `.vscode/` contém apenas a configuração do LaTeX Workshop.

No VS Code, abra esta pasta inteira e compile usando a receita:

`pdflatex -> bibtex -> pdflatex x2`

O contador automático de palavras da extensão LaTeX Utilities foi desativado,
pois o executável `texcount` não está instalado neste ambiente.
