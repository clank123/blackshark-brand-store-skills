# 黑鲨 · 品牌与门店经营 Skills

**BlackShark Brand & Store Ops Skills** — owned and maintained by 黑鲨（BlackShark）.

Package name: `blackshark-brand-store-skills`. BlackShark is the project owner and the intended public attribution. Customer identities and private business information are not part of that attribution.

An open-source collection of agent skills for connecting brand strategy with store operations: customer choice, store roles, product experiences, resource decisions, evidence and learning.

## Scope

The intended capabilities cover opening, ongoing operations, campaigns, repeat visits, structural adjustments and multi-store coordination. Each task should use the parts it needs; a simple handoff should remain simple.

The planned core skills are:

- `blackshark-brand-store-strategy`: connect brand objectives, store roles, customer journeys and resource choices.
- `blackshark-operating-validation`: define the evidence needed for a decision and distinguish outcomes from assumptions.
- `blackshark-action-planning`: turn an agreed direction into concrete actions and dependencies.
- `blackshark-project-handoff`: prepare work that the responsible people can execute and review.
- `blackshark-operating-review`: compare expectations, execution and outcomes, then update the relevant decisions.

All five cores have been tested in a local installation. They preserve confirmed decisions and authority, scale the handoff shape to the work, retain complete dependencies behind any priority view, and keep readiness, business effect and method reliability separate.

## Getting started

Read the [Usage guide](USAGE.md) or [中文使用说明](USAGE.zh-CN.md) to choose one skill or connect all five. The [end-to-end synthetic walkthrough](examples/end-to-end.synthetic.md) shows how an open question becomes a strategy, validation contract, action plan, handoff and evidence-bounded review.

Install all five skills globally for every supported agent environment detected by the Skills CLI:

```bash
npx skills add clank123/blackshark-brand-store-skills --all -g
```

Update all globally installed skills later with the following command. This update is not limited to this package:

```bash
npx skills update -g
```

The installer detects the supported agent environments on the current machine. Open a new agent session after installation or update so the refreshed skills are loaded.

## Business context

Business-specific context is supplied by the user for the current task. Real organization details, customer records, internal documents, credentials and operating results remain outside the skill package. The core must not assume access to a particular knowledge repository, local filesystem path or collaboration platform.

[The example context](examples/business-context.synthetic.json) and the [end-to-end synthetic walkthrough](examples/end-to-end.synthetic.md) are entirely fictional. They illustrate one possible input and workflow, not a required exhaustive form or evidence of business performance.

## Release status

Released under the [Apache License 2.0](LICENSE). This package provides agent instructions and examples; it does not prove business outcomes or authorize external actions.
