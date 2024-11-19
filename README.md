# Counting $k$-bounded functions on $[n]$

## Abstract / Resumo

### Abstract
In this work, we introduce the concept of $(\alpha, \lambda)$-bounded functions, characterized by limited local variation, which are especially useful in discrete sets. Initially, we formally define these functions and investigate their fundamental properties, highlighting significant differences from continuous functions. The main result obtained is the asymptotic characterization of $a(n, k)$, representing the number of functions from $[n]$ to $[n]$ that are $k$-bounded with respect to Manhattan distance. The proof of this result combines Toeplitz matrices with a well-known inequality from graph theory. Additionally, we emphasize the relevance of the intersection between algebraic combinatorics, graph theory, and the analysis of discrete metric spaces, suggesting future research into the topological properties of these functions and their potential applications in computational and mathematical contexts.

### Resumo
Neste trabalho, introduzimos o conceito de funções $(\alpha, \lambda)$-limitadas, caracterizadas por variação local limitada, que são especialmente úteis em conjuntos discretos. Inicialmente, definimos formalmente essas funções e investigamos suas propriedades fundamentais, destacando diferenças significativas em relação às funções contínuas. O principal resultado obtido é a caracterização assintótica de $a(n, k)$, representando o número de funções de $[n]$ para $[n]$ que são $k$-limitadas em relação à distância de Manhattan. A prova desse resultado combina matrizes de Toeplitz com uma desigualdade bem conhecida da teoria dos grafos. Além disso, enfatizamos a relevância da interseção entre combinatória algébrica, teoria dos grafos e análise de espaços métricos discretos, sugerindo pesquisas futuras sobre as propriedades topológicas dessas funções e suas potenciais aplicações em contextos computacionais e matemáticos.

## Compile instructions

To compile the LaTeX project and generate the PDF files in both English and Portuguese, follow the instructions below.

### Prerequisites

Ensure you have the necessary dependencies installed:

```sh
sudo apt install texlive-full
sudo apt install inkscape
```

### Compilation command

Use the following latexmk command to compile the project:

```sh
latexmk -bibtex -pdf -pvc --shell-escape -interaction=nonstopmode -outdir=./pdf tex/main.tex
```

## How the translation works

The translation between Portuguese and English is managed using custom LaTeX commands defined in the preamble:

```tex
\newcommand{\en}[1]{\ifen#1\fi}
\newcommand{\pt}[1]{\ifpt#1\fi}

\entrue
% \pttrue
```

### Commands:
- `\en{...}`: Encloses English text.
- `\pt{...}`: Encloses Portuguese text.

### Language selection:
- To compile the document in English, ensure \entrue is active and \pttrue is commented out.
- To compile in Portuguese, comment out \entrue and uncomment \pttrue.

## Recommended tool: diff-pdf

To compare different versions of your compiled PDFs, we recommend using the diff-pdf tool. It allows you to visually inspect differences between two PDF files, which is especially useful after making translations or updates.

### Download and installation:

You can download diff-pdf from [its GitHub repository](https://github.com/vslavik/diff-pdf).

### Usage:
```sh
diff-pdf --output-diff=diff.pdf old_version.pdf new_version.pdf
```

This command will generate a PDF showing the differences between the two versions, helping you ensure that translations and updates are correctly reflected.

## Project structure

- **pdf/**: Contains the compiled PDF files in both English and Portuguese.
  - **english.pdf**: Compiled English version of the document.
  - **portuguese.pdf**: Compiled Portuguese version of the document.
- **tex/**: Contains all LaTeX source files for the project.
  - **chapters/**
    - **introduction.tex**: Contains the introduction section.
    - **ch1.tex**: Source file for Chapter 1.
    - **ch2.tex**: Source file for Chapter 2.
    - **ch3.tex**: Source file for Chapter 3.
    - **conclusion.tex**: Contains the conclusion section.
    - **appendix.tex**: Contains the appendix section of the document.
  - **data.tex**
  - **figures/**: LaTeX files that define the figures used in the document.
  - **main.tex**: The main LaTeX file that orchestrates the compilation of the entire document by including all chapters, figures, and pages.
  - **pages/**: Contains front matter and other page-specific `.tex` files.
    - **abstract.tex**: Contains the abstract section in English.
    - **acknowledgment.tex**: Contains the acknowledgments section.
    - **dedicatory.tex**: Contains the dedicatory section.
    - **first_cover.tex**: Defines the first cover page of the document.
    - **notations.tex**: Lists the notations used throughout the document.
    - **resumo.tex**: Contains the resumo (summary) section in Portuguese.
    - **second_cover.tex**: Defines the second cover page of the document.
  - **refs.bib**: Bibliography file containing all references cited in the document.
