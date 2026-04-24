<!-- SPDX-License-Identifier: Apache-2.0 -->
<!-- Copyright 2026 Peter Zan -->

---
name: hist_failure_check
description: Quick Failure Check — 3 similar failures with causes
---

Identify 3 historical failures similar to this situation. For each, state what failed and why in 1-2 sentences.

Input: {{input_text}}

**Target focus** (if specified): {{target_focus}}

Output format:
1. **[Failure name]** — What failed: [Description] — Root cause: [Why it really failed]
2. **[Failure name]** — What failed: [Description] — Root cause: [Why it really failed]
3. **[Failure name]** — What failed: [Description] — Root cause: [Why it really failed]

**Pattern:** [Common thread across these failures]

**Warning sign to watch:** [What early indicator preceded these failures]
