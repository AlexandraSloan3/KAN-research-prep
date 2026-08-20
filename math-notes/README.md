# Mathematical Foundations for KAN

[`Mathematical-Foundations-for-KAN.pdf`](Mathematical-Foundations-for-KAN.pdf)
is the published reading copy of the mathematical notes.

The editable LaTeX project is kept in [`source/`](source/). It contains one
file per chapter, the bibliography, an empty figures directory, and the
vendored KaoNotes/kaobook class files required by the document.

## Build

From `math-notes/source/`, run:

```sh
latexmk main.tex
```

The build requires XeLaTeX, BibTeX, and the Libertinus fonts. A local build
creates `source/main.pdf`, which is ignored by Git. After reviewing it, replace
the published PDF in this directory when a new reading copy is ready.

The vendored class and style files are distributed under the LaTeX Project
Public License 1.3c; see [`source/LICENSE-LPPL-1.3c.txt`](source/LICENSE-LPPL-1.3c.txt).
