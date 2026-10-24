## 1. What this is
RouterBench is a public dataset of benchmark prompts together with answers
from 11 different LLMs, built for developing and testing LLM routers. For
every prompt it records each model's response, the estimated cost of that
response, and a score saying whether the answer was correct. This project
uses only the 0-shot version (prompts without worked examples), because
real users send plain questions.

## 2. Where it came from
- Published by: Martian (Hugging Face account: withmartian)
- Dataset page: https://huggingface.co/datasets/withmartian/routerbench
- DOI: 10.57967/hf/1996
- Paper: Hu et al., "RouterBench: A Benchmark for Multi-LLM Routing
  System", 2024, arXiv:2403.12031
- Code repository (separate from the data): https://github.com/withmartian/routerbench
- File used: routerbench_0shot.pkl
- Downloaded on: FILL IN (YYYY-MM-DD)
- File size: FILL IN
- SHA-256 fingerprint (optional): FILL IN

## 3. License and terms
- The Hugging Face dataset page states no license, and its Files tab has no LICENSE file.
- The GitHub code repository is MIT-licensed. I am not assuming that license also covers the data.
- Prompts come from public benchmarks (MMLU, GSM8K, MT-Bench, MBPP,
  HellaSwag, Winogrande and others), each with its own terms. Not
  audited individually.
- Responses were produced by 11 LLMs, some commercial; providers' terms
  may apply to those outputs.
- How this project handles it: educational, non-commercial research and
  portfolio use only; the raw file is not redistributed (excluded from
  Git, download instructions below); the paper is cited.
- Last checked: 24-10-2026. Paper checked for a data license but not realated to it found.

## 4. What one row means


## 5. Known limitations
- The models are older, so quality and prices are not today's. Use this
  data to study routing behaviour, not to predict current costs.
- Costs are estimates based on the dataset authors' API pricing.
- Prompts come from public benchmarks, not real user traffic, so a router
  that works here may behave differently on real queries.
- Models may have seen some benchmark questions during training
  (contamination).
- English only.
- Scores come from the dataset authors' pipeline and are not re-verified
  here.

## 6. How this project uses and changes the data
- The raw file stays untouched in data/raw/.
- Cleaned versions are written to data/processed/ (ignored by Git).
- Cleaning is done in notebooks so every step can be repeated.