# KAN Research Preparation

Study material for preparing independent research on Kolmogorov-Arnold
Networks (KAN). The repository now has two deliberately separate parts:

1. a single, typeset book containing the mathematical foundations; and
2. Jupyter notebooks following *Dive into Deep Learning* (D2L).

## Contents

### Mathematical notes

- [Read the PDF](math-notes/Mathematical-Foundations-for-KAN.pdf)
- [LaTeX source and build instructions](math-notes/README.md)

The book covers the linear algebra, calculus, probability, optimisation, and
learning foundations needed for later KAN work. The PDF is the reading copy;
its LaTeX source is retained so the book remains editable and reproducible.

### Dive into Deep Learning notebooks

- [Notebook workspace](notebooks/dive-into-deep-learning/)

This area is reserved for chapter-by-chapter D2L notebooks and is still a work
in progress. It is kept separate from the mathematical book so that future
code and experiments do not recreate the repository's former lecture-folder
structure.

## Repository layout

```text
math-notes/
  Mathematical-Foundations-for-KAN.pdf   published reading copy
  README.md                              source and build notes
  source/                                LaTeX source, bibliography, and styles

notebooks/
  dive-into-deep-learning/               D2L notebooks (work in progress)
```

## Status

The mathematical notes are maintained as one continuous document. The D2L
notebook collection is incomplete and will grow independently.

## Licence

Except for separately identified third-party material, the original
mathematical prose, explanations, examples, derivations, and arrangement in
`math-notes/` are licensed under
[CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/).

You may share unmodified copies for non-commercial purposes with appropriate
attribution. Commercial use and distribution of modified, translated,
abridged, or otherwise adapted versions require separate written permission
from the copyright holder.

See [`LICENSE-CONTENT.md`](LICENSE-CONTENT.md) for the complete scope and
licensing notice.

Vendored KaoNotes/kaobook class and style files remain under the LPPL 1.3c.
Notebooks and source code are not covered unless explicitly stated otherwise.

Earlier repository versions remain subject to the licences under which they
were originally published.
