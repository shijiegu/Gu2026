# gucompaper: Naturalistic behavior and self-generated neural activity predictive of self-correction

Analysis code accompanying the Gu et al. change-of-mind paper.

The code was previously developed inside the [Spyglass](https://github.com/LorenFrankLab/spyglass)
framework under `spyglass.shijiegu` and has been extracted into a standalone, installable package.

**DOI** 10.5281/zenodo.20371883

## Install

From the repository root:

```bash
pip install -e .
```

This installs the `gucompaper` package in editable mode along with its runtime
dependencies. The code still relies on `spyglass-neuro` and DataJoint tables
defined in Spyglass, so a working Spyglass environment (database, NWB files) is
expected at runtime.

## Layout

```
src/gucompaper/
    Analysis_SGU.py
    behavior.py
    changeOfMind*.py
    changeOfMind_figures/   # figure-generation scripts
    ...
```

Internal imports use the `gucompaper` namespace, e.g.:

```python
from gucompaper.Analysis_SGU import TrialChoice
from gucompaper.changeOfMind_figures.figure4d import load_theta_df
```
