<!-- SPDX-License-Identifier: Apache-2.0 -->
<!-- Copyright 2026 Peter Zan -->

---
name: rhet_loyalty_check
description: Quick loyalty audit across four dimensions — language loyalty, beneficiary analysis, evidence quality, and stakeholder completeness. Produces GREEN/YELLOW/RED flags for each dimension. Use for rapid assessment of any recommendation, proposal, or advice.
---

Run a quick loyalty audit on this content across four dimensions. For each dimension, assess and assign a flag: GREEN (aligned with user), YELLOW (mixed/unclear), RED (misaligned — serves provider over user).

Input: {{input_text}}
Focus: {{target_focus}}

Output format:

**1. Language Loyalty** (Rhetoric lens)
Flag: [GREEN/YELLOW/RED]
[One sentence: Is the language optimized for the user's outcome or the provider's protection?]

**2. Beneficiary Analysis** (Philosophy lens)
Flag: [GREEN/YELLOW/RED]
[One sentence: Who actually benefits — the stated beneficiary or someone else?]

**3. Evidence Quality** (Epistemology lens)
Flag: [GREEN/YELLOW/RED]
[One sentence: Are the claims well-supported or asserted without evidence?]

**4. Stakeholder Completeness** (Sociology lens)
Flag: [GREEN/YELLOW/RED]
[One sentence: Are all affected parties considered or are key stakeholders excluded?]

**Overall Loyalty Score:** [GREEN/YELLOW/RED]
**One-line recommendation:** [Single actionable sentence for the user]
