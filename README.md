# FlowSpace — Tester Access

FlowSpace is a fast, native workbench for MuleSoft development: it renders
Mule 4 configuration XML on an Anypoint-Studio-style canvas, lets you edit
component properties (including SQL, DataWeave bodies, and scheduler
settings) with byte-precise saves, and adds multi-workspace profiles,
embedded terminals, and a built-in git review window with a visual flow
diff.

## Install

**➡️ [Download the latest release](https://github.com/nqnconsulting/flowspace-testing/releases/latest)** — or browse [all releases](https://github.com/nqnconsulting/flowspace-testing/releases).

Grab the installer for your OS from the release's assets:

- **macOS** (Apple Silicon): open the `.dmg`, drag FlowSpace to
  Applications. The build is not yet notarized — the FIRST launch must be
  **right-click → Open → Open** (double-click will be blocked by
  Gatekeeper).
- **Windows**: run the `-setup.exe` (or `.msi`). SmartScreen will warn on
  the unsigned binary — choose **More info → Run anyway**.
- **Linux**: `chmod +x` the `.AppImage` and run it, or install the
  `.deb`/`.rpm`.

## Quick start

1. **Add Workspace** (top-left) → pick any Mule 4 project folder (the one
   containing `src/main/mule/`).
2. Click an XML config in the explorer — flows render on the canvas.
   Multiple files open as tabs; unsaved edits survive tab switches.
3. Click any component → edit its properties in the right panel (try a
   DB SQL query or a Scheduler). Saves rewrite ONLY the bytes you changed.
4. Toggle **Diagram | XML** for the raw source (editable, validated).
5. **Terminal** button (top-right): a real shell per workspace, splittable
   (Cmd/Ctrl+N opens a pane to the right).
6. **Git** button (top-right): Add repository → pick a repo → changes
   list, side-by-side diffs, and for Mule configs a **Flow diff** view
   that marks added/changed components right on the canvas.
7. **Profiles** (sidebar): separate workspace sets per client/org —
   switching never kills your terminals.
8. Dark mode: ☾ in the sidebar.

## Feedback

Please file everything — bugs, confusion, wishes — as **Issues** on this
repo. A screenshot plus what you clicked is perfect. If the app ever shows
a blank window or a dead button, say what you did right before; that's
gold for us.

## Notes for testers

- Windows and Linux builds are young — the terminal and file dialogs
  there have had less testing than macOS. Reports especially welcome.
- Your project files: edits happen only when you save, all writes are
  validated XML, and the app never touches git credentials — every git
  operation runs read-only against the repo you added.
