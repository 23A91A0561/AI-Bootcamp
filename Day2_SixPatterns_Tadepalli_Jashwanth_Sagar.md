# Day 2 — Six Prompt Patterns Lab

**Name:** Tadepalli Jashwanth Sagar  
**Date:** 11 June 2026

## Student Question

> Explain Big-O notation for a placement interview.

---

# Pattern 1 — PERSONA

## Prompt

You are a senior placement coach at Aditya University. You have prepared 200 B.Tech CSE students for TCS, Infosys, and Cognizant placement interviews. A 3rd-year CSE student with 7.5 CGPA asks you about Big-O notation. Explain it the way you would in a 1-on-1 prep session — concrete, conversational, exam-relevant.

## Output

Big-O notation is a way to describe how the running time or memory usage of an algorithm grows as the input size increases. In placement interviews, you can think of it as a "performance rating" for your code.

For example, if you search for a number in an array by checking each element one by one, the time grows linearly with the number of elements, so the complexity is O(n). If you use two nested loops to compare every pair of elements, the complexity becomes O(n²).

Interviewers ask Big-O questions because they want to know whether you can write efficient code, not just code that works. A common interview answer would be: "Linear search has O(n) time complexity because, in the worst case, it checks every element once."

## Self Score (1–5)

**5/5**

## Peer Score (/10)

**9/10**

---

# Pattern 2 — FEW-SHOT

## Prompt

Here are example explanations from a placement coach:

Q: What is recursion?  
A: A function calling itself with a smaller problem. Like Russian dolls — open one, find a smaller one inside. Stops at base case. Example: factorial.

Q: What is a stack?  
A: LIFO data structure. Push to add, pop to remove. Like a stack of plates — you take from the top.

Q: What is Big-O notation?  
A:

## Output

Big-O notation tells us how an algorithm's running time grows as the input size increases. Think of it like measuring how quickly a queue gets longer as more people join it. For example, linear search is O(n) because it may check every item once, while a nested-loop comparison is O(n²) because the work grows much faster as the input size increases.

## Self Score (1–5)

**4/5**

## Peer Score (/10)

**8/10**

---

# Pattern 3 — CHAIN-OF-THOUGHT

## Prompt

Explain Big-O notation to a placement interview candidate.

Step 1: Define Big-O in one sentence.

Step 2: Give one concrete example with code.

Step 3: Explain why interviewers ask about it.

Step 4: Synthesise into a 3-sentence summary.

## Output

### Step 1: Definition

Big-O notation describes how the running time or memory usage of an algorithm grows as the input size increases.

### Step 2: Example

```python
def find_max(arr):
    max_val = arr[0]
    for num in arr:
        if num > max_val:
            max_val = num
    return max_val
```

This algorithm scans the array once, so its time complexity is O(n).

### Step 3: Why Interviewers Ask

Interviewers use Big-O questions to evaluate whether candidates can analyze efficiency and choose scalable solutions.

### Step 4: Summary

Big-O notation measures algorithm efficiency as input size grows. An algorithm that scans a list once is typically O(n). Understanding Big-O helps you compare solutions and write code that performs well on large datasets.

## Self Score (1–5)

**5/5**

## Peer Score (/10)

**10/10**

---

# Pattern 4 — STRUCTURED OUTPUT

## Prompt

Explain Big-O notation for a placement interview.

Return ONLY valid JSON with this exact shape:

{
  "definition": "one-sentence definition",
  "intuition": "concrete analogy",
  "code_example": "Python snippet showing O(n) and O(n²)",
  "common_pitfall": "what students get wrong",
  "interview_test_question": "a follow-up question an interviewer might ask"
}

## Output

```json
{
  "definition": "Big-O notation describes how an algorithm's running time or memory usage grows as input size increases.",
  "intuition": "Imagine organizing books: checking each book once is O(n), while comparing every book with every other book is O(n²).",
  "code_example": "O(n): for x in arr: print(x) | O(n²): for x in arr: for y in arr: print(x,y)",
  "common_pitfall": "Students often count exact operations instead of focusing on growth rate and dominant terms.",
  "interview_test_question": "What is the time complexity of binary search and why?"
}
```

