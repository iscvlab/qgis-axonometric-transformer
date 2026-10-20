# Changelog

## [1.2.2] - Hotfix

- **Fixed Windows Multi-Format Clipboard Integration**: Restored the Qt `QMimeData` OLE `IDataObject` and `CF_HDROP` file drop pipeline on Windows. Eliminates the issue where `_copy_windows_in_memory` emptied the clipboard and set only raw string formats, preventing paste into external design applications.
- **Direct 1-Click Transparent Paste Across All Design Apps**: Seamlessly paste (`Ctrl+V` / `Cmd+V`) with 100% full alpha transparency into **Adobe Illustrator** (native in-memory PDF `/SMask`), **Figma** (in-memory SVG + PNG), **Affinity Designer**, **Photoshop**, **Microsoft Office** (PowerPoint, Word), **Discord**, **Slack**, and **Windows File Explorer** (pastes `.png` directly).
- **Suppressed Text Auto-Detection in Illustrator**: Removed `text/plain` from the clipboard payload to prevent Adobe Illustrator from mistakenly pasting a text frame containing the temporary file path instead of the graphic.
- **Cleaned Qt6 / QGIS 4 Imports**: Explicitly imported `QUrl` across all PyQt shims, maintaining 100% compliance with portal AST linters and the green **QGIS 4 Ready** badge.
- **100% Flake8 / PEP8 Code Quality Compliance**: 0 violations across entire codebase.

## [1.2.1]

- In-Memory Multi-Format Clipboard Engine: Direct embedded paste with transparent background into Adobe Illustrator and Affinity Designer via in-memory PDF with soft mask alpha (`/SMask`).
- Added `image/svg+xml` clipboard format for Figma and `image/png` for Canva, Photoshop, and Microsoft Office.
- Zero temporary disk files during clipboard copy (100% in-memory transit).
- Fixed Qt6 AST forward-compatibility: explicitly scoped `QPageSize.Unit.Point` and `QPageLayout.Orientation.Portrait` for the in-memory PDF writer, earning the official green **QGIS 4 Ready** badge.
- 100% Flake8 / PEP8 code quality compliance (0 violations across entire codebase).
- Upgraded pre-flight security gates and privacy protections.

## [1.2.0]

- Added Framing Fill ground option with customizable color and opacity.
- Added 3D Base Plate opacity slider with 5 percent step snapping.
- Solid 3D Base Plate engine: continuous front-wall extrusion with dynamic winding order detection, Painter's algorithm depth sorting, and solid top cap under transparent maps.
- Clean aligned Section 3 UI grid layout with dual sliders.
- Verified 100 percent Qt6 / QGIS 4 forward-compatibility.

## [1.1.3]

- Approved and published on official QGIS plugin repository (Plugin ID: 6219).
- Passed portal security scan (0 issues) and Qt6 / QGIS 4 forward-compatibility.
- Fixed root package naming slug for seamless in-app Plugin Manager installation.
- 1-click in-app install live via QGIS Plugin Manager.
