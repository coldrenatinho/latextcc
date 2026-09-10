# 🎓 TCC — Mini Índice (WIN) + Machine Learning

## Desenvolvimento de um sistema inteligente de apoio à decisão para traders utilizando técnicas de Machine Learning aplicadas ao Mini Índice (WIN)

Repositório destinado à organização, redação em LaTeX e acompanhamento do **Trabalho de Conclusão de Curso (TCC)** do curso de **Sistemas de Informação da Universidade do Estado de Mato Grosso — UNEMAT, Campus de Sinop**.

O projeto investiga o uso de técnicas de **Machine Learning** para classificar movimentos do **Minicontrato Futuro de Ibovespa (WIN)** a partir de dados históricos e indicadores técnicos, com o objetivo de construir um protótipo de **apoio à tomada de decisão** para traders.

> O sistema é acadêmico e experimental. Não tem como objetivo executar ordens automaticamente, garantir lucro ou substituir análise financeira profissional.

---

## 📌 Identificação

| Informação | Descrição |
|---|---|
| **Curso** | Bacharelado em Sistemas de Informação |
| **Instituição** | Universidade do Estado de Mato Grosso — UNEMAT |
| **Campus** | Sinop — MT |
| **Disciplina** | FACET-SNP-336 — Trabalho de Conclusão de Curso I |
| **Semestre** | 2026/2 |
| **Acadêmico** | Pedro Henrique Freitas Silva |
| **Objeto de estudo** | Minicontrato Futuro de Ibovespa (WIN) |
| **Área** | Sistemas de Informação / Machine Learning / Séries Temporais Financeiras |
| **Situação** | TCC I — Projeto de Pesquisa |

---

## 📖 Tema

Aplicação de técnicas de Machine Learning a dados históricos e indicadores técnicos do Mini Índice (WIN) para apoio à tomada de decisão de traders.

## 📝 Título provisório

> **Desenvolvimento de um sistema inteligente de apoio à decisão para traders utilizando técnicas de Machine Learning aplicadas ao Mini Índice (WIN).**

O título poderá ser refinado durante o desenvolvimento conforme a orientação acadêmica e a delimitação experimental.

---

## ❓ Problema de pesquisa

Séries temporais financeiras apresentam ruído, não linearidade e mudanças de comportamento ao longo do tempo. No mercado futuro brasileiro, o Mini Índice (WIN) possui forte presença em operações de curto prazo, mas a interpretação simultânea de preços, volume e indicadores técnicos pode ser difícil e sujeita a decisões inconsistentes.

### Questão de pesquisa

> **Em que medida modelos de Machine Learning, treinados com dados históricos e indicadores técnicos do Mini Índice (WIN), conseguem classificar a direção do mercado e fornecer informação útil para um sistema de apoio à decisão de traders?**

---

## 💡 Pressuposto

Parte-se do pressuposto de que modelos de Machine Learning podem identificar relações nos dados históricos do WIN que auxiliem a classificação de movimentos de alta e baixa. O trabalho não pressupõe previsibilidade perfeita nem rentabilidade garantida; o desempenho será medido experimentalmente em dados não utilizados no treinamento.

---

## 🎯 Objetivo geral

> **Desenvolver e avaliar um sistema inteligente de apoio à decisão para traders, utilizando técnicas de Machine Learning aplicadas a dados históricos e indicadores técnicos do Mini Índice (WIN).**

## 🎯 Objetivos específicos

1. realizar revisão bibliográfica sobre Mini Índice, séries temporais financeiras, indicadores técnicos e Machine Learning;
2. selecionar e documentar uma fonte de dados históricos do WIN;
3. preparar e explorar os dados, tratando valores ausentes, inconsistências e ordenação temporal;
4. construir variáveis derivadas de preço, retorno, volume e indicadores técnicos;
5. definir o problema de classificação da direção futura do mercado;
6. implementar um modelo de referência simples e modelos de Machine Learning selecionados;
7. comparar os modelos com métricas adequadas de classificação;
8. utilizar separação cronológica entre treino, validação e teste para reduzir risco de vazamento de informação;
9. analisar limitações, estabilidade e possibilidade de overfitting;
10. desenvolver um protótipo que apresente os resultados de forma compreensível para apoio à decisão;
11. documentar código, dados permitidos, parâmetros e experimentos para favorecer a reprodutibilidade.

