# Ex-Ante Evaluation of AI-Induced Diversity Collapse

This repository contains the code and analysis materials for studying whether large language models induce population-level convergence in creative outputs before deployment in human-facing settings. The project evaluates creative diversity using matched human and AI-generated responses across multiple creative tasks, with a focus on measuring whether AI systems generate outputs that are individually plausible but collectively redundant.

The core premise is that generative AI systems are often evaluated at the level of a single user or output, whereas many creative domains are population-level environments. In these settings, the value of a slogan, story, or idea depends not only on its quality, but also on how many other agents produce similar outputs. A model that performs well for individual users may still produce a diversity collapse if repeated independent use causes many outputs to cluster in the same regions of idea space.

## Repository contents

This repository includes notebooks and supporting utilities for:

- preprocessing human creative-response datasets;
- generating or loading AI self-play outputs;
- embedding human and AI outputs into a shared semantic space;
- estimating semantic similarity, clustering, and diversity metrics;
- comparing AI-generated output distributions against matched human baselines;
- producing tables and figures for the manuscript.

## Tasks and data structure

The analyses are organized around creative tasks in which multiple responses are generated for the same prompt or stimulus. Depending on the task, a response may be a story, slogan, or short divergent-thinking answer. The workflow treats each prompt as a local population of outputs and compares the distribution of AI-generated responses against the corresponding distribution of human responses.

Human and AI responses are analyzed using the same representation and evaluation pipeline to support direct comparison. The main quantities of interest are population-level diversity, redundancy, and convergence rather than only average output quality.

## Reproducibility

The notebooks are intended to be run in sequence following the numbering in the filenames. Supporting helper functions are contained in `utils.py`. Generated outputs, intermediate files, and figures may be written to local output folders depending on the notebook.

A typical workflow is:

1. Prepare or load the human-response data.
2. Prepare or load AI-generated responses for the same prompts.
3. Compute text embeddings.
4. Calculate similarity, clustering, and diversity metrics.
5. Generate summary statistics and manuscript figures.

## Anonymity note

This repository has been prepared for anonymous peer review. Author-identifying information has been removed from the code, documentation, and repository metadata where possible.
