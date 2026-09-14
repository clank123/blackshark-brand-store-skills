# Usage guide

[中文版本](USAGE.zh-CN.md)

This package contains five standalone agent skills. Use only the skill needed for the current task, or connect them into an end-to-end operating flow. The package does not require a particular private knowledge repository, local path or collaboration platform.

This repository is released under the [Apache License 2.0](LICENSE).

## Install and update

Install all five skills globally for every supported agent environment detected by the Skills CLI:

```bash
npx skills add clank123/blackshark-brand-store-skills --all -g
```

To update all globally installed skills later, not only the skills from this package:

```bash
npx skills update -g
```

Open a new agent session after installation or update so the refreshed skills are loaded.

## Choose a skill

| Current need | Skill | Expected result |
| --- | --- | --- |
| Clarify how brand intent, store roles and customer occasions fit together | `blackshark-brand-store-strategy` | A strategy relationship model with choices and evidence limits |
| Define what must be learned before making or extending a claim | `blackshark-operating-validation` | A proportionate validation and evidence contract |
| Turn an agreed direction into complete work without hiding dependencies | `blackshark-action-planning` | A full action structure plus a separate priority view |
| Prepare work for one person or a collaborating team | `blackshark-project-handoff` | A handoff shape proportionate to responsibility and risk |
| Compare expectations, execution and outcomes | `blackshark-operating-review` | An evidence-bounded decision to continue, adjust, complete or stop |

Each skill can be used independently. A simple, already-approved task does not need to pass through all five skills.

## Provide the smallest useful context

Start with the facts needed for the current question. A useful input may include:

- the business objective and current question;
- store roles, customer occasions and material constraints;
- confirmed decisions, existing owners and current authority;
- what changed, which parts did not change and any explicit non-goals;
- available evidence, missing evidence and the requested output.

The input does not need to be an exhaustive form. See `examples/business-context.synthetic.json` for one fictional shape.

## Preserve decisions and authority

State confirmed decisions and current authority explicitly when continuing existing work. The skills should inherit unchanged facts, owners, approvals and non-goals. If one assumption changes, reopen only the affected part instead of asking every participant to approve the whole direction again.

A gate is a decision condition, not automatically a meeting or an approval request. Missing information should limit the relevant claim or block only the dependent action.

## Run an end-to-end flow

For a new or materially changed operating question:

1. Use `blackshark-brand-store-strategy` to connect the objective, store roles, customer journey, offer, channel, experience and resource choices.
2. Use `blackshark-operating-validation` to define what evidence is needed and what cannot yet be claimed.
3. After the direction is confirmed, use `blackshark-action-planning` to preserve the complete dependency set and create a separate priority view.
4. Use `blackshark-project-handoff` to select a lightweight, collaborative or complex handoff based on the real work.
5. When results return, use `blackshark-operating-review` to separate execution, customer response, store economics, brand-network effects and method reliability.

The fictional `examples/end-to-end.synthetic.md` walkthrough demonstrates this sequence without private business context.

## Tool and permission boundary

These skills can produce analysis, plans, drafts and handoff text. The package itself does not send messages, publish content, change external systems or create commitments. A host agent may have tools, but any external action still requires the authority appropriate to that action.

Keep credentials, customer records, staff identities, internal links, private documents and real operating results outside the reusable skill files. Supply private business context only for the current authorized task and follow the host environment's retention and access rules.

## Interpret results carefully

Keep these states separate:

- readiness: whether the work can begin;
- execution: what was actually completed;
- business effect: what changed in customer or commercial outcomes;
- method reliability: whether the approach is reusable under stated conditions.

A completed handoff does not prove business effect. One positive result may support another experiment, but it does not by itself establish a generally reliable method.

## Example prompts

Open strategy question:

> Use `blackshark-brand-store-strategy` to propose differentiated roles for two fictional stores introducing one shared product. Mark assumptions and evidence limits.

Approved low-risk change:

> The direction, owner and authority are already confirmed. Use `blackshark-project-handoff` to prepare a lightweight text change. Do not create a new project or request unchanged approvals.

Evidence-bounded review:

> Use `blackshark-operating-review` to compare the expected customer behavior with the observed evidence. Keep commercial effectiveness unknown where no result was measured.
