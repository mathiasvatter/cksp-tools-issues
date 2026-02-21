# Changelog

## [v0.0.13] - 2025-10-07

### Added
* **Rudimentary parsing of `.nki` metadata** with metadata section when opening an instrument in the custom NKI editor.
* **Completion provider for import paths**, enabling faster and more accurate module imports.

### Changed
* Updated **Kontakt warning, error, and info colors** to closely match VS Code’s built-in diagnostic styling for a more consistent experience.

### Fixed
* Fixed issue where changing the **resource file assigned to a script slot** did not automatically remap existing Kontakt log messages to the newly selected file.
* Fixed issue where the **“Close Kontakt” button** remained enabled after Kontakt had already been closed.
* Fixed issue where reopening Kontakt would fail to recreate the **Kontakt Log Webview** properly.