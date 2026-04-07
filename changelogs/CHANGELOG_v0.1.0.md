# Changelog

## [v0.1.0] - 2026-04-05

### Added

#### Project & Workflow
* Added **Welcome View in Project Settings** that is shown if no Kontakt project is found with the option to create one.
* Added **file watchers** for `.cksp`, `.ksp`, `.nkr` and `.png` files to automatically update UI and language features on file changes.
* Added new command **CKSP: Reindex Workspace** to manually rebuild workspace symbols, definitions and project UI state.
* Added new command **CKSP: Initialize Kontakt project**, automatically creating:
  * folder structure used for *Native Instrument Libraries*
  * `.nki` file in `Instruments/` with first script slot linked to `scripts/main.txt`
  * linked resource container and `Resources/` folder
  ```
    ├── Instruments
    │   └── <ProjectName>.nki
    ├── Samples
    │   ├── Resources
    │   │   └── scripts
    │   │       └── main.txt
    │   └── <ProjectName>.nkr
    ├── dev
    └── main.cksp
  ```
  ![create-project](https://mathiasvatter.github.io/cksp-assets/assets/create_project.gif)


#### Editor & Language Features
* Added **hover documentation and completion items** for CKSP **`#pragma` directives** ([#21](https://github.com/mathiasvatter/cksp-compiler-issues/issues/21)).
* Improved **completion items** for arrays now showing additional size information
![array_completion](https://mathiasvatter.github.io/cksp-assets/assets/array_sizes_completion.gif)


#### UI & UX
* Added **“Help and Feedback” section** to the sidebar.
* Improved **GitHub Release Webview** layout (better alignment of assets and markdown styling)
* Improved **Project Settings UI**:
  * Fixed theme-related button color inconsistencies  
  * Shortened long paths in dropdown menus for better readability  


### Changed
* Updated **compiler version sorting**: stable releases are now shown **before alpha versions**.
* Refactored **background feature registration** in `extension.ts` by separating provider registration, workspace watchers and scheduler logic into dedicated helper functions.
* Added **debounced document updates** for CKSP text changes to reduce repeated reparsing and definition rebuilds while typing.
* Updated **README.md** with badges and a linked YouTube video.


### Fixed 
* Fixed issue [#20](https://github.com/mathiasvatter/cksp-compiler-issues/issues/20): **`ui_control` completion items** no longer retain unwanted parentheses.
* Fixed issue where **`control_par` completion items** appeared twice when using `->` notation.
* Fixed issue where the **completion provider could crash** when resolving certain built-in constants.
