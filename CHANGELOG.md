# Changelog

All notable changes to the Distinct VS Code extension are documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).


## [0.10.2] - 2026-11-15

### Fixed

- **FTUE Context ready**: after connecting AI and recreating the local Context API with embeddings, the home page shows full runtime status instead of staying in limited mode.
- **FTUE startup**: **Context ready** no longer stays on “waiting”; startup progress dismisses once activation completes.
- **Table Info** and schema webviews: load without blocking on PocketBase realtime; staged startup with clearer handling when initialization is still in progress.

### Changed

- **Query-only FTUE**: simplified finish step when you are not setting up AI context.
- **Schema PocketBase**: smarter readiness checks before mounting schema webviews (container runtime only; host PocketBase binary removed).

## [0.10.1] - 2026-11-14

### Fixed

- **Marketplace package**: republish with the container-based local runtime (Docker Compose). Marketplace 0.10.0 shipped a pre-cutover host bundle; install **0.10.1** or newer for container startup.

## [0.10.0] - 2026-11-14

### Changed

- **Local services** run as version-pinned containers (schema PocketBase, Context API, SQL language server) supervised by Docker Compose instead of host binaries.

## [0.9.7] - 2026-05-28

### Fixed

- **Without sign-in**: datasets and the schema explorer load correctly; table edits and schema sync work when using the extension locally without an account.
- **Optional sign-in**: the local data layer stays stable across auth updates — no unnecessary rebuilds or race conditions when sign-in state changes.

## [0.9.6] - 2026-05-26

### Added

- **Optional sign-in**: use the extension without an account when allowed — run local queries, manage datasets, and use individual mode with data stored on your machine.
- **Send feedback** without signing in, with an optional contact email field when you want a reply.
- **Local MCP** for unsigned individual users (same local server as when signed in to an individual account).

### Changed

- **Signed-out** screen: when sign-in is optional, copy explains that local data and queries need no account; sign-in is presented as unlocking account features.
- **Home** and **Settings** are usable without sign-in when auth is not required; sign-in remains available from the header.
- Extension access follows a remote **access policy** (`extension_auth_required`) instead of always requiring sign-in on launch.

## [0.9.5] - 2026-05-19

### Changed

- Marketplace **README**: **About us** team section uses HTML layout with smaller photos (75px) and LinkedIn links with safe `rel` attributes for consistent marketplace rendering.

## [0.9.3] - 2026-05-19

### Changed

- Marketplace **README**: team photos use sized HTML images so they display at a consistent width in the marketplace listing.

## [0.9.2] - 2026-05-19

### Added

- **Pin tabs** in the data view: pin a result tab so rerunning a query opens a new tab instead of replacing the pinned one.

### Changed

- **Data grid**: smoother column sizing when switching tabs or showing the grid again (layout remeasurement when a panel becomes visible or active).
- **Select all** (Ctrl/Cmd+A) in the data grid: eligibility updates correctly when switching between dock panels.
- Marketplace **README**: **About us** section with team photos and LinkedIn links.

## [0.9.1] - 2026-05-19

### Added

- **Home** page: **Use AI** info box describing the `/distinct` skill and making tables accessible to agents.

### Changed

- **Home** page layout: navigation cards appear first; the **What can I do with DISTINCT?** tips section sits below with a clearer heading and a two-column grid.
- **Home** info boxes: refined styling and hover state; shortcut labels use consistent **Cmd** / **Ctrl** spelling on macOS.
- Marketplace **README** links to [distinct.sh](https://distinct.sh/) for more about the extension.

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