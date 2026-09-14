---
name: blackshark-operating-review
description: Use when execution and evidence must be reviewed at a weekly, project, node, store, or multi-store level and the original problem needs an evidence-bounded state update.
---

# BlackShark Operating Review

Review what actually happened, what changed, and what should happen to the original problem. This general core does not require a fixed meeting, report, repository, or operating platform.

## Anchor to the original problem

Identify the original problem or decision, its prior state, expected behavior, actions, evidence window, and applicable decision boundary. Preserve its identifier when one exists. Review scope may be weekly, project, node, single-store, brand, or multi-store; choose only the relevant layers.

Separate:

1. execution fact — what was or was not done;
2. customer behavior — what people actually did;
3. store or business result — operating and economic effects within the stated window;
4. brand or network result — shared demand, transfer, role conflict, or durable brand evidence;
5. method reliability — repeated real samples, independent operation, boundaries, counterexamples, and failure modes.

Do not infer a later layer from an earlier one. Publication or task completion is not customer behavior; positive feedback is not revenue; one store or one cycle is not a reusable method.

## Decide from evidence

For each relevant layer, state fact, inference, confidence, limitation, and result. When evidence is insufficient, write `未知` or `无法判断` and continue observing if that is the bounded next step. In that case, do not manufacture a new action（不制造新动作）, do not manufacture a new rule（不制造新规则）, and do not force a knowledge record merely to fill a template.

Update the original problem（原问题）directly to exactly one current state:

- `继续`: the direction remains live under existing conditions;
- `调整`: a supported change is needed, with the changed premise named;
- `完成`: the original acceptance condition is met;
- `停止`: the stop condition is met or the direction is no longer justified.

If a final state cannot yet be supported, keep the prior state and mark the result unknown. Do not reopen unaffected decisions or turn review into a fresh approval round.

## Method learning

Create or revise a reusable method only when there is genuinely new, bounded knowledge. Promotion requires repeated real samples, ability to operate independently, explicit applicable boundaries, and counterexamples or failure modes. A method cannot be promoted by occurrence count alone（不能按次数）.

## Output

Return the review scope, evidence by layer, original-problem state update and rationale, next observation or action only if supported, and any method-learning decision. Keep readiness, business effect, and method reliability distinct.

Read `references/review-model.md` for the evidence matrix and conservative update rules.
