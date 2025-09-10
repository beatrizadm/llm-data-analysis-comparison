# Prompts used


## Summary
1. [Initial Prompt for Base Preparation](#1-initial-prompt-for-base-preparation)
1. [Prompt for Question Assessment](#2-prompt-for-question-assessment)


## 1. Initial Prompt for Base Preparation

Analyze the provided dataset to identify its key characteristics for data-driven decision-making. Upon receiving a specific analytical question, address it strictly using the dataset. Your deliverables must include a clear, concise answer to the question and the Python code that extracts and processes the data used to derive your answer.

[Question]

If the question is not objectively answered in the first attempt, iterate up to a maximum of 3 times until a solution is found or the limit is reached.
* Follow the best approach to solve this problem based on the dataset.



## 2. Prompt for Question Assessment

### Main prompt

Role: You are an expert in evaluating structured question sets for LLM testing, focusing on data science, experimental design, LLMs, and NLP. Your task is to analyze a predefined set of 36 questions organized into 4 analysis types (descriptive, diagnostic, predictive, prescriptive) and 3 difficulty levels (basic, moderate, challenging). Use the provided context to validate question relevance, alignment, and scientific rigor.


### Context

1. **Research Objectives:** Evaluate LLMs’ ability to perform robust data analysis and answer domain-specific questions based on structured or unstructured datasets (e.g., ‘Analyze sales trends from a retail dataset and explain factors driving regional revenue disparities’)
1. **Dataset:**
    
* Changes according to the Dataset:
    * Dataset 1 - Academic Records from UFCG: A university in Brazil maintains an educational database to monitor student development indices, general information, and graduation methods. This database tracks academic performance, enrollment details, and whether students graduate through coursework, research, or other pathways.

    * Dataset 2 - Sicor: A dataset of rural credit contracts issued under Brazil’s SICOR program during the first half of 2024, covering all 27 Brazilian states. It records contractual and financial information about agricultural credit operations, enabling analysis of financing patterns, regional distribution, and economic support for producers.

    * Dataset 3 - HIV: A public UNICEF dataset containing key HIV epidemiology indicators for children and adolescents (ages 0–19), spanning 2000–2023 with global coverage. It compiles sex- and region-disaggregated estimates to track prevalence, trends, and progress in prevention and treatment among young populations.


### Instructions for Analysis

1. **Evaluate Question Structure:**
* Verify alignment of each question with its analysis type:
    * Descriptive: Factual recall/summarization (e.g., "Define TF-IDF and list its use cases").
    * Diagnostic: Identifies causes/anomalies (e.g., "Why does a model overfit on imbalanced data?").
    * Predictive: Forecasts outcomes (e.g., "Predict churn risk using customer embeddings").
    * Prescriptive: Recommends actions (e.g., "Design a pipeline to reduce false positives in cancer screening").
* Assess difficulty levels:
    * Basic: Straightforward, requiring foundational knowledge.
    * Moderate: Requires synthesis of multiple concepts.
    * Challenging: Demands critical thinking, creativity, or specific knowledge on the subjects.

2. **Criteria for Evaluation:**
* Clarity: Is the question unambiguous?
* Intent Alignment: Does it match its analysis type and difficulty?
* Diversity: Covers edge cases, and scenarios relevant to the category.
* Bias: Neutral phrasing, free from leading language.
* Grounding: Rooted in theory or practical use cases.

3. **Identify Gaps:**
* Type mismatches (e.g., a "predictive" question that is actually descriptive).
* Highlight difficulty inconsistencies (e.g., a "challenging" question that is too simplistic).
* Note redundancy (e.g., overlap between questions).

4. **Propose Revisions:**
* For flawed questions, suggest 2 revised versions that fix issues while preserving intent.
* Ensure revised questions adhere to the original analysis type and difficulty.


### Output Format

**Analysis by Category & Difficulty**

* Descriptive Analysis
    * Basic:
        * Question 1:
            * Issue: 
                * [If applicable] "Fails to meet: [Criterion] (e.g., Clarity due to ambiguous terminology; Diversity due to NLP-only focus)."
                * [If no issues] "All criteria satisfied."
            * Suggestion: [e.g., "Rephrase to focus on defining terms like 'TF-IDF'."]
        * Revised Question 1A: [New text]
        * Revised Question 1B: [New text]
    * Moderate: [Repeat structure]
    * Challenging: [Repeat structure]

* [... Repeat for Diagnostic, Predictive and Prescriptive]


**Gap Summary**

* Difficulty Imbalance: [e.g., "Challenging tier lacks ambiguity handling."]
* Redundancies: [e.g., "Overlap between predictive Q3 and diagnostic Q2."]

**Recommendations**
* Add 2–3 questions on [specific gap, e.g., "ethical implications"].
* Rebalance difficulty in [category] by [action, e.g., "simplify phrasing"].
* Validate with [specific benchmark, e.g., "HumanEval for code-based questions"].

**Focus:** Prioritize structural coherence, category/difficulty alignment, and scientific robustness. Ensure all 36 questions are critiqued, revised, and mapped to their intended purpose. Highlight how revisions improve the state of the art in LLM evaluation.













