# Curriculum Vitae

LaTeX source for my CV. The latest compiled version is [`cv.pdf`](cv.pdf).

Publications are generated from [`publications.bib`](publications.bib) via biblatex.

## Build

```sh
./make.sh   # latexmk -C cv.tex && latexmk -pdf cv.tex
```
