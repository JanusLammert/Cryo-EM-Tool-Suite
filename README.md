# Cryo-EM Tool Suite

A collection of lightweight, browser-based and command-line tools that bridge automated cryo-EM reconstruction pipelines and expert-guided structure determination — supporting 2D class curation, helical mask design, cross-sectional hypothesis generation, metadata exploration, particle measurement, and workflow provenance tracking. All tools are compatible with RELION output formats.

This repository serves as a central index for the suite. Each tool lives in its own repository with its own README, license, and version history; links below point to the individual projects.

## Tools

| Tool | Category | Description | Repository |
|---|---|---|---|
| **CLASS·SELECT** | Interactive Analysis | Browser-based 2D class average browser and particle exporter for RELION. Assigns classes to up to eight named, colour-coded groups across multiple classification rounds, with optional pairwise similarity matrix loading and STAR file export filtered by group. | [Select2DClasses](https://github.com/JanusLammert/Select2DClasses) |
| **HelixMask** | Interactive Analysis | Browser-based helical mask design tool. Draws a 2D cross-section mask with brush, eraser, polygon, and flood-fill tools, auto-generates an initial mask via density thresholding and connected-component analysis, and extends it into a full 3D helical mask with a cosine soft edge. | [HelixMasker](https://github.com/JanusLammert/HelixMasker) |
| **2D Class Stitcher** | Interactive Analysis | Turns RELION/cryoSPARC 2D class averages into an interactive sinogram solver, automatically solving cyclic order and mirror orientation of multi-selected classes and reconstructing an initial 3D helical volume via SART. | [Manual_Stitcher](https://github.com/JanusLammert/Manual_Stitcher) |
| **RELION StarVis** | Data Exploration | Browser-based interactive metadata visualizer for RELION STAR files, with histogram, scatter plot, multi-histogram, and statistics table views, draggable threshold lines, and freehand lasso selection for subpopulation export. | [StarVis](https://github.com/JanusLammert/StarVis) |
| **EMsight** | Data Exploration | Browser-based tool for direct measurement of particle dimensions on micrograph images (MRC/MRCS/TIFF), with population statistics, robust estimators, and KDE distributions per named polymorph group. | [EMSight](https://github.com/JanusLammert/EMSight) |
| **rel2obsi & canvas_generator** | Workflow Documentation | Python tools that parse the RELION pipeline DAG and job metadata to generate a structured Obsidian knowledge vault (one Markdown note per job, with embedded class montages and parameter tables) and a visual Canvas file rendering the full pipeline as an interactive node graph. | [relion2obsidian](https://github.com/JanusLammert/relion2obsidian) |

## Getting started

Five of the seven tools are self-contained HTML5/JavaScript applications that require no installation and run in any modern web browser — open the relevant tool's repository and follow its README for the specific file to launch. The remaining two (`rel2obsi` and `canvas_generator`, both in `relion2obsidian`) are Python command-line scripts requiring Python ≥3.8; see that repository's README for installation via pip.

## License

All tools are released under the GNU General Public License v3.0 (GPLv3). See the individual repositories for full license text.
