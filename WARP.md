# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Repository Overview

This is a learning repository for the Springboard Data Science Bootcamp (January 2023 cohort). It contains assignments, case studies, notes, and capstone project work organized by course units and modules.

The repository is primarily used for:
- Completing tiered assignments (Tier 1-3) in Jupyter notebooks
- Working on data science case studies
- Storing course notes and learning materials
- Tracking bootcamp progress through versioned releases

## Repository Structure

The repository follows a structured organization:

- **Assignments/**: Contains tiered assignments (Tier 1, 2, 3) for each unit
  - Each assignment typically has 3 difficulty tiers in separate notebooks
  - Tier 1 has more code filled in; Tier 3 is most challenging
  - Currently includes: London Housing analysis (Unit 4) and Monalco Mining case study

- **Capstone Projects/**: Dedicated space for major capstone project work (currently empty)

- **Notes/Springboard notes/**: Organized learning notes by unit
  - Uses Obsidian for note-taking and linking
  - Contains units 4, 5, and 6 currently
  - Markdown-based with Obsidian-specific features

- **Resources/**: Additional datasets, reference materials, and cheat sheets (currently empty)

- **Documentation/**: Course-related documentation and guidelines (currently empty)

## Working with Notebooks

### Jupyter Notebooks
All assignments are Jupyter notebooks (`.ipynb` files). When working with them:

- Notebooks follow a standard data science pipeline:
  1. Sourcing and loading data
  2. Cleaning, transforming, and visualizing
  3. Modeling
  4. Evaluating and concluding

- Required libraries for most assignments:
  - pandas (data manipulation)
  - numpy (numerical operations)
  - matplotlib.pyplot (visualization)

- Notebooks may load data from external URLs (e.g., London Datastore)

- Each notebook has structured markdown sections explaining objectives, hints, and expected DataCamp course prerequisites

### Running Notebooks
To work with notebooks in this repository:
```bash
jupyter notebook
```
Or use JupyterLab:
```bash
jupyter lab
```

## Git Workflow

### Branches
- `main`: Primary development branch
- `release`: Production branch for versioned releases
- Currently on `release` branch with version 1.6.0

### Version Control
- Versions are tracked using git tags (e.g., `1.6.0`)
- Version number stored in `version.txt` at repository root
- Super-linter GitHub Action runs on pushes to `main` branch

## CI/CD

### GitHub Actions
A Super-Linter workflow (`.github/workflows/superlinter.yml`) runs on the `main` branch:
- Validates code quality and formatting
- Errors are disabled (`DISABLE_ERRORS: true`)
- Notes directory is excluded from linting (`FILTER_REGEX_EXCLUDE: 'Notes/.*'`)

To validate locally before pushing:
```bash
# No specific local linting setup; relies on GitHub Actions
```

## Assignment Guidelines

When working on assignments:

1. **Tiered Approach**: Start with Tier 3 (highest difficulty), fall back to Tier 2 or Tier 1 if needed
2. **Learning Focus**: After completing Tier 1, revisit higher tiers to internalize skills
3. **Data Pipeline**: Follow the structured pipeline in each notebook
4. **Prerequisites**: Each assignment specifies which DataCamp courses provide the necessary background

## Notes System

The repository uses Obsidian for note-taking:
- Markdown files with bidirectional linking
- Organized by course units and sub-units
- See `Notes/Springboard notes/How to use Obsidian.md` for details

## Data Sources

Assignments may pull data from external sources:
- London Datastore (for housing price data)
- Course-provided datasets in PDF/Excel formats
- URLs embedded directly in notebooks

## Important Paths

- Assignment notebooks: `Assignments/<topic-name>/<tier>.ipynb`
- Course notes: `Notes/Springboard notes/Unit <X>/`
- Case study materials: `Assignments/case-study-<name>/`
