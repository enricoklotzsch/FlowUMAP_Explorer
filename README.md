# FlowUMAP Explorer

Standalone release for multi-workspace FlowJo `.wsp` + `.fcs` UMAP analysis.

## Features

- Load one or multiple FlowJo workspace files.
- Map each workspace to its own FCS folder (supports same filenames across experiments).
- Build one integrated UMAP across experiments.
- Filter and facet by `Experiment`, condition, donor, timepoint, and workspace group.
- Cluster summary panel with top/high-low markers.

## Quick Start

```bash
python3 -m venv .venv311
source .venv311/bin/activate
python -m pip install -r flow_umap_analysis/requirements.txt
python -m streamlit run flow_umap_analysis/gui/umap_explorer.py
```

Or use launcher:

```bash
chmod +x launch_flowumap.command
./launch_flowumap.command
```

## Notes

- For multi-experiment projects where FCS filenames are reused, use:
  - `Workspace-to-FCS mapping` -> `Manual map each workspace`
- If using NumPy 2.x, the app includes a runtime compatibility patch for `fcsparser`.
