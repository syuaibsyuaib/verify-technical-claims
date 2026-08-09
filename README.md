# verify-technical-claims

[![GitHub Downloads](https://img.shields.io/github/downloads/syuaibsyuaib/verify-technical-claims/total?logo=github)](https://github.com/syuaibsyuaib/verify-technical-claims/releases)
[![PyPI Downloads](https://img.shields.io/pypi/dm/verify-technical-claims?logo=python)](https://pypi.org/project/verify-technical-claims/)

This repository contains a skill definition for pre-empirically verifying technical claims. The skill is designed to assess technical concepts, physics claims, or market assertions by prioritizing [...]

## Repository contents

- `SKILL.md` — main skill description, core principles, reasoning workflow, and response format.
- `agents/openai.yaml` — skill agent configuration for OpenAI platforms or similar integrations.
- `evals/evals.json` — evaluation scenarios for testing skill quality (if available).
- `references/` — supporting documents for methods, validation protocols, and formal notation guidance.

## Primary goals

1. Review technical claims using evidence from research papers, official standards, documentation, or credible market publications.
2. Formalize arguments with clear logic and model definitions.
3. Identify hidden assumptions, inference gaps, and limitations before making empirical decisions.
4. Provide answers in English with proportional truth status and recommended next actions.

## How to use

1. Read `SKILL.md` to understand the skill's principles, workflow, and answer format.
2. Use this skill when validating technical claims, evaluating concept designs, or reviewing initial analysis results.
3. Update `references/` when adding new methodologies or relevant sources.
4. Run evaluations with `evals/evals.json` to verify the skill's consistency when applicable.

## Contribution

- Add new test cases to `evals/evals.json` for additional scenarios.
- Update `references/` with new protocols, frameworks, or guidance.
- Revise `SKILL.md` if the verification process or response style needs adjustment.

## Notes

This repository is a validation skill or framework, not an application codebase. The focus is on documenting reasoning, logic, and references for systematic claim assessment.
