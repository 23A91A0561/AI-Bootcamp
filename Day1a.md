# AI Playground Lab Report: Comparative Analysis of 4 Free-Tier LLMs

**Lab:** Day 1, Lab 1A – AI Playground (Turnkey Walkthrough)  
**Name:** Tadepalli Jashwanth Sagar  
**Date:** 09 June 2026
**Tasks:** Summarisation, Code Generation, Logical Reasoning  
**Tools evaluated:** ChatGPT (free), Claude (free), Gemini (free), Perplexity (free)  

---

## Executive Summary

This report compares four leading AI assistants across three real-world tasks relevant to placement training. The key finding is **no single tool dominates all tasks**. ChatGPT offers the best balance for general use, Claude excels at nuanced reasoning and thorough writing, Perplexity is the strongest for fact‑verification but weak at pure reasoning, and Gemini is useful for quick factual queries but fails on strict code constraints.

---

## Task 1 – Summarisation (Article on AI in placement training)

**Objective:** Generate 5 bullet points, ≤15 words each, preserving key claims without fabrication.

### Output Quality Analysis

| Tool        | Strengths                                                                 | Weaknesses                                                              | Score |
|-------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|-------|
| **ChatGPT** | Clean, conversational bullets; balanced coverage.                         | Missed the AICTE 18% statistic (minor omission).                        | 4/5   |
| **Claude**  | Most thorough; preserved nuance (e.g., “60% error reduction”); stayed ≤15 words. | Slightly more verbose than needed.                                     | 5/5   |
| **Gemini**  | Included the 18% statistic that others missed; strong on numeric facts.   | Style too curt; one bullet awkwardly phrased.                          | 4/5   |
| **Perplexity** | Excellent citations (inline source links).                               | Bullet phrasing slightly cluttered; added external source references.   | 4/5   |

**Key insight:** Claude is the best for preserving detail and nuance. Perplexity is best when you need verifiable sources.

---

## Task 2 – Code Generation (Python resume‑scoring function)

**Constraint:** Use only standard library. Return `dict` with `score`, `reasoning`, `missing_skills`.

### Code Correctness & Constraint Adherence

| Tool        | Result                                                                                     | Score |
|-------------|--------------------------------------------------------------------------------------------|-------|
| **ChatGPT** | ✅ Works, standard library only (`re`, `collections`). Clean docstring and example.         | 5/5   |
| **Claude**  | ✅ Works, but slightly over‑engineered (extra edge cases). Still meets all constraints.    | 4/5   |
| **Gemini**  | ❌ Failed – imported `sklearn` (external library). Code would not run without installation. | 1/5   |
| **Perplexity** | ⚠️ Basic but works; missing docstring in the returned code snippet (incomplete).          | 3/5   |

**Key insight:** Gemini is unreliable for coding tasks with strict library constraints. ChatGPT produced the most idiomatic, constraint‑compliant solution. Claude gave the most thorough explanation.

---

## Task 3 – Logical Reasoning (Time‑based puzzle)

**Puzzle:** Three students leaving at 7:00, +30 min, +15 min; third has 25 min walk; class at 8:30. On time?

### Reasoning Transparency & Correctness

| Tool        | Answer | Steps Shown                                                                 | Confidence Calibration | Score |
|-------------|--------|-----------------------------------------------------------------------------|------------------------|-------|
| **ChatGPT** | ✅ 8:10, on time | All steps explicit (7:00 → 7:30 → 7:45 → 8:10 → compare to 8:30)            | Appropriate             | 5/5   |
| **Claude**  | ✅ 8:10, on time | Most thorough (even states “no hidden tricks”)                              | Appropriate             | 5/5   |
| **Gemini**  | ✅ 8:10, on time | Skipped intermediate steps (gave only final calculation)                    | Appropriate             | 3/5   |
| **Perplexity** | ✅ 8:10, on time | Treated as a search task; cited external source rather than original reasoning | Over‑reliance on search | 2/5   |

**Key insight:** ChatGPT and Claude are strongest for transparent step‑by‑step reasoning. Perplexity (built for search) is weakest at original logical deduction.

---

## Overall Comparison Matrix

| Tool       | Task 1 (Summarise) | Task 2 (Code) | Task 3 (Reason) | **Composite Score** | **Best Use Case**                                   |
|------------|--------------------|---------------|-----------------|---------------------|------------------------------------------------------|
| ChatGPT    | 4                  | 5             | 5               | 14/15               | All‑purpose, fast, well‑structured responses        |
| Claude     | 5                  | 4             | 5               | 14/15               | Long documents, careful reasoning, high‑stakes writing |
| Gemini     | 4                  | 1             | 3               | 8/15                | Quick factual queries (if code not needed)          |
| Perplexity | 4                  | 3             | 2               | 9/15                | Fact‑checking, cited answers (not reasoning)        |

---

## Recommendations for Placement Mentors

1. **Use ChatGPT as your default** – It handles summarisation, code, and reasoning reliably with a clean interface.

2. **Switch to Claude when** – You need to analyse long articles, preserve subtle claims, or produce careful, well‑reasoned outputs (e.g., writing feedback for students).

3. **Use Perplexity exclusively for fact verification** – Ask it to cite sources. Do not rely on it for multi‑step reasoning or code with constraints.

4. **Be cautious with Gemini** – It is fine for simple Q&A but failed the code constraint and skipped reasoning steps. Not recommended for placement‑critical tasks.

5. **Teach the “verification chain”** – As the article suggests: AI → second source (Perplexity with citations) → open primary URL. This is the only reliable way to avoid hallucinations.

---

## Key Takeaways for Training

- **No tool is perfect.** Every mentor should fill a comparison matrix themselves – the disagreement is the learning moment.
- **Free tier matters.** Students will use free accounts. Paid models skew comparisons.
- **Reasoning is a distinct skill.** Perplexity’s failure on the logic puzzle shows that search‑augmented LLMs are not good at pure deduction.
- **Code constraints expose weaknesses.** Gemini’s violation of the “standard library only” rule is a powerful teaching example.

---

## Acceptance Check (as per lab)

- ✅ Matrix with 12 cells filled (see above)  
- ✅ 3‑sentence conclusion written below  
- ✅ This report pushed to public GitHub repo

### 3‑Sentence Conclusion

> **I would use ChatGPT** for general tasks where I need a fast, well‑structured response.  
> **I would use Claude** for long documents, careful reasoning, and high‑stakes writing.  
> **I would use Perplexity** for any factual claim I cannot afford to get wrong.

---
