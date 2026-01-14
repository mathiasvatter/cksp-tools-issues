# Changelog

## [v0.0.11] - 2026-01-14

### Added
* **OnTypeFormattingProvider** that automatically closes **KSP blocks** with correct indentation when pressing `Enter`, improving editing flow. For example, pressing `Enter` after typing the line `function myFunction(param1, param2)` will insert `end function` after the cursor. 
* **Syntax highlighting** support for the new pragma parameter **`max_callback_depth`**.

### Changed
* Updated **extension description** and **README.md** for clarity and accuracy.

### Fixed
* Fixed incorrect highlighting where **annotated real arrays** (using the `?` type identifier) were misinterpreted as **ternary expressions**.
* Fixed incorrect highlighting of the opening parenthesis after calls to **built-in functions**.
* Fixed incorrect **macro definition highlighting** inside **struct scopes**.
* Fixed incorrect highlighting of **access chains** within struct scopes.
* Fixed [#10]: **struct member declarations** using modifier keywords (`const`, `read`, etc.) are now highlighted correctly.
* Fixed [#9]: `?` type annotations in **`ui_control` parameters** no longer break syntax highlighting.
* Fixed [#1]: **line comments inside block comments** no longer cause incorrect syntax highlighting.

### Meta
* Issued a **hotfix for the VS Code Marketplace** that needed a version bump. Therefore, **v0.0.10** will be skipped in Github releases.
* Added a **development-mode guard** to prevent force-downloading CKSP compiler versions during local development.
