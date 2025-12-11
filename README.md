# 📄 KWeaver Design Docs (KEP-Style)

English | [中文](./README.zh.md)

## 📌 Background

KWeaver is growing across complex subsystems—Ontology Data Flow, Data Agent, Sandbox, distributed execution, and more. To keep architecture consistent, enable effective collaboration, and maintain traceable decisions for every major change, we follow a structured design doc process.

KWeaver adopts a **KEP (Kubernetes Enhancement Proposal)-style governance model** for enhancements and design documents.

---

## 🧩 What Is a KEP?

KEP = **Enhancement Proposal + Design Document**

Originally from the Kubernetes community, used to manage:

* New feature proposals
* Architecture designs
* Technical improvements
* Large-scale system changes
* Community discussion and reviews

It is a proven governance pattern for long-running, multi-contributor projects.
What is an Enhancement? [Read more...](WHAT_IS_AN_ENHANCEMENT.md)

---

## 🏆 Why KEP for KWeaver?

| KWeaver needs | KEP provides |
| --- | --- |
| Collaborative design review | PR + line-by-line comments |
| Standardized docs | Single template and structure |
| Traceable evolution | Versioned docs with status |
| Architecture sanity | Clear goals/non-goals, risks, alternatives |
| Contributor clarity | Full context for every change |
| Auditable decisions | History that can be referenced |

This is critical for systems spanning:

* Ontology
* Data Flow
* Data Agent
* Sandbox
* VEGA

---

## 📁 Repository Layout for KEPs

```text
docs/
└── keps/
    ├── 0001-core-architecture.md
    ├── 0002-dsl-v2.md
    ├── 0003-data-agent.md
    ├── 0004-task-pipeline-v2.md
    └── templates/
        └── kep_template.md
```

Notes:

* `0001`, `0002`, ... are ordered IDs for stable sorting.
* Each file is a full design document.
* `templates/kep_template.md` is the canonical template.
* Every KEP is reviewed via PR; discussions and changes stay in GitHub.

---

## 🔄 KEP Workflow in KWeaver

### 1) Open a design Issue

Create a GitHub Issue:

```text
[KEP] <feature name>
```

Include:

* Background / Why
* Problems to solve
* Initial ideas (draft)

### 2) Create the KEP doc

Copy from the template:

```text
docs/keps/templates/kep_template.md
```

Save as:

```text
docs/keps/00xx-<short-title>.md
```

IDs are assigned in order.

### 3) Submit via Pull Request (core step)

Example PR title:

```text
KEP-0003: Data Agent Design
```

Use the PR for:

* Discussion
* Line-by-line review
* Questions
* Design updates

### 4) Manage status (keep it visible)

Each KEP tracks status:

```text
Status: Draft / Review / Implementable / Implemented / Deprecated
```

Typical meaning:

* Draft: initial writeup
* Review: under team review
* Implementable: approved for implementation
* Implemented: shipped
* Deprecated: retired

### 5) Implementation must follow the KEP

When status is **Implementable**:

* Related code PRs must reference the KEP.
* Implementation stays consistent with the design.
* Conflicts require updating the KEP first.

### 6) Long-term tracking

Each release can highlight delivered KEPs, e.g.:

```text
KWeaver v0.3 shipped:
* KEP-0002 DSL V2
* KEP-0004 Task Pipeline V2
```

Docs become durable project assets.

---

## 📦 Examples of KEP-Style Projects

* Kubernetes: `https://github.com/kubernetes/enhancements`
* Istio: `https://github.com/istio/enhancements`
* Knative: `https://github.com/knative/enhancements`
* OpenTelemetry: `https://github.com/open-telemetry/oteps`
* Helm (HIPs): `https://github.com/helm/community/tree/master/hips`
* Rust (RFCs): `https://github.com/rust-lang/rfcs`
* VS Code (API proposals / feature RFCs): `https://github.com/microsoft/vscode/issues?q=label%3Aapi-proposal`

These show how mature projects structure proposals, discussion, status, and implementation links.

---

## 📄 KEP Template (simplified for KWeaver)

Located at:

```text
docs/keps/templates/kep_template.md
```

Template content:

```text
# KEP-<ID>: <Title>

- Author(s):
- Status: Draft / Review / Implementable / Implemented / Deprecated
- Created: YYYY-MM-DD
- Last Updated:
- Discussion PR:

## 1. Motivation
Why is this needed? What problems exist today?

## 2. Goals
What this design aims to achieve.

## 3. Non-Goals
What is explicitly out of scope.

## 4. High-Level Design
Architecture, data flows, module boundaries.

## 5. Technical Details
- APIs / interfaces
- Data structures
- State machines
- Execution flow
- Compatibility and migration

## 6. Risks / Trade-offs

## 7. Alternatives Considered

## 8. Milestones

## 9. References
```
