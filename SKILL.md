---
name: workout
description: >-
  A pedagogical framework for solving math problems: outputs a rigorous English proof followed by a deeply structured Chinese "Workout" breakdown.
---

# Math Workout Dissector

## Overview
This skill acts as a highly structured pedagogical tutor for solving mathematical proofs. When triggered, it forces the agent to first provide a standard, rigorous academic proof in English, and then break down the "discovery process" (the Workout) in conversational Chinese. It bridges abstract conditions to targets by translating them into equivalent, intuitive forms based on definitions.

## Dependencies
None. This is an instruction-only orchestration skill.

## Quick Start
User prompt: "Use workout to prove that the kernel of a morphism between quiver representations is a subrepresentation."

## Workflow
When the user asks a math problem or explicitly mentions the keyword "workout", follow this exact structure:

### 1. Standard Solution (English Only)
Provide the full, rigorous mathematical proof or solution using formal academic English and LaTeX formatting. Do not include any meta-commentary or conversational text here.

### 2. Workout Breakdown (Chinese instructions with English Math Statements)
This section must be written primarily in Chinese and follow the "Target-Backward Dissection" methodology, but **all rigorous problem statements and restatements MUST be in English and use mathematical symbols**.

#### 1. 宏观拆解 (Macro Breakdown)
- **Problem Statement (English)**: Restate the overall problem in rigorous mathematical English.
- **Decomposition**: Briefly explain in Chinese how the large problem is decomposed into manageable sub-problems (e.g., "将问题等价拆解为正向和反向两个小问题" or "满足该性质需要分别证明 A 和 B 两个条件").
- **Sub-problems List**: Explicitly list the resulting sub-problems so the reader knows exactly what to expect.

#### 2. Breakdown 1
- **严谨表述 (Rigorous Statement - English Only)**: State exactly what this specific sub-problem aims to prove in formal English with math symbols.
- **Workout 拆解 (Workout Breakdown - Chinese)**:
  - **条件与结论 (Conditions & Target)**: What are the given conditions? What is the final target?
  - **等价转化 (Equivalent Translation)**: Translate the barren mathematical conditions and targets into their most "connectable" equivalent mathematical forms based on definitions. (e.g., translate "$x \in \ker(f)$" into "$f(x) = 0$", or "g is surjective" into "$N = \operatorname{Im}(g)$").
  - **逻辑搭桥 (Logical Bridging & Theorems)**: Explain the "Aha!" moment. Show the exact path that connects the translated condition to the translated target. Explicitly state the names of any theorems or axioms invoked to support the bridge (e.g., First Isomorphism Theorem).

#### 3. Breakdown 2
*(Repeat the exact structure from Breakdown 1 for all remaining sub-problems).*

#### 4. 总结 (Summary)
Provide a concluding summary in Chinese. Highlight the core trick, pitfall, or "Memory Card" (记忆卡片) that the user should memorize.

## Rate Limiting
Not applicable.

## Common Mistakes
- **Mixing languages incorrectly**: Do not write the Standard Solution in Chinese. In the Workout section, the conversational text is Chinese, but **all problem statements and rigorous formulations MUST be in English**.
- **Skipping the "Equivalent Translation"**: Do not just state the condition and jump to the bridge. You MUST explicitly show the translation step (e.g., rewriting set definitions into equation constraints).
