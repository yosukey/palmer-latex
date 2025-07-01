# palmer.sty: Palmer Dental Notation Package in Latex

A LaTeX package for representing Zsigmondy-Palmer dental notation using TikZ. This package allows dental professionals and researchers to easily typeset dental charts and notations in academic documents.

## Overview

The Palmer package provides a simple syntax for creating dental notation diagrams that follow the Zsigmondy-Palmer system. It supports:

- Single tooth notation
- Quadrant representation
- Full mouth diagrams
- Custom alignment options
- Midline symbol placement

## Installation

Place the file in the working directory or in the LaTeX installation path, and include the following command in the preamble:

```
\usepackage{palmer}
```

## Basic Usage

```latex
\Palmer[<options>]{<UL>}{<UR>}{<LR>}{<LL>}{<upper midline>}{<lower midline>}
```

Where:
- `[options]`: Optional alignment mode (center, base, bottom)
- `<UL>`: Upper left quadrant
- `<UR>`: Upper right quadrant
- `<LR>`: Lower right quadrant
- `<LL>`: Lower left quadrant
- `<upper midline>`: Symbol for upper midline position
- `<lower midline>`: Symbol for lower midline position

Note that “left” and “right” here refer to the notation’s visual representation, not the anatomical left
and right of the jaw.

For detailed documentation and more examples, please refer to the example.pdf file included in this repository.

## License

Copyright 2025-- Yosuke Yamazaki  
Released under the LaTeX Project Public License 1.3 or later
