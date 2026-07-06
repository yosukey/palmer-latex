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
- `[options]`: Optional comma-separated list of key–value settings (see [Options](#options))
- `<UL>`: Upper left quadrant
- `<UR>`: Upper right quadrant
- `<LR>`: Lower right quadrant
- `<LL>`: Lower left quadrant
- `<upper midline>`: Symbol for upper midline position
- `<lower midline>`: Symbol for lower midline position

Note that “left” and “right” here refer to the notation’s visual representation, not the anatomical left
and right of the jaw.

For the upper-left and lower-left quadrants, characters are entered from mesial to distal (natural reading
order) and are automatically reversed for display, following standard dental charting conventions. An error
is raised if all four quadrant arguments are empty.

## Options

The optional first argument accepts a comma-separated list of the following keys:

- `align=base|center|bottom`: Vertical alignment of the notation within a line of text (default: `base`; `centre` is accepted as a synonym for `center`).
- `gap-ratio=<number>`: A value in the range `[0, 1]` that uniformly scales the white space around the notation. The default of `1` gives the maximum spacing, and `0` gives the tightest. Out-of-range values are clamped, with a warning.
- `no-vert`: Suppresses the vertical (midline) bar. Useful for representing a single jaw without distinguishing left from right. When active, the midline arguments are ignored.
- `no-reverse`: Displays the upper-left and lower-left quadrants in the input order instead of reversing them (affects only the UL and LL quadrants).

Several keys may be combined, for example:

```latex
\Palmer[align=center, gap-ratio=0.5]{12}{12}{12}{12}{}{}
```

The Boolean options `no-vert` and `no-reverse` may be written on their own as shorthand for `no-vert=true`
and `no-reverse=true`.

### Document-wide defaults

`\palmerset` applies one or more of the options above to every subsequent `\Palmer` call, so common defaults
need not be repeated. Options given in an individual call override these defaults for that call only.

```latex
\palmerset{align=center, gap-ratio=0.5}
\Palmer{1}{1}{1}{1}{}{}                 % uses the defaults above
\Palmer[gap-ratio=1]{2}{2}{2}{2}{}{}    % overrides gap-ratio for this call
```

Because `\palmerset` follows TeX's grouping rules, call it in the preamble (after `\usepackage{palmer}`) or at
the start of the document to set defaults for the whole document.

## Changes in Version 2

Version 2 introduces a key–value interface for the optional argument. When upgrading from version 1, note:

- **The optional argument is now a key–value list.** Use `align=center` (and `align=base`, `align=bottom`) instead of the bare `center` / `base` / `bottom` of earlier releases.
- **The vertical bar is suppressed with the `no-vert` option.** The old `novert` keyword placed in the sixth or seventh (midline) argument is no longer recognized.
- **New `gap-ratio` option** for uniformly tightening the white space around the notation.
- **New `no-reverse` option** for disabling the automatic reversal of the left quadrants.
- **New `\palmerset` command** for setting options for a whole document.

For detailed documentation and more examples, please refer to the example.pdf file included in this repository.

## License

Copyright 2026-- Yosuke Yamazaki  
Released under the LaTeX Project Public License 1.3 or later

## Support This Research

This dental notation typesetting LaTeX macro was developed by Dr. Yamazaki at Nihon University School of Dentistry
as part of ongoing research in oral health and dental informatics. 

This software is freely available for all uses, including commercial applications. 
If you find it valuable for your work or publishing, please consider supporting 
our continued research.

## Acknowledgement

This work was conducted with the support of JSPS KAKENHI Grant Number JP25K15395.
