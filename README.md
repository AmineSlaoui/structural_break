# Structural Break

Structural break detection for the CrunchDAO competition.

## Layout

```
structural_break/
├── environment.yml   conda env definition (defaults channel)
├── .gitignore
├── data/             competition data — gitignored
└── notebooks/        exploration
```

## Setup

One time:

```bash
conda env create -f environment.yml
conda activate structural_break
python -m ipykernel install --user --name structural_break \
    --display-name "Python (structural_break)"
```

Every session after that:

```bash
conda activate structural_break
jupyter lab
```

Select the **Python (structural_break)** kernel. If you use an editor, point its
interpreter at `~/miniconda3/envs/structural_break/bin/python`.

## Managing dependencies

Everything lives in `environment.yml`. Add the package there — under the `pip:`
block only if it isn't on the conda `defaults` channel — then apply the change:

```bash
conda env update -f environment.yml --prune
```

## Competition data

```bash
crunch setup structural-break <your-token>
```
