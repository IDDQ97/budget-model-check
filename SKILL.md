---
name: budget-model-check
description: Use before coding when choosing a capable, lower-usage model for a task, especially with a limited subscription allowance.
---

# Budget Model Check

Before inspecting project files or changing code, recommend the least costly model that is likely to complete the task well. Base the choice on task scope, uncertainty, impact, and the models actually available in the current tool.

Give one compact preflight:

```text
Model: <available model and effort>
Why: <one short sentence>
Escalate if: <one observable signal>
```

If the recommendation differs from the active model, pause for the user to switch or approve continuing with the active model. Do not claim to switch models or launch another coding tool unless the environment actually supports it.

## Routing

- Clear, small, local change: choose the most efficient available model at low effort (for example, GPT-6 Luna · Low or Claude Code's lowest-cost model).
- Clear task spanning several files: choose an efficient model at medium effort (for example, GPT-6 Luna · Medium or Claude Code's mid-tier model).
- Unclear root cause, architecture, security-sensitive behavior, or high-impact change: choose the strongest practical workhorse model at medium effort (for example, GPT-6 Sol · Medium or a stronger Claude Code model, depending on availability and need).
- A supported browser workflow specifically needs WebMCP: recommend GPT-5.6 Terra when available.
- Recommend a separate Claude Code pass only when an independent plan or review is likely to catch a consequential mistake. Use it after the implementation plan or diff exists; do not run two tools that edit the same working tree concurrently.

Treat model names and plan limits as changeable. Check the active model picker and current plan information when those facts affect the recommendation. Do not estimate remaining subscription time or promise a fixed number of prompts; task size, context, tools, and provider limits vary.

Escalate one step if a focused attempt fails a relevant check, misses a stated requirement, or leaves the cause unresolved. If the issue is missing information or an environment failure, resolve that first instead of choosing a stronger model.