---

## 🧪 Desenho experimental inicial

```text
Dados históricos do WIN
        ↓
Limpeza e ordenação temporal
        ↓
Preço + retorno + volume
        ↓
Indicadores técnicos
        ↓
Construção da variável-alvo
        ↓
Treino → validação → teste cronológico
        ↓
Modelos de Machine Learning
        ↓
Comparação de métricas
        ↓
Protótipo de apoio à decisão
```

### Modelos candidatos

- Regressão Logística como baseline;
- Random Forest;
- XGBoost;
- MLP (rede neural), caso o escopo e os dados permitam;
- LSTM como possibilidade de extensão, sem ser requisito obrigatório do TCC.

### Métricas previstas

- Accuracy;
- Precision;
- Recall;
- F1-score;
- Balanced Accuracy;
- ROC-AUC, quando aplicável;
- matriz de confusão.

---

## 🚧 Delimitação

O trabalho será inicialmente limitado ao **Mini Índice (WIN)**. Mini Dólar, criptomoedas e ações individuais não fazem parte do escopo principal.

O foco científico será a **classificação e avaliação dos modelos**, não a criação de um robô de execução automática. Qualquer backtest eventualmente utilizado será tratado como análise complementar e deverá considerar limitações metodológicas.

---

## 📂 Estrutura do repositório

| Arquivo | Conteúdo |
|---|---|
| `projeto.tex` | Arquivo principal do documento |
| `cap1.tex` | Introdução, problema, objetivos, justificativa e delimitação |
| `cap2.tex` | Referencial teórico e trabalhos relacionados |
| `cap3.tex` | Metodologia e desenho experimental |
| `cap4.tex` | Cronograma |
| `TCC.bib` | Referências bibliográficas |
| `modelocapa.tex` | Capa |
| `folhaderosto.tex` | Folha de rosto |
| `folhaaprova.tex` | Modelo da folha/ata de aprovação |
| `resumos.tex` | Resumo e abstract |
| `siglas.tex` | Lista de siglas |
| `figs/` | Imagens do template e futuras figuras do trabalho |

---

## 📚 Eixos da revisão bibliográfica

A revisão deverá cobrir principalmente:

- mercado futuro e Minicontrato Futuro de Ibovespa;
- séries temporais financeiras;
- análise técnica e construção de atributos;
- aprendizado supervisionado;
- Random Forest, gradient boosting e redes neurais;
- avaliação de classificadores;
- validação temporal e prevenção de data leakage;
- overfitting em aplicações financeiras;
- sistemas de apoio à decisão;
- trabalhos relacionados ao WIN e ao Ibovespa.

---

## ✅ Critério de sucesso acadêmico

O projeto será considerado tecnicamente bem-sucedido se produzir um processo experimental reprodutível, comparar modelos de forma metodologicamente adequada, documentar resultados positivos e negativos e demonstrar como as saídas podem ser apresentadas em um sistema de apoio à decisão. **Não existe meta de lucro garantido nem obrigação de superar o mercado.**

---

## 🔬 Referência diretamente relacionada ao tema

O trabalho de Souza et al. (ICEIS 2026) avalia Random Forest e MLP para previsão de tendência intraday utilizando contratos de Mini Índice (WIN), seleção de atributos e otimização de hiperparâmetros. Ele é uma das referências centrais para a construção do referencial e do desenho experimental deste TCC.

---

## ⚠️ Pendências que ainda precisam ser confirmadas com a orientação

- nome do(a) orientador(a) no documento;
- fonte definitiva e período dos dados do WIN;
- periodicidade dos candles/dados intraday;
- horizonte utilizado para definir alta e baixa;
- conjunto final de indicadores técnicos;
- modelos finais que entrarão no experimento;
- formato da interface do protótipo.
