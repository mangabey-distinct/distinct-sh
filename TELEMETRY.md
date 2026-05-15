# Telemetry

DISTINCT can send **anonymous usage information** to help us understand how the extension is used, fix problems, and improve features. Telemetry follows the same rules as other VS Code extensions. See Microsoft’s [VS Code Telemetry Extension Guide](https://code.visualstudio.com/api/extension-guides/telemetry) for how extension telemetry works in general.

## What we collect

In plain terms, we may record things like:

- **Extension health** — whether startup and main services completed successfully and how long key steps took.
- **Feature usage** — that you used a capability (for example running a query, exporting results, syncing schema, signing in, testing a connection, saving a knowledge item, or using chat), whether it succeeded or failed, and **how long it took**.
- **Safe numbers** — things like how many rows or columns were in an export, how long a query took, or the **length of your query in characters** (not the SQL text itself), or how many file attachments you added to a chat message (not the message text).
- **MCP tools** — when a DISTINCT MCP tool runs, we may record the **tool name** (for example `run_query`, `search_context`) and whether it finished without throwing. We do **not** record tool **arguments** or return payloads.
- **AI table analysis** — that indexing or analysis steps ran, how long they took, and high-level counts. We do **not** upload the text we analyzed.
- **UI usage** — that you opened a screen or used a control (using internal labels, not what you typed).
- **Some settings** — that a tracked setting was turned on or off, or otherwise changed. We do **not** record the actual value (for example, not your project id or connection details).
- **Errors (safe summary only)** — a **short internal error category or code** (for example, that something was a permission or timeout issue). We do **not** send the full error message or stack trace, which could sometimes contain sensitive details.

We also attach context such as a random **session id**, which **warehouse type** you are using (for example BigQuery vs Snowflake), which **editor** host you are in, and **when** the event happened. When you are **signed in**, we include an opaque **user id** (not your email), whether you use **individual** or **team** mode, and when you are in team mode your **tenant id** (an opaque org identifier), so we can understand usage per account and organization.

## What we never collect

| We do **not** collect |
| --------------------- |
| Query **text**, parameter **values**, or cell **values** from your data |
| **Names** of tables, columns, datasets, or projects |
| **Descriptions** you or the AI wrote about your data |
| **Chat content** — messages, prompts, answers, or tool arguments/results in telemetry |
| **Credentials** — API keys, tokens, or passwords |
| **File paths** or raw error text that might reveal your environment |

## Your choices

- **Turn telemetry off in VS Code** — Open Settings and set **Telemetry > Telemetry Level** to **Off**, or set `telemetry.telemetryLevel` to `"off"`. That disables this extension’s telemetry along with other VS Code telemetry that respects that setting.
- **Learn more** — You can read about VS Code’s telemetry behavior with: `code --telemetry`.

## Where the data goes

When telemetry is enabled, events are sent to **Microsoft Azure Application Insights**, using the official VS Code extension telemetry support, so handling aligns with typical VS Code extension practices.

If you have questions, please [open an issue](https://github.com/mangabey-monkey/distinct/issues) on our GitHub repository.
