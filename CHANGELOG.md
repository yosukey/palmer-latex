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
