# Changelog

## [v0.0.9] - 2025-10-28

### Added

* **New Changelog Webview** to display release notes directly within VS Code after each update.
* **Button to open the Welcome Page** from the Changelog View for easier onboarding.
* **sKSP-like shorthand callbacks** added — e.g. `icb`, `ncb`, `rcb`, etc., for faster callback creation.
* **Syntax highlighting** improvements for:
  – Scientific number notation (`1.2e-3`, `.5e2`, etc.)
  – Struct fields declared **without the `declare` keyword**
  – **Methods**, **constructors**, and **#pragma** commands, namely `combine_callbacks`, and `pass_by`.
* Automatic **re-download of previously installed compiler versions** when updating CKSP Tools.

### Changed

* All **UI control snippets** updated and corrected ([#6](https://github.com/mathiasvatter/cksp-tools-issues/issues/6))
* **CSS styles centralized** and **webview titles redesigned** for a cleaner, unified look.
* **Dropdown menu in CompileMainFileView** now correctly refreshes when downloading new versions.
* **Signature Help Provider** improved to distinguish between **type annotations** and built-in **function names** (issues with `: int (`).

### Fixed

* Fixed [#7](https://github.com/mathiasvatter/cksp-tools-issues/issues/7): **constant variable completions** no longer insert the `const` keyword.
* Fixed issue where **UI control variables** sometimes did not appear as completion items.
* Fixed issue where **completion items** were incorrectly suggested **while declaring variables**.
* Fixed bug where **no compiler was selected** when not working inside a VS Code workspace.

