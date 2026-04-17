# syn_DataGen

Deterministic planning template for synthetic tabular data generation.

## Contents

- `synthetic_pipeline_plan_template.json`: A structured execution plan template that maps schema/profile analysis to:
  - data understanding,
  - model selection (Copula/CTGAN/Diffusion rules),
  - preprocessing,
  - training,
  - generation,
  - evaluation,
  - model reusability.

## Usage

1. Parse your dataset schema and statistical profile.
2. Resolve all `PENDING_INPUT` fields.
3. Execute steps in order and persist artifacts listed in `reusability.artifacts`.

## Notes

- Identifier-like columns should be excluded from model training.
- Generation must preserve statistical and dependency fidelity.
- Evaluate synthetic utility against real-data baselines before deployment.
