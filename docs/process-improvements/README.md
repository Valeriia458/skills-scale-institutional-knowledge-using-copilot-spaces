# Process improvements: add personas, checklists, and templates

This branch implements a set of process improvements requested in issue #4:
- Explicitly adds additional personas to the roles document (Engineering Manager, UX Researcher/Designer, Release Manager, DevOps/Platform Engineer, Customer Success/Support Lead, Data Analyst, Security Liaison, Program/Portfolio Manager).
- Adds actionable checklists for planning, release, and retrospective action items.
- Adds a machine-readable persona mapping for automation (labels, CODEOWNERS, templates).

Why these changes:
- Clarify ownership and reduce ambiguity in handoffs.
- Standardize release readiness and rollback procedures to reduce production risk.
- Ensure action items from retrospectives are tracked and completed.
- Enable automation (labels, templates) using the persona mapping file.

Files added/updated in this PR:
- docs/octoacme-roles-and-personas.md (updated to include Additional Personas and mapping)
- docs/checklists/planning-checklist.md
- docs/checklists/release-checklist.md
- docs/checklists/retrospective-action-items.md
- docs/templates/persona-mapping.yml
- docs/process-improvements/README.md

Acceptance criteria (suggested):
- [ ] Docs added to `docs/` and linked from the main roles/process docs
- [ ] Stakeholders (PMs, PdMs, Eng Managers, Security) have reviewed and approved role responsibilities
- [ ] Checklists are referenced in planning and release playbooks

Next steps:
- Open PR and request review from @Valeriia458
- Iterate on wording based on feedback and assign owners to each persona
- Optionally seed automation (labels/CODEOWNERS) using `docs/templates/persona-mapping.yml`
