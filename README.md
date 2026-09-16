# TCC — Estoque Fácil

Fonte LaTeX do projeto de **Trabalho de Conclusão de Curso I** de Renato Araujo da Silva, desenvolvido no curso de Sistemas de Informação da Universidade do Estado de Mato Grosso (UNEMAT), Campus de Sinop.

> **Projeto e Desenvolvimento do Software “Estoque Fácil”: um Sistema Web para Gestão e Controle de Estoques Baseado em Demandas de Mercado, Decisões Arquiteturais e Critérios de Qualidade de Software**

## Sobre o trabalho

O TCC utiliza o **Estoque Fácil** como objeto de um estudo de caso em Engenharia de Software. O protótipo surgiu de observações exploratórias feitas durante minha atuação no suporte a um ERP em Sinop, especialmente sobre dificuldades de conferir saldos, rastrear retiradas e recuperar o histórico de materiais.

Essas observações motivam o problema, mas não são apresentadas como levantamento estatístico das empresas da região. A fundamentação combina literatura acadêmica, normas, documentação técnica, fontes oficiais de sistemas existentes e inspeção do código do protótipo.

O código da aplicação está em um repositório separado: [coldrenatinho/Estoque_Facil](https://github.com/coldrenatinho/Estoque_Facil).

## Escopo acadêmico

Este repositório corresponde ao **TCC I** e contém a delimitação da pesquisa, a fundamentação teórica, o estado inicial do protótipo, os diagramas e o protocolo planejado de avaliação.

O Estoque Fácil ainda não é apresentado como produto concluído ou validado. No **TCC II**, a proposta é selecionar uma versão identificável do sistema, implementar as complementações priorizadas e produzir evidências de testes sobre:

- adequação funcional e integridade das movimentações;
- rastreabilidade por produto, setor e funcionário;
- permissões, segurança e confiabilidade;
- desempenho, interação e manutenibilidade;
- reprodutibilidade do ambiente de avaliação.

## Conteúdo atual

O documento está organizado em quatro capítulos:

1. **Introdução** — contexto, problema, pressuposto, objetivos, justificativa e delimitação;
2. **Referencial teórico** — estoques, sistemas web, requisitos, arquitetura, tecnologias, qualidade e comparação documental de Bling, Conta Azul Pro, Omie, Odoo e ERPNext;
3. **Metodologia** — estudo de caso, estado do protótipo, arquitetura, modelo de dados, casos de uso UML, requisitos e protocolo de avaliação;
4. **Cronograma** — períodos acadêmicos, entregáveis do TCC I e sequência planejada para o TCC II.

As referências são mantidas em `TCC.bib`. As descrições do protótipo citam o repositório de software e distinguem recurso identificado no código, comportamento ainda não verificado e funcionalidade futura.

## Estrutura do repositório

```text
projeto.tex          documento principal e configuração abnTeX2
cap1.tex             introdução
cap2.tex             referencial teórico
cap3.tex             metodologia
cap4.tex             cronograma
resumos.tex          resumo e abstract
modelocapa.tex       capa
folhaderosto.tex     folha de rosto
folhaaprova.tex      folha de aprovação
siglas.tex           abreviaturas e siglas
TCC.bib              referências bibliográficas
figs/                imagens e diagramas TikZ
test/                rascunho isolado do capítulo 1
```

Os principais diagramas editáveis estão em:

- `figs/arquitetura-estoque.tex`;
- `figs/dados-estoque.tex`;
- `figs/uml-casos-operacao.tex`;
- `figs/uml-casos-administracao.tex`;
- `figs/uml-sequencia-saida.tex`.

## Compilação

É necessário ter uma distribuição TeX Live com `pdflatex`, BibTeX, abnTeX2 e TikZ. Execute na raiz do repositório:

```bash
mkdir -p .latex-build
pdflatex -interaction=nonstopmode -halt-on-error \
  -output-directory=.latex-build projeto.tex
(cd .latex-build && BIBINPUTS=..: bibtex projeto)
pdflatex -interaction=nonstopmode -halt-on-error \
  -output-directory=.latex-build projeto.tex
pdflatex -interaction=nonstopmode -halt-on-error \
  -output-directory=.latex-build projeto.tex
```

O resultado será criado em `.latex-build/projeto.pdf`. As execuções adicionais resolvem citações, sumário, numeração e referências cruzadas.

Após compilar, verifique no log:

```bash
rg "undefined|Overfull|LaTeX Error" .latex-build/projeto.log
```

Também é necessário revisar visualmente tabelas, capa e diagramas. Uma compilação bem-sucedida não comprova a correção das afirmações acadêmicas nem dos recursos descritos.

## Exportação para Word

Uma versão para revisão pode ser gerada em DOCX com um conversor de LaTeX, como o Pandoc. Como o documento usa abnTeX2 e figuras TikZ, a exportação exige conferência posterior de capa, sumário, referências, tabelas e diagramas. O arquivo Word é um artefato de distribuição; o LaTeX permanece como fonte principal.

## Estado do projeto

- **Etapa:** TCC I — projeto de pesquisa;
- **semestre:** 2026/2;
- **autor:** Renato Araujo da Silva;
- **orientador:** Juliano De Avila;
- **instituição:** UNEMAT — Campus Universitário de Sinop;
- **situação do software:** protótipo em evolução, com avaliação planejada para o TCC II.

## Contribuições

Alterações devem preservar a escrita acadêmica em português brasileiro e a separação entre código existente, trabalho previsto e resultado efetivamente demonstrado. Antes de enviar uma contribuição:

1. compile o documento completo;
2. confira erros, referências indefinidas e caixas excedentes;
3. revise as páginas afetadas no PDF;
4. inclua fontes novas em `TCC.bib`;
5. não versione arquivos auxiliares ou saídas de compilação.
