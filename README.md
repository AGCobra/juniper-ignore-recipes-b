# Juniper Cursor Ignore Recipe Builder

A small, dependency-free browser utility for choosing optional `.cursorignore` patterns.

The juniper recipe notebook keeps dependency folders, generated builds, and test reports in separate choices.

## Use

Open `docs/index.html` in a browser and choose any of these groups:

- Dependencies: `node_modules/`
- Generated builds: `dist/` and `build/`
- Test coverage: `coverage/`
- Logs: `*.log`

The preview updates in a fixed order; Copy recipe copies its text or selects it for manual copying if clipboard access is unavailable.
All four groups are selected initially, and the initial preview remains usable without JavaScript.
Choosing no groups produces a comment with no exclusion patterns.

Review the preview, then merge only the lines you need into your project-root `.cursorignore`; keep any existing rules you still need.
Cursor uses gitignore syntax and already ignores many common files by default.
These examples are optional.
Terminal and MCP tools may still access ignored files, so `.cursorignore` is not complete protection for secrets.

Source: [Cursor documentation: Ignore files](https://cursor.com/docs/reference/ignore-file), checked September 16, 2026.

## How it works

One HTML file contains the page, a little CSS, and vanilla JavaScript.
There is no build step, dependency installation, upload, configuration change, filesystem access, or script-initiated network request.
The page creates text for you to review and copy; it does not install or apply rules.

## Publishing experiment

This independent utility is also part of a public experiment on discovering newly published pages through text search.
Identical copies may be published to compare whether a relevant directory link changes discoverability.
It is not affiliated with Cursor.
