# Validation contract

```text
ID and scope
Current facts / problem / unknowns
Hypothesis and target user behavior
Candidate actions and explicit non-goals
Owner, time window, constraints, project relationships
Evidence contract: metric meaning, source, baseline, target, collector, confidence, limits
Gates: input, release, evidence, method promotion
Continuation and stop conditions
Result: 成立 / 部分成立 / 不成立 / 无法判断
Next decision: 加码 / 保持 / 调整 / 停止 / 补证据
Business-result account / reusable-capability account
```

The contract is an interface, not a mandatory form. For a small or already-confirmed task, retain only the fields needed to prevent a wrong decision and preserve the evidence boundary. Reuse inherited approvals and authority; list only genuinely new or changed decisions. A change to one store or project does not create a reconfirmation gate for unaffected approved work.

Report evidence on three independent lines:

```text
Readiness: ready / conditionally ready / not ready, with missing execution conditions
Business effect: supported / partly supported / unsupported / cannot determine, with observed evidence
Method reliability: candidate / bounded pattern / reusable method, with sample and counterexample limits
```

Do not let a missing business-result metric erase a readiness conclusion, and do not let one positive business cycle prove method reliability.
