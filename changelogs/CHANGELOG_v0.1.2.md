# Changelog

## [v0.1.2]

### Added
* Added support for **`#region` and `#endregion` folding**, making it possible to organize and collapse custom sections in `*.ksp` and `*.cksp` files.
  ```cksp
  //#region UI CALLBACKS
  ...
  //#endregion
  ```
* Added rendering and styling for **GitHub-style Markdown alerts** in webviews, including `NOTE`, `TIP`, `IMPORTANT`, `WARNING`, and `CAUTION` blocks.
* Added configurable safeguards that disable expensive language features and workspace indexing for large files. The limits can be adjusted with:
  * `cksp.largeFiles.maxLines` (default: `10000`)
  * `cksp.largeFiles.maxSizeKB` (default: `2048`)
  
  Setting either value to `0` disables that limit.

### Changed
* Improved `.nki` metadata loading by retrieving multiple metadata fields in a single invocation.
* Improved Markdown formatting across the Welcome, Changelog, and GitHub Releases webviews.
* Updated README and documentation links to point to the current public CKSP repositories.

### Fixed
* Fixed [#24](https://github.com/mathiasvatter/cksp-tools-issues/issues/24) and [#25](https://github.com/mathiasvatter/cksp-tools-issues/issues/25): corrected syntax highlighting for **method calls** and the **`override` keyword after function return type annotations**.
* Fixed [#26](https://github.com/mathiasvatter/cksp-tools-issues/issues/26): commas inside quoted strings no longer produce incorrect Signature Help or Inlay Hint argument positions.
* Fixed [#27](https://github.com/mathiasvatter/cksp-tools-issues/issues/27): clearing the Kontakt Log now also clears associated **Problems diagnostics** and file decoration badges.
* Fixed [#30](https://github.com/mathiasvatter/cksp-tools-issues/issues/30): `emphasis` is now converted correctly, preserving spaces and readable formatting in hover documentation.
