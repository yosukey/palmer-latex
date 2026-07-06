## [2.0.0] - 2026-07-07

### Added
- `gap-ratio` option: uniformly scales the white space around the notation. Accepts a value in `[0, 1]` (`1` = default/maximum spacing, `0` = tightest); out-of-range values are clamped with a warning.
- `no-reverse` option: displays the upper-left and lower-left quadrants in input order, disabling the automatic mesial-to-distal reversal.
- `no-vert` option: suppresses the vertical (midline) bar (replaces the former `novert` keyword; see Removed).
- `\palmerset` command: applies any of the options as defaults for the whole document (or current group); options given in an individual call override them.

### Changed
- **Breaking:** The optional argument is now a comma-separated key-value list. Vertical alignment must be specified as `align=base|center|bottom` instead of the bare `base`/`center`/`bottom` used in v1.x (`centre` remains accepted as a synonym for `center`).
- Updated the example file (example.pdf) to document the new key-value interface and the added options.

### Removed
- **Breaking:** The `novert` keyword placed in the sixth or seventh (midline) argument is no longer recognized. Use the `no-vert` option in the optional argument instead.

## [1.0.2] - 2026-02-27

### Changed
- Add explicit `line cap=rect` and `line width=0.04em` options to the TikZ drawing environment for more consistent cross-bar rendering across TeX engines and font sizes.
- Rewrote the example file (example.pdf). (2026-03-04)

## [1.0.1] - 2025-09-08

### Added
- Add standard package identification (`\ProvidesPackage`).
- Add robust error handling (`\PackageError`) to stop compilation if all four quadrants are empty.

### Changed
- Changed main command definition from `\newcommand` to `\DeclareRobustCommand` to improve stability in section headings and other moving arguments.
- Replaced internal semantic length commands (e.g., `\lowerOnlyBaseShift`, `\vbaroverhangsetting`) with their hardcoded values. This change simplifies the internal code structure while ensuring identical typesetting output to v1.0.0.

## [1.0.0] - 2025-07-01
### Added
- Initial release.
