# KAN Research Preparation Notes

A continuously maintained set of long-form study notes written while preparing
for independent research on Kolmogorov–Arnold Networks (KAN). The notes cover
linear algebra, the calculus needed for optimisation, the probability needed for
estimation, and the foundations of deep learning, and they compile to a single
book from `main.tex`.

**Author:** J Song (Alex) · **Contact:** jsong.alex@proton.me

## Typesetting

The book is typeset with **KaoNotes**, a research-oriented LaTeX framework
developed by the same author and released separately:

- Repository: <https://github.com/AlexandraSloan3/kaonotes>
- Concept DOI: [10.5281/zenodo.22018510](https://doi.org/10.5281/zenodo.22018510)
- Version 0.1.1: [10.5281/zenodo.22018865](https://doi.org/10.5281/zenodo.22018865)

KaoNotes adapts the wide-margin design of
[kaobook](https://github.com/fmarotta/kaobook) by Federico Marotta. The class and
package files vendored here (`kaobook.cls`, `kao.sty`, `kaotheorems.sty`,
`kaorefs.sty`) are unmodified copies distributed under the LaTeX Project Public
License 1.3c; the licence text is included as `LICENSE-LPPL-1.3c.txt`.

If you cite the typesetting framework, cite KaoNotes at the version DOI above.
This repository and KaoNotes are separate projects with separate scope, licences,
and DOIs.

## Scope

| Part | Chapters | Contents |
| --- | --- | --- |
| I — Linear Algebra | 1–10 | Column space, elimination and `A = LU`, the four subspaces, orthogonality and least squares, determinants, eigenvalues, the SVD, linear transformations, optimisation, and learning from data |
| II — Calculus for Learning | 11–14 | Derivatives and the chain rule, gradients, Jacobians and Hessians with Taylor approximation, gradient-based optimisation and backpropagation |
| III — Probability for Learning | 15–19 | Sample spaces and Bayes' rule, random variables, expectation and covariance, limit theorems, maximum likelihood and Bayesian estimation |
| IV — Deep Learning Foundations | 20–21 | What a learning problem is; a map of supervised, unsupervised, and reinforcement learning problems |
| V — Where the Halves Meet | 22 | How the linear-algebra picture maps onto layers, and what remains to be read |

Linear algebra is covered in full. Calculus and probability are covered only as
far as the research requires: calculus stops at what optimisation needs, and
probability stops at estimation. Stochastic processes, integration technique,
series, and differential equations are out of scope.

The KAN literature itself is **not** covered. Chapter 22 states the open
questions and marks unverified ground with `[needs verification]` rather than
guessing.

## Repository structure

```
main.tex                     entry point; document setup and chapter list
chapters/                    one file per chapter, 01–22
references/references.bib    bibliography
figures/                     figures (currently empty)
latexmkrc                    reproducible build configuration
kaobook.cls, kao*.sty        KaoNotes template files (unmodified)
LICENSE-LPPL-1.3c.txt        licence for the template files

MIT18.06(2010)/              original handwritten scans, kept as source material
mu-li-course/                course notebooks and original handwritten scans
calculus/                    placeholder (see below)
probability/                 placeholder (see below)
```

Handwritten scans are retained in place as the source material the early
chapters were typeset from. Nothing has been deleted or moved.

## Building

Requires a TeX distribution providing **XeLaTeX**, `latexmk`, and BibTeX, plus
the Libertinus fonts used by the template. The document body is entirely
English, so no CJK support is loaded.

```sh
latexmk main.tex
```

or, without `latexmk`:

```sh
xelatex main.tex
bibtex  main
xelatex main.tex
xelatex main.tex
```

`main.pdf` is a build artefact and is not tracked.

## Notebooks

`mu-li-course/ch02-preliminaries/` contains committed Jupyter notebooks and
scripts covering Chapter 2 of *Dive into Deep Learning* onwards. **These are
outside the scope of this rewrite**: they have not been modified, moved,
renamed, or deleted, and the book does not attempt to duplicate them. Only the
Chapter 1 handwritten notes were typeset into the book.

## Sources and citation principles

The notes were written while studying the following. They are learning sources,
not sources of text: every definition, derivation, and worked example in the book
is written out independently, and no textbook or lecture prose is reproduced.

- Gilbert Strang, *Introduction to Linear Algebra*, 6th ed., Wellesley–Cambridge
  Press, 2023
- Gilbert Strang, *18.06 Linear Algebra*, MIT OpenCourseWare, Spring 2010
- Joel R. Hass, Christopher E. Heil, Maurice D. Weir, *Thomas' Calculus*,
  14th ed., Pearson, 2018; MIT 18.01 / 18.02 OpenCourseWare
- Dimitri P. Bertsekas, John N. Tsitsiklis, *Introduction to Probability*,
  2nd ed., Athena Scientific, 2008; MIT 6.041 OpenCourseWare. MIT 18.05 uses its
  own course notes (Orloff & Bloom) and is cited separately
- Aston Zhang, Zachary C. Lipton, Mu Li, Alexander J. Smola, *Dive into Deep
  Learning*, Cambridge University Press, 2023

Each chapter opens with a `Sources:` line naming the sections it was written
against. Full entries are in `references/references.bib`.

## Status

The notes are maintained rather than finished. Content that could not be read
confidently from a handwritten page, or that has no source behind it yet, is
marked `[needs verification]` in the text rather than filled in by guesswork.

## Licence

The repository `LICENSE` covers the notes. The vendored KaoNotes template files
are covered by `LICENSE-LPPL-1.3c.txt` instead.
