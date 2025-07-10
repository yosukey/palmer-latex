# palmer.sty: Zsigmondy-Palmer Dental Notation Package in LaTeX

A LaTeX package for representing Zsigmondy-Palmer dental notation using TikZ. This package allows dental professionals, educators, researchers, and publishing specialists to efficiently typeset typographically consistent and visually balanced dental notation in academic and clinical documents.

## Overview

The palmer package provides a simple syntax for creating dental notation diagrams that follow the Zsigmondy-Palmer system. 

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

## Support This Research

This dental notation typesetting LaTeX macro was developed by Dr. Yamazaki at Nihon University School of Dentistry
as part of ongoing research in oral health and dental informatics. 

This software is freely available for all uses, including commercial applications. 
If you find it valuable for your work or publishing, please consider supporting 
our continued research.
