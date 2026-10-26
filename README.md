# TRACE — Measure Drawing Tool

A clickable prototype for an architectural measure-drawing tool: upload a site scan, let the AI draft a dimensioned plan, review and export it.

## Structure

This is built with Claude's `.dc.html` Design Component format — each screen is a self-contained artboard, laid out on an infinite canvas via `project/canvas.json`.

```
project/
  canvas.json        — board layout / positions
  Main.dc.html        — Home / Projects (card grid + simple list view)
  Scans.dc.html        — Project · Scans workspace (plan/3D/RCP, element table, export queue)
  Archimedes.dc.html   — Project · Archimedes (AI drafting: upload/describe → generate → edit)
  Data.dc.html          — Project · Data (areas, door/window schedule, soil, climate)
  Templates.dc.html    — Starter templates
  Spreadsheet.dc.html  — Raw measurement data grid (editable, CSV export)
  Drawings.dc.html     — Exported drawing files list
  Settings.dc.html     — Workspace preferences
```

## Viewing / editing

These files are authored for Claude's Artifact canvas (Design artifact type). Open the published artifact to view or edit them, or load `project/canvas.json` + the `.dc.html` files back into a new Design artifact to continue iterating.

## Status

Prototype — no real backend. File uploads, CSV exports, and chat-driven edits all run client-side; the AI drafting layer in Archimedes is a scripted stand-in for the real drafting engine.
