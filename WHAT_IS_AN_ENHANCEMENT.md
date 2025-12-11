# What is an Enhancement?

This note summarizes the Kubernetes enhancements definition and tracking heuristics, adapted from the upstream guide [kubernetes/enhancements/README.md](https://github.com/kubernetes/enhancements/blob/master/README.md).

## Links

* Main README (EN): `README.md`
* Chinese README: `README.zh.md`
* 什么是 Enhancement (ZH): `WHAT_IS_AN_ENHANCEMENT.zh.md`

## Translations / Related Docs

* Chinese README: `README.zh.md`
* 什么是 Enhancement (ZH): `WHAT_IS_AN_ENHANCEMENT.zh.md`
* Main README (EN): `README.md`

## When to treat something as an enhancement

* Would merit a blog post on release; user-visible and relied upon.
* Requires multiple SIGs/owners or cross-cutting coordination.
* Graduates through stages (Alpha → Beta → Stable).
* Significant scope (e.g., redesigning components, API changes, multi-week effort).
* Notable UX/operational impact that may require user retraining.

## Usually **not** an enhancement

* Implemented solely via a CRD.
* Flaky test fixes, refactors, or small perf-only tweaks.
* Minor error-message or event additions.

## Process cues (from Kubernetes)

* File an enhancement issue once the idea has buy-in; expect multi-release work.
* Use labels for ownership and stage (e.g., `sig/*`, `kind/feature`, `stage/{alpha,beta,stable}`).
* Track status across releases via boards/spreadsheets; keep discussions in linked issues/PRs.
Refer to the upstream guide for full details: [kubernetes/enhancements/README.md](https://github.com/kubernetes/enhancements/blob/master/README.md).
