# TeSiP Severity Benchmark
Regulation-aligned benchmark dataset for railway hazard severity classification derived from the TeSiP/SIRF functional safety catalog, with structured hazard-severity pairs and reproducible evaluation support.

## Overview

This dataset is derived from the Technical Safety Plan (TeSiP) and SIRF guideline used in railway approval processes under the CENELEC EN 50126/50128/50129 framework.

It provides structured hazard–severity pairs with expert-defined consequence labels, enabling evaluation of machine learning and large language models (LLMs) for safety-critical classification tasks.

## Task Definition

The task is a **multi-class classification problem**:

- **Input**: textual hazard description (`hazard_is_given_if`)
- **Output**: severity class (`damage_injury_level_text`)

### Label Set

- `LV` — Slight Injuries  
- `SV` — Serious Injuries  
- `Deaths` — Fatal injuries  

## Dataset Characteristics

- Source: TeSiP / SIRF (German railway safety guideline)
- Type: regulator-aligned expert dataset (not synthetic)
- Structure: JSON
- Instances: 101 hazard–severity pairs
- Domain: railway functional safety

## Example Instance

```json
{
  "function": "carry / receive cargo",
  "hazard_is_given_if": "securing of load fails",
  "relevant_part_hazard": "Inadequately secured cargo",
  "damage_injury_level_text": "Deaths"
}
```
## Notes
Labels represent normative severity categories, not empirical outcomes.
Dataset excludes non-injury class (SV0).

## Usage

This dataset can be used for:

LLM evaluation under deterministic prompting
Safety-critical classification benchmarking
Analysis of class imbalance and error patterns
Research on AI-assisted risk assessment

## License

MIT License

## Citation

If you use this dataset, please cite: TBD after publication

## Contact

Padma Iyenghar
innotec GmbH – TÜV Austria Group
