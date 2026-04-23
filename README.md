# HAPINN: A Solver-Guided Anchor-Based Framework for Parameterized Differential Equations

This repository contains the LaTeX source and supporting materials for the article:

**HAPINN: A Solver-Guided Anchor-Based Framework for Parameterized Differential Equations**

## Authors

**Sergo A. Episkoposian**  
Department of Applied Mathematics and Physics  
National Polytechnic University of Armenia  
Teryan 105, Yerevan 0003, Armenia  
Email: sergo.episkoposyan@polytechnic.am

**Alfred V. Petrosyan**  
Department of Applied Mathematics and Physics  
National Polytechnic University of Armenia  
Teryan 105, Yerevan 0003, Armenia  
Email: petrosyanalfred58@gmail.com

**Armen S. Yepiskoposyan**  
Institute of Physics  
Yerevan State University  
Al. Manukyan 1, Yerevan 0003, Armenia  
Email: earmen04@gmail.com

## Overview

This repository accompanies a framework paper on **HAPINN** (**H**ybrid **A**nchor-based **P**hysics-**I**nformed **N**eural **N**etwork), a solver-guided methodology for parameterized differential equations.

The central idea of the paper is that solver-generated anchors should not be interpreted as dense supervision, but as **structural admissibility constraints** that narrow the set of residual-consistent near-minimizers and improve training stability.

## Main contributions of the paper

The manuscript develops:

- a unified abstract formulation of HAPINN for parameterized boundary-value and initial-boundary-value problems;
- a canonical hybrid loss combining physics residuals and anchor consistency;
- a projection-based transfer theorem in a coercive elliptic model setting;
- finite-dimensional sufficient conditions for anchor-residual stability;
- a closed-form analytical toy model clarifying the anchor mechanism;
- a five-component decomposition of total error;
- and a framework-level interpretation of a previously published hybrid PINN--TCAD semiconductor realization.

## Scope and honesty statement

This repository is intentionally aligned with the actual scope of the article.

The associated paper is:

- a **conceptual** contribution,
- a **methodological** contribution,
- a **theoretical** contribution.

It is **not** presented as a new large-scale benchmark paper, and it does **not** claim a new empirical campaign across multiple PDE families.

The semiconductor evidence discussed in the manuscript refers to **previously published work**, which is interpreted in the paper as a concrete instance of the HAPINN framework.

## Repository structure

```text
hapinn-framework-paper/
├── README.md
├── LICENSE
├── CITATION.cff
├── .gitignore
├── paper/
│   ├── main.tex
│   ├── main.pdf
│   ├── references.bib
│   └── figures/
├── notes/
│   ├── contribution_statement.md
│   ├── reproducibility_note.md
│   └── submission_note.md
└── supplementary/
    ├── toy_model_derivation.md
    └── framework_scope_note.md
```

## Compilation

The manuscript is prepared in LaTeX using the `elsarticle` class.

This source currently includes an internal `thebibliography` section, so a basic build is:

```bash
pdflatex main.tex
pdflatex main.tex
```

If you later switch the manuscript to BibTeX, a standard build sequence would be:

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

## Reproducibility note

This repository is primarily intended to provide transparent access to the manuscript source and supporting notes.

It does not currently include a new benchmark software package, because the associated article is not an empirical benchmark study. The goal of the repository is to document the paper accurately and transparently.

## Suggested citation

If you use or refer to this repository, please cite the associated manuscript. Citation metadata are provided in `CITATION.cff`.

## License

The materials in this repository are distributed under the license specified in the `LICENSE` file.
