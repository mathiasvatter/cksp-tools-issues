# Changelog

## [v0.1.1] - 2026-05-20

### Added
* Added **parsing and auto-completion support for `.nckp` files**, enabling completion of **UI controls from Kontakt performance files**. *Note: for this to work, a valid resource container path has to be set in Project Settings.*
* Added **JSON file association** for `.nckp` files.
* Added **JSON Schema support** for `.nckp` performance view files to improve validation and editor assistance.

### Changed
* Updated **README badges** and badge URLs after previous badges were marked as retired.

### Fixed
* Fixed [#23](https://github.com/mathiasvatter/cksp-compiler-issues/issues/23): corrected syntax highlighting for:
  * line comments in colon-types,
  * indented `end struct` edge cases.