# Contributing to FancePro

## Two constraints that are the project

**No build, no dependencies.** This is HTML, CSS and JavaScript served as files. Do not add a bundler, a framework, or a package that needs installing. If a change requires a build step, it is the wrong change for this repo.

**Agents stay in their lane.** Four agents each have a mandate and a strict JSON contract, and the value comes from what they are forbidden to do:

| Agent | May not |
| --- | --- |
| Budgeting | Pick a payoff method or asset mix |
| Debt strategy | Set the investing share |
| Investment planning | Name a product or choose a payoff method |
| Coordinator | **Average the proposals** |

The coordinator resolving conflict by averaging is the specific failure this project exists to avoid. A pull request that softens any of these constraints removes the reason the interface is interesting.

## Determinism

The agents are deterministic. The same case must produce the same allocation every run. If your change introduces variability, it needs to be justified in the pull request.

## Guardrails

Rules are numbered and cited in the output. When the coordinator publishes an allocation it names the conflict and shows the arithmetic. Keep that visible - the audit trail is the product.