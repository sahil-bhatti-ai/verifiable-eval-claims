# Verifiable Evaluation Claims (work in progress)

Status: started October 2026. Not finished.

## Idea
A model can have perfect file hashes and still have a wrong test score.
This project shows that with a small PyTorch model.

## Plan
- Data: UCI Adult (public).
- Model: small PyTorch MLP, plus a scikit-learn baseline.
- Four flaws to recreate on purpose:
  1. Leaky train/test split
  2. Shortcut feature
  3. Different test sets for different models
  4. Single seed
- For each run, save a manifest.json (data hash, seeds, split hashes).
- A checker script, verify.py, tests if a reported claim is valid.

## Done so far
- Project set up with uv.

## Not done yet
- Everything else. No results yet.