# Master Thesis (FAU, 2026)

LaTeX source for my MSc thesis at FAU, Lehrstuhl für Technische Mechanik (LTM).

**Title:** Bridging Interphase and Interface Models for Composites: Parameter Identification in Mechanical Problems

*Plain-English version: training a neural network to translate between two ways of modeling the thin boundary layer between particles and matrix in composite materials.*

**Author:** Sumanth Reddy Settipalli
**Supervisor:** Soheil Firooz, M.Sc.
**Institution:** Lehrstuhl für Technische Mechanik (LTM), Friedrich-Alexander-Universität Erlangen-Nürnberg
**Year:** 2026
**Status:** Submitted February 2026, defended March 2026

## What this thesis is about

Particle-reinforced composites have a thin interphase region between inclusion and matrix that affects effective elastic properties. Two modeling approaches exist: a 3-Layer Interphase model (finite-thickness coating) and an Extended Interface model (zero-thickness with surface parameters). This thesis identifies the Extended Interface parameters that reproduce the same effective bulk and shear moduli as a given 3-Layer configuration, using a Physics-Informed Neural Network built on Mori-Tanaka homogenization.

## Code

The neural network implementation lives in a separate repository: [PINN-for-composite-interface-identification](https://github.com/Sumanthreddy-DE/PINN-for-composite-interface-identification).

This repository contains only the written thesis (LaTeX source + figures).

## Build

```bash
latexmk -pdf main.tex
```

Or with plain `pdflatex`:

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

## License

The written thesis content and figures in this repository are licensed under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license. See [`LICENSE`](LICENSE).
