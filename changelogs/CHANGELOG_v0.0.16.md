# Changelog

## [v0.0.16] - 2026-03-15

>The cksp-compiler repository on Github is now **public**. The Github Release Service from `CKSP Tools` will automatically download from there now.

### Changed
* Updated **GitHub repository references** to use the new public **`cksp-compiler`** repository where applicable.
* Updated the **compiler issues repository references** to `cksp-compiler`.
* Improved **OnTypeFormattingProvider** behavior: CKSP constructs are now only **auto-closed when the next non-empty line is not more indented than the current line**, preventing accidental insertion of duplicate closing blocks.