## Self Score (1–5)

**5/5**

## Peer Score (/10)

**10/10**

---

# Pattern 5 — SYSTEM PROMPT

## System Prompt (Custom Instructions)

You are a senior placement coach for B.Tech CSE students at an Indian engineering college. You prepare students for TCS / Infosys / Cognizant interviews. You explain technical concepts in 50–80 words max, conversationally, with one concrete code example.

## User Prompt

Explain Big-O notation.

## Output

Big-O notation tells you how an algorithm's performance changes as input size grows.

```python
for item in arr:
    print(item)
```

The loop runs once per element, so it's O(n). Interviewers ask Big-O questions to check whether you understand efficient coding and can compare different solutions to the same problem.

## Self Score (1–5)

**4/5**

## Peer Score (/10)

**8/10**

---

# Pattern 6 — PROMPT CHAINING

## Conversation 1 (Extract)

### Prompt

List the 5 most important sub-concepts a B.Tech student must understand about Big-O notation. Just the list, no explanation.

### Output

1. Definition of Big-O
2. Common Time Complexities
3. Comparing Algorithms
4. Time vs Space Complexity
5. Interview Relevance

---

## Conversation 2 (Expand)

### Prompt

For each of these 5 sub-concepts of Big-O notation, write a 1-paragraph explanation tailored to a 3rd-year B.Tech CSE student preparing for placement interviews.

### Output

**Definition of Big-O:** Big-O notation measures how an algorithm's running time or memory usage grows as the input size increases.

**Common Time Complexities:** Common complexities include O(1), O(log n), O(n), O(n log n), and O(n²). Understanding them helps compare efficiency.

**Comparing Algorithms:** Comparing algorithms using Big-O allows developers to select solutions that scale better.

**Time vs Space Complexity:** Time complexity measures execution time growth, while space complexity measures memory growth.

**Interview Relevance:** Interviewers use Big-O questions to assess problem-solving skills and understanding of efficient code design.

---

## Conversation 3 (Polish)

### Prompt

Synthesise these 5 paragraphs into ONE concise 80-word interview-prep explanation of Big-O notation. Preserve all 5 sub-concepts. Conversational tone. End with one practice question.

### Output

Big-O notation describes how an algorithm's performance changes as input size grows. Common complexities include O(1), O(log n), O(n), and O(n²). It helps compare different solutions and choose the most efficient one. Besides time complexity, interviewers may also ask about space complexity, which measures memory usage. Understanding both helps you design scalable programs and perform well in technical interviews.

**Practice Question:** What is the time complexity of binary search?

## Self Score (1–5)

**5/5**

## Peer Score (/10)

**10/10**

---

# Peer Review Rubric

| Criterion | Score (0–2) | Notes |
|------------|------------|--------|
| Clarity | 2 | Single objective per prompt |
| Context | 2 | Audience specified |
| Specificity | 2 | Big-O and placement interview focus |
| Format | 2 | Output structure defined |
| Verification | 1 | Limited validation steps |

**Total:** **9/10**

---

# Reflection

For my placement-prep students, the patterns I will use most are **Persona** and **Prompt Chaining**.

Persona prompts help tailor explanations to a student's background, skill level, and interview goals, making concepts easier to understand. Prompt Chaining is useful because it breaks a complex topic into smaller steps, allowing the AI to first identify key ideas, then expand them, and finally produce a concise, high-quality explanation. Together, these patterns improve both relevance and clarity for placement preparation.

---

# Submission Checklist

- [x] Pattern 1 — Persona
- [x] Pattern 2 — Few-Shot
- [x] Pattern 3 — Chain-of-Thought
- [x] Pattern 4 — Structured Output
- [x] Pattern 5 — System Prompt
- [x] Pattern 6 — Prompt Chaining
- [x] Self-score for each pattern
- [x] Peer-score for each pattern
- [x] Reflection paragraph completed
- [x] Ready to push to Day2_SixPatterns.md
