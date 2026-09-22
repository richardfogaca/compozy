# Spec phases (spec-phases/v1)

Choose the requested phase explicitly; `full` remains the default. A phase is an
artifact-writing boundary, not permission for implementation or external effects.
Reuse current decisions, research and completed sections before creating anything.

- **product:** Produce or refine Part I (what/why) of `_spec.md` and applicable
  `_user_stories.md` only. Use the grill protocol for unresolved consequential
  product choices; inspect discoverable facts first. State users/problem, observable
  outcomes, scope, constraints, non-goals and open decisions. Do not author technical
  design, task decomposition or execution plans. Preserve any existing Part II and
  companions; identify impacted contracts when product decisions change. Mark the
  spec `<!-- spec-phase: product -->` while technical reconciliation remains pending.
  This is a usable PRD, not an implementation-ready spec. Stop at this artifact for
  PRD-only requests. Product readiness means sufficient requirements for technical
  shaping, not stakeholder acceptance or implementation authorization.
- **technical:** Start from sufficient Part I or accepted requirements supplied by
  the caller. Link their source and approval state and carry their requirements
  into Part I without another product interview. Complete/reconcile Part II and
  only applicable surface/test/ADR companions. Missing consequential product
  decisions block dependent technical work; never invent them. Preserve completed
  tasks and mark affected downstream inputs for reconciliation, not wholesale reset.
- **full:** Complete both parts using the normal workflow, skipping satisfied work.

After technical/full work, use `<!-- spec-phase: complete -->` only when applicable
contracts are coherent and blocking decisions are settled. This marker describes
spec completeness, not approval or validated implementation. If incomplete, retain
`<!-- spec-phase: product -->` and name the gaps. Maintain exactly one phase marker
near the title. Existing unmarked specs remain supported: inspect actual content
and acceptance rather than inventing a migration or reauthoring them.

`cy-create-tasks` must not decompose a product-only or unresolved spec. Complete the
missing technical work within existing authority first, or report the precise gap.
A clear ordinary fix requires neither a PRD nor this skill. A complex task with
settled requirements can enter technical mode directly. A spec-only request ends
at the requested artifact; when implementation is already authorized, return to
its caller so the workflow continues without another routine approval.
