# Admin Structure Page

Use this reference when refining backend, admin, configuration, list, audit, status processing, or operations management prototypes.

The goal is to preserve operational clarity. Admin prototypes should be scannable, comparable, and action-oriented before they are visually polished.

## Applicable Pages

- Configuration pages
- List and table pages
- Detail, edit, audit, approval, and processing pages
- Rule management, status management, and exception handling pages

## Structure Principles

- Start with page responsibility: query, compare, configure, approve, process, or monitor.
- Keep filter, table/list, detail, side panel, and action area responsibilities distinct.
- Lists are for scanning and comparison, not for explaining rules.
- Details are for structured fields and necessary operations, not for dumping the PRD.
- Put high-frequency actions near the data they affect; keep destructive or exceptional actions visually secondary unless they are the current main task.
- Keep page skeleton stable across states. State changes should be expressed through values, tags, visibility, and actions.

## List And Table Rules

- Every column must support identification, comparison, decision, or operation.
- Delete columns that only repeat adjacent information.
- Cell subtext is only for structured incremental information: time, count, source, range, missing reason, version, or related object.
- Do not put process explanations, rule explanations, consequences, or review notes into cell subtext.
- If every row repeats the same meaning, remove the repeated copy and express it through the column name, status tag, or filter.
- For dense tables, prioritize field comparison over decorative spacing.

## Action And State Rules

- Primary action should match the current page responsibility.
- Secondary actions should be lower contrast and should not compete with the primary action.
- Disabled, loading, empty, error, no-permission, completed, and blocked states should be explicit.
- When an action is unavailable, show the reason only if the operator needs it to decide the next step.
- Avoid binding demo behavior to ordinary controls unless the interaction is part of the prototype's review scope.

## Visual Rules

- Use restrained density, stable toolbars, clear tables/forms, and predictable spacing.
- Do not over-card every region.
- Do not use presentation-site effects, decorative gradients, or heavy visual frames.
- Status colors must keep fixed meaning across the page.
- Review auxiliary controls, such as summary or hot zones, must not look like production actions.

## Review Questions

- Can an operator quickly compare rows and identify what requires action?
- Does every field, column, and button have a clear operational responsibility?
- Are explanations living in the page body because the PRD is unclear?
- Are same-type pages and states using the same skeleton, field names, and module titles?
- Does the layout survive dense data, long names, sparse data, and no-permission states?
