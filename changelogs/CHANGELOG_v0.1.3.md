# Changelog

## [v0.1.3] - 2026-07-13

### Added
* Added the foundation for **optional CKSP Language Server support**. CKSP Tools can detect and start Language Server functionality provided by the selected CKSP compiler.
  > [!NOTE]
  > Compatible CKSP compiler versions have not been released yet. Until then, CKSP Tools continues to use its built-in language features.
* Added the **CKSP: Restart Language Server** command.
* Added Kontakt Log button to **Clear Log on Compile**.

### Changed
* Improved GitHub release fetching with retries, a longer timeout, and a cached fallback.
* Built-in editor providers now defer capabilities handled by a running Language Server while keeping CKSP Tools-specific completions available.
* Added a dedicated Language Server crash log location.

### Fixed
* Fixed syntax highlighting for curly-brace comments inside function parameter lists.
* Fixed syntax highlighting for type annotations in bare method headers such as `write(self, array: int[])`.
