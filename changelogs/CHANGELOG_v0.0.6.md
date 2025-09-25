# Changelog

## \[v0.0.6] - 2025-09-25

### Added

* **DotCompletionProvider** for **method auto-completion** when using dot notation.
* **ArrowCompletionProvider** to provide **shorthand control completion items**.
* **Distinction between method and function definitions** for more accurate highlighting and completions.
* **New keyword highlighting** and support for **`bool` typecasting** in CKSP syntax.
* **Documentation** and **Issue Report** buttons in the CKSP sidebar for easier user support.

### Changed

* **Signature Help** now shows function signatures while typing a method call and automatically **skips the first parameter (`self`)**.
* Updated **TextMate grammar** with a new **type pattern** and **`meta.function`** scope for richer syntax highlighting.
* Internal **package logic updated**:
  – Unnecessary files are excluded from the published `.vsix`.
  – HTML files are now bundled as runtime strings instead of static assets.
* **Error messages** in the GitHub Release Panel are now displayed in **English**.

### Fixed

* **Release view refresh** issue resolved: hiding/unhiding pre-releases now updates correctly.
* **Inlay hint alignment fixed** when function parameters span multiple lines.
