---
name: verify-technical-claims
description: Verify technical claims and concepts by checking facts against research papers, standards, official documentation, reputable web sources, and market publications before deciding. Use when the user asks to verify whether a concept is true, validate a technical idea, prove or disprove a technical claim, compare a concept with scientific evidence, assess market-backed feasibility, derive or screen a candidate physics formula before simulation, or request formal-logic reasoning for a technical claim.
---

# Verify Technical Claims

## Purpose

Use this skill as a pre-empirical screening gate to check technical claims before costly simulation or implementation: gather evidence from trustworthy sources, convert the claim into premises and a conclusion, test the validity of the logic, then answer with a truth status proportional to the evidence.

## Core Principles

- Do not make a decision before checking the relevant facts and references.
- Prefer primary sources first: research papers, standards, official documentation, technical specifications, regulator reports, or official vendor data.
- For market claims, use credible market publications: analyst reports, company filings, industry reports, adoption data, benchmarks, or vendor publications with a bias note.
- Separate three things: the empirical truth of the premises, the validity of the inference, and the strength of the conclusion.
- Treat axioms as primitive postulates/assumptions within a formal system, not automatically as "absolute truth" in the empirical world.
- Determine the domain, predicates, relations, conditions, and semantic model before evaluating a claim that uses quantifiers or first-order structure.
- Do not describe a concept as "proven true" when the evidence only shows it is "supported," "plausible," or "not yet sufficiently evidenced."
- Use formal proof to screen a concept before experimentation: find contradictions, hidden assumptions, minimal requirements, and logical consequences that must hold true for the concept to succeed.
- Do not claim empirical performance, runtime efficiency, hardware stability, or market impact as proven from formal logic alone.
- For candidate physics formulas, always check dimensions/units, symmetry/invariance, conservation laws, limiting cases, and testable predictions before recommending simulation.
- Treat this skill as a system that must keep improving toward greater rigor; use `references/continuous-improvement.md` whenever there is a correction, gap, new example, or new methodological need.
- Do not let the skill be the sole judge of its own output; use `references/meta-validation-protocol.md` to test the skill's results against comparison cases, external sources, falsification, and cross-method checks.
- If web access is available and the claim depends on current information, perform a web search. Provide links to the sources used.
