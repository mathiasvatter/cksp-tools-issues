# Changelog

## [v0.0.12] - 2026-02-11

> **Note**: This release includes significant new features, especially related to **Kontakt integration**. I will try to add more detailed documentation to those soon, but in the meantime, feel free to explore and reach out if you have any questions or feedback! 

### Added

#### Kontakt Integration
* **Custom Webview when opening `*.nki` files** with button controls to open the file in Kontakt, close the running Kontakt instance and view the Kontakt Console log.
* Ability to **assign resource (script) files to an instrument's script slots** from the NKI editor with the option to open them directly. Assignments are stored in workspace settings, so they persist across sessions.
* **Diagnostics View**: highlights Kontakt **errors, warnings, and info messages** directly in resource files and aggregates them in the **Problems Tab**.
* **Console to Source navigation**:  
  – Added a **resource column** to the Kontakt Console Webview mapping log entries to their source files.  
  – `Cmd+Click` log entries to jump to the corresponding line in the linked resource file.
  – Selected lines are visually highlighted via VS Code decorations.  
* **Assignment** of resource files to individual console log entries directly from the Kontakt Console Webview via a new context menu entry.
* Context menu entry to open `*.nki` files in Kontakt directly from the **Browse Panel**.
* **Clear Log** and **Pause Log** buttons in the Kontakt Log Webview.
* New **toolbar** in the Kontakt Log Webview to hide/unhide log columns.
* VS Code command to **close a running Kontakt instance**.
> **Windows restriction**: only one `.nki` file can be open in Kontakt at a time.

#### File & Editor Support
* Added **file icons** for `.nki`, `.nkr`, and `.nka`.
* Added **language configuration and TextMate grammar** for `.nka` files with basic syntax highlighting.
* Highlighting support for **Javadoc/Doxygen-style annotations (`@...`)** in `.cksp` and `.ksp` files.
* Highlighting for **task markers** such as `TODO`, `FIXME`, etc. (without requiring `@`) in `.cksp` and `.ksp` files.
* Added auto-closing support to the `namespace` keyword, so typing `namespace MyNamespace` and pressing `Enter` will insert an indented `end namespace` block.
* Added completion support for **basic types** (`int`, `real`, `bool`, `string`, `any`, `number`) and **structs** with documentation in completion item details.

#### Compiler & Version Management
* Compiler binaries are now stored in **VS Code global storage**, preventing re-download on each extension update.
* Added **automatic cleanup of old compiler versions** to prevent clutter. This is configurable with two new settings:
    - `cksp.autoCleanupCompilers`  
    - `cksp.maxStoredCompilerVersions`
* Removed optional release downloads — new CKSP releases are now **automatically downloaded** when detected.

#### Editor & UX Improvements
* Inlay hints are now shown only when a function exceeds a configurable parameter threshold. This is configurable via this setting:
    - `cksp.inlayHintsMinParameterCount`
* Inlay hints are omitted when function call arguments share common substring with the parameter name to reduce visual clutter.
* Improved parsing efficiency of Kontakt console output.
* Improved performance of the Semantic Highlighter.
* Main file selection (for compilation) now **sorts candidate file paths by length** for more predictable results.
* Introduced `Logger.ts` to manage debug and extension logs in a dedicated VS Code Output channel.
* Updated styling of webviews.

---

### Fixed
* Fixed [#2](https://github.com/mathiasvatter/cksp-tools-issues/issues/2): Added missing `sh_left` and `sh_right` documentation in the Hover Provider.
* Fixed [#11](https://github.com/mathiasvatter/cksp-tools-issues/issues/11): More engine variables now correctly appear in auto-completion.
* Fixed [#15](https://github.com/mathiasvatter/cksp-tools-issues/issues/15): Added missing `get_control_par_string_arr()` and `get_control_par_real_arr()` definitions.
* Fixed [#16](https://github.com/mathiasvatter/cksp-tools-issues/issues/16): Added missing `purge_group` and `get_purge_state` support to the extension.
