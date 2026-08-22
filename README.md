# Feature Graph prototype

An experimental PyTorch package for deriving Boolean features from numeric
signals and composing those features through named operators.

## Install

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install -e .
```

The reusable package lives in `src/feature_graph`. `example.py` and
`cp_example.py` are dataset-specific research scripts: they require local CSV
files whose paths are configured in the corresponding constants modules.
They are retained as provenance, not presented as zero-configuration demos.

## Core API

- `get_base_features` computes high/low masks relative to a baseline.
- `get_feature_graph` applies named operators to those masks.
- `get_features_from_state` converts a CartPole state into model features.

This project remains standalone because it is software, not a notebook-only
learning collection.
