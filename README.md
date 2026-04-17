# Chapter 34: Teaching Architecture Without Teaching Syntax
### Pedagogical Frameworks for Agentic Systems
**Book:** Design of Agentic Systems with Case Studies
**Course:** INFO 7375 — Prompt Engineering for Generative AI

---

## Overview

This repository contains the complete deliverables for Chapter 34 of *Design of Agentic Systems with Case Studies*. The chapter argues that the primary failure mode in organizational AI education is teaching features rather than principles -- producing teams that can use today's framework but cannot evaluate tomorrow's.

The book's master claim is: architecture is the leverage point, not the model. This chapter is a specific instance of that claim applied to instructional design. A curriculum is an architecture. The feedback loop it runs, the assessment instruments it deploys, and the sequence in which it presents concepts are design decisions with predictable structural outcomes.

---

## Repository Contents

```
chapter34.pdf          -- Final chapter with all figures
chapter34_notebook.ipynb  -- Runnable Jupyter notebook demo
authors_note.pdf       -- 3-page pedagogical report
```

---

## The Chapter

**Chapter 34: Teaching Architecture Without Teaching Syntax**

The chapter is organized around the operator/evaluator distinction: a curriculum that validates learning through working demos produces teams that can build but cannot read an unfamiliar architecture. The chapter develops three structural decisions that close that gap:

1. Dissonance-first unit design -- every unit opens with a scenario the learner cannot resolve with their current model
2. Structured pair protocol -- the navigator asks what would break, not whether the code is correct
3. ICE as a justification instrument -- the score is not the deliverable, the causal justification is

The chapter opens with the 2018 Uber Tempe fatality as the anchor case and uses the Epic sepsis prediction model as the worked ICE example.

---

## The Notebook

The notebook demonstrates the chapter's central argument in running code. It has four parts:

**Part 1 -- The working demo**
A three-subagent customer service system routes a simple query correctly. The demo passes. This is the capstone moment.

**Part 2 -- The AI scaffold**
An AI scaffold generates ICE scores for a checkpoint placement decision. The AI proposes Impact 8. The justification is syntax-level -- it describes what the checkpoint intercepts, not where that interception sits in the causal chain.

**Part 3 -- The Human Decision Node**
A hard-stop cell that throws a RuntimeError if not filled in. The architectural decision node requires the user to evaluate the AI's proposed score before the notebook continues. The correct rejection: Impact 3, not 8, because the routing decision is already made upstream -- the checkpoint is downstream of the point of no return.

**Part 4 -- The deliberate failure case**
The same system receives a multi-domain query. The single-label classifier routes to one agent and silently drops the other two domains. No error is thrown. The failure is architectural, not syntactic.

**Part 5 -- The Try exercise**
The reader modifies the system to trigger a new failure mode and predicts what breaks before running it.

### Running the Notebook

1. Open in Google Colab or Jupyter
2. Replace `YOUR_OPENAI_API_KEY` with your OpenAI API key
3. Run cells in order
4. At the Human Decision Node cell -- fill in the dictionary before running Part 4. The notebook will not continue until all fields are completed.

### Requirements

```
openai
jupyter
```

---

## Learning Outcomes

After engaging with this chapter and notebook, a practitioner will be able to:

1. Distinguish architectural reading from architectural building and explain why building does not develop reading automatically (Bloom's level 2 -- Understand)
2. Identify loop compression in an existing training unit and name which structural decision is absent or degraded (Bloom's level 4 -- Analyze)
3. Apply the ICE framework as a justification instrument by constructing causal-chain justifications for architectural decisions (Bloom's level 3 -- Apply)
4. Evaluate a proposed agentic architecture against the causal chain tracing method introduced in the worked example (Bloom's level 5 -- Evaluate)
5. Design a dissonance-first instructional unit for one concept in an existing agentic systems curriculum (Bloom's level 6 -- Create)

---

## Figures

All figures were generated from Figure Architect prompts using Whimsical and are embedded in the chapter PDF.

| Figure | Title | Priority |
|--------|-------|----------|
| Hero | Architectural Reading vs. Pattern Execution | Mandatory |
| Figure 1 | The Three-Stage Operational Loop | Critical |
| Figure 2 | The Three Structural Decisions as an Interdependent System | Important |
| Figure 3 | The Compression Failure: Two Curriculum Paths | Critical |
| Figure 4 | The Capability Gap: Demonstrated vs. Actual | Supplementary |
| Figure 5 | The Compression Experiment: Research Design | Important |

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Bookie | Chapter prose generation and structural rewrite |
| Eddy the Editor | Pedagogical audit and Priority Fix protocol |
| Figure Architect | High-assertion zone detection and figure prompt generation |
| Courses | Bloom's Taxonomy learning outcomes and Show-and-Tell sequence |
| Eddy the Storyboarder | 14-scene CapCut video storyboard |

---

## Submission

- Chapter PDF: `chapter34.pdf`
- Notebook: `chapter34_notebook.ipynb`
- Author's Note: `authors_note.pdf`
- Video: https://youtu.be/zEo92gzPTiI
