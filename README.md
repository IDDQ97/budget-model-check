# Budget Model Check

A small agent skill that recommends a suitable model before coding starts, with limited subscription usage in mind. It gives a short reason and a concrete escalation signal. It does not automatically change models or start another coding assistant.

The routing is intentionally conservative: use an efficient model for clear work, increase capability only when uncertainty or impact calls for it, and keep independent reviews for consequential changes. Model names, availability, and subscription limits can change; the skill asks the agent to use the current model picker and plan information.

## Install

### Codex

Copy this folder into your personal skills directory:

```text
~/.codex/skills/budget-model-check/
```

On Windows, the default location is:

```text
%USERPROFILE%\.codex\skills\budget-model-check\
```

### Claude Code

Copy `SKILL.md` into:

```text
~/.claude/skills/budget-model-check/SKILL.md
```

Then invoke it from Claude Code's skill menu (typically `/budget-model-check`) or let Claude load it when the task matches its description.

## Example

For a small, clearly scoped fix:

```text
Model: GPT-6 Luna · Low
Why: The change is local and the expected behavior is clear.
Escalate if: The focused test still fails after one targeted fix.
```

For an intermittent bug across session refresh and routing, the skill should recommend a stronger workhorse model because the cause is uncertain.

## Notes

- This is guidance, not an automatic model router. The user may need to change models in the app.
- Subscription usage cannot be translated into a reliable fixed number of hours or prompts.
- The skill recommends Claude Code as a separate review only when that extra pass is useful; it does not launch Claude Code.

## License

MIT. See [LICENSE](LICENSE).
