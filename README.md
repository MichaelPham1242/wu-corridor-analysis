# Western Union corridor analysis

This repository contains a locally runnable Jupyter notebook for analyzing Western Union's directional remittance-corridor footprint, pricing, provider competition, and modeled bilateral flows.

The checked-in notebook has been executed end to end. It contains 44 cells, including 37 code cells, with saved outputs and no execution errors.

## Contents

- `WU_Corridor_Analysis_Local.ipynb` — executed analysis notebook
- `WU_Corridor_Analysis_Data.zip` — core corridor data loaded by the notebook
- `WU_Roadmap_Source_Pack.zip` — extended source pack loaded by the notebook
- `WU_Roadmap_Source_Pack_manifest.json` — source-pack contents and coverage
- `WU_Roadmap_Source_Pack_validation.json` — source-pack validation results
- `outputs/` — generated Excel workbooks and figures from the verified run

## Run locally

Python 3.12 was used for the verified run.

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python -m jupyter lab WU_Corridor_Analysis_Local.ipynb
```

Keep both ZIP files beside the notebook. The notebook extracts them into `local_runtime/` and writes regenerated artifacts to `local_outputs/`; both folders are ignored by Git.

## Verified outputs

- `WU_RPW_Footprint_Analysis.xlsx` — 8 worksheets
- `WU_RPW_Extended_Analysis.xlsx` — 21 worksheets
- Four publication-ready PNG figures in `outputs/wu_writeup_figures/`

The bilateral corridor values are modeled estimates. Western Union corridor shares are downstream analytical outputs and should not be read as company-disclosed corridor revenue.
