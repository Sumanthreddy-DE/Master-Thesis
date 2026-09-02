# Master Thesis (FAU, 2026)

LaTeX source for my MSc thesis at FAU, Lehrstuhl für Technische Mechanik (LTM).

**Title:** Bridging Interphase and Interface Models for Composites: Parameter Identification in Mechanical Problems

*Plain-English version: training a neural network to translate between two ways of modeling the thin boundary layer between particles and matrix in composite materials.*

**Author:** Sumanth Reddy Settipalli
**Supervisor:** Soheil Firooz, M.Sc.
**Institution:** Lehrstuhl für Technische Mechanik (LTM), Friedrich-Alexander-Universität Erlangen-Nürnberg
**Year:** 2026
**Status:** Submitted February 2026, defended March 2026

## Read the thesis

[Settipalli-MSc-Thesis-FAU-2026.pdf](Settipalli-MSc-Thesis-FAU-2026.pdf) (82 pages) is the compiled thesis, built from the `main.tex` in this repository. No LaTeX toolchain is needed to read it.

## What this thesis is about

Particle-reinforced composites have a thin interphase region between inclusion and matrix that affects effective elastic properties. Two modeling approaches exist: a 3-Layer Interphase model (finite-thickness coating) and an Extended Interface model (zero-thickness with surface parameters). This thesis identifies the Extended Interface parameters that reproduce the same effective bulk and shear moduli as a given 3-Layer configuration, using a Physics-Informed Neural Network built on Mori-Tanaka homogenization.

## Code

The neural network implementation lives in a separate repository: [PINN-for-composite-interface-identification](https://github.com/Sumanthreddy-DE/PINN-for-composite-interface-identification).

This repository contains the written thesis only: the compiled PDF, the LaTeX source and the figures.

## Build

```bash
latexmk -pdf main.tex
```

Or with plain `pdflatex`:

```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

The bibliography is embedded in `main.tex` via `filecontents`, so no separate
`.bib` file is required. It is processed with `biber`, not `bibtex`, because the
document loads `biblatex` with `backend=biber`.

## License

The written thesis content and figures in this repository are licensed under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license. See [`LICENSE`](LICENSE).
