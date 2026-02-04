# Chain-of-Thought Prompting for Question Answering

## Overview

This project explores how **Chain-of-Thought (CoT) prompting** impacts performance in large language model (LLM)-based question answering systems. We compare direct prompting against CoT-style prompting and evaluate model outputs using both **traditional QA metrics** and **LLM-based evaluation frameworks**.

The focus is on:
- Reasoning quality and correctness
- Prompting trade-offs (accuracy vs verbosity vs cost)
- Systematic evaluation of LLM outputs

---

## Pipeline Summary

1. Input question is passed to an LLM
2. Prompting strategy is applied:
   - Direct Answer Prompting
   - Chain-of-Thought Prompting
3. Model generates an answer (with or without explicit reasoning)
4. Outputs are evaluated using multiple evaluation strategies

---

## Prompting Strategies

### Direct Prompting
- Produces concise final answers
- Lower latency and token usage
- Limited visibility into reasoning steps

### Chain-of-Thought Prompting
- Explicit intermediate reasoning generation
- Improved performance on multi-step and riddle-style questions
- Increased interpretability at the cost of higher token usage

---

## Evaluation Methods

To assess answer quality beyond surface-level accuracy, we employ both
**rule-based** and **LLM-assisted evaluation methods**:

### Traditional QA Evaluation
- Exact match / correctness checks
- Comparative accuracy between prompting strategies
- Error analysis across reasoning-heavy questions

### RAGAS-Inspired Metrics
- Faithfulness of reasoning to the question
- Answer relevance and consistency
- Structured evaluation of reasoning quality

### G-Eval (LLM-as-a-Judge)
- Uses an LLM to score answers based on:
  - Correctness
  - Logical coherence
  - Completeness
- Enables flexible, scalable evaluation when ground-truth labels are limited

These evaluation techniques allow for a more nuanced comparison between
prompting strategies, particularly for reasoning-intensive tasks where
traditional metrics may fall short.
