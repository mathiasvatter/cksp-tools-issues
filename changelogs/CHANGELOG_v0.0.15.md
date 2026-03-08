# Changelog

## [v0.0.15] - 2026-03-08

### Added

#### Project Settings Panel:

* Added **workspace dropdown** to select the **default Kontakt version** used by the project.
* Added **dropdown in the NKI editor** to configure the **Kontakt version per `.nki` file** made persistent by workspace settings mapping Kontakt executable paths to specific `.nki` instrument files.
* Added **dropdown in the Compile View** to select the **project resource container**.
* Added **placeholder option** in project configuration dropdowns that allows clearing the selected:
  * compiler version
  * main file
  * resource container
  * Kontakt version  
  If a required value is unset, the extension now prompts a **QuickPick selection** when compiling or launching Kontakt.
* Added setting **`cksp.kontaktLogFontSize`** to customize the **font size in the Kontakt Log view**.

#### Editor & Completion
* Added **completion provider for resource picture files**, when typing single or double quotes after `:=`, `,` or `(` to suggest image files from the project resources. For this to work, a resource container must be selected in the project settings. ![resource-completion](https://mathiasvatter.github.io/cksp-assets/assets/resource-pictures-completion.gif)
* Improved **path completion provider** to suggest items for the **next path segment** while typing. ![path-completion](https://mathiasvatter.github.io/cksp-assets/assets/import-path-completion.gif)


### Fixed

* Fixed issue where **Kontakt 8 logs were not shown** in the Kontakt Log panel.  
  The extension now correctly parses log entries since **Kontakt 8 writes logs to `stderr` instead of `stdout`**.
