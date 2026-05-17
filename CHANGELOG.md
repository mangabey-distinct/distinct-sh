# Changelog

All notable changes to the Distinct VS Code extension are documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).


## [0.9.0] - 2026-05-17

This **minor** bump reflects a more **stable** extension build, released together with a **better website** for Distinct.

### Added

- **Data grid**: **select all** (Ctrl/Cmd+A), clearer **row selection** and copy for full-row selections, smoother **scroll** behavior, and faster row-height updates; **search** within a table's columns in the schema explorer.
- Shortcuts for **AI chat**: add the current table, paste the editor selection, and **fix SQL with the agent** from query errors or table info.

### Changed

- Clearer **signed-out** messaging and small **sign-in** improvements.
- Simpler **Home** extension settings and removal of the in-app **version update banner**.
- Marketplace **README** updated with new screenshots.

## [0.8.10] - 2026-05-15

### Added

- Guided **first-time experience** on the Home page with steps and a progress indicator.
- Option to **open the Home page when the extension starts** (toggle from Home).
- **Refresh datasets** from the settings page.
- **SQL completion settings** on the Home settings page (for example table names with project IDs and backticks), applied to the BigQuery language server.
- **Run** and **copy** actions for queries from the query UI.
- **Copy to clipboard** for knowledge items and for table identifiers in the schema explorer.
- **Table info banner** when refreshing table statistics hits your configured data scan limit, with a quick link to settings.

### Changed

- Updated **bigquery-sql-completion** to **0.3.2** with improved language server integration.
- **Charts** in the extension now use Recharts.
- **Long queries** are supported reliably (large SQL is stored so it is no longer limited by record size).
- **Vertex AI** connections use the **global** location as default if not set to ither location.
- Refined **usage analytics** (telemetry events and fields).
- Visual updates across the extension: colors, icons, search toggle, data view tabs, parameters panel, and schema explorer.
- **Data grid** behavior when tabs have a lot of rows and columns.
- **SQL parameters** panel redesigned for clearer editing.
- Updated the embedded **Distinct** BigQuery skill used by agent integrations.

### Fixed

- **Data view tabs**: warning export filename and sticky headers that are allways visible.

## [0.8.9] - 2026-05-09

### Added

- **Send feedback** from the Home page and from the Schema Explorer Actions panel (`distinct.openFeedback`), including a form for bug reports, feature requests, and general feedback when you're signed in.

## [0.8.8] - 2026-05-09

### Added

- Initial addition of LICENSE file for the VS Code extension.

## [0.8.6] - 2026-05-09

### Added

- Initial addition of README and CHANGELOG files for the VS Code extension as well as the Marketplace listing structure.

## [0.8.5] - 2026-05-09

### Added

- The start of this changelog.