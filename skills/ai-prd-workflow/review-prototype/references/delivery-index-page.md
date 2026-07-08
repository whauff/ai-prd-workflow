# Delivery Index Page

Use this reference when refining a total directory page, project directory page, review navigation page, or delivery entrance page.

The goal is traceability and review efficiency. Directory pages are not marketing pages, dashboards, or documentation dumps.

## Two-Level Entry Model

Use two levels when a workspace contains multiple requirements or multiple deliverables.

Total directory page:

- Acts as project index only
- Shows project name, date, status, version, short summary, and an "enter project" action
- Does not expose deep PRD, rules, prototype, flowchart, or archive links

Project directory page:

- Acts as the review entrance for one requirement
- Shows project name, recent update, version/status, review order, official deliverable entrances, and update log
- Owns the traceability record for changes that affect review understanding

## Review Order Model

Use a stable review order when the requirement has several deliverables:

1. Align the口径 first: brief, review summary, decision log, or rule conclusion
2. Review the prototype next: admin, mobile, employee-side, store-side, or other relevant entrances
3. Cross-check final deliverables: PRD, rules, flowchart, delivery notes, or acceptance path

This order is a recommendation, not a forced process. Adjust labels to the deliverables that actually exist.

## Naming Rules

- Use fixed Chinese names for stable deliverables.
- Keep version numbers only where they help distinguish formal versions.
- Do not expose raw filenames such as `review_decisions_v1.0.html` as link labels.
- Do not append versions to every button. If a file changes but the overall package version does not, record it in the update log.
- Status text should be short and semantically stable: for example `可评审`, `已上线`, `归档`.

## Visual Rules

- Directory pages should be quiet, scannable, and sparse.
- Clickable entries must look more clickable than descriptions.
- Avoid large hero titles, decorative dividers, heavy pills, nested cards, and long explanatory paragraphs.
- Metadata, version, and update time should be visible but quiet.
- Use status color sparingly to distinguish review state, launch state, or archive state.

## Update Log Rules

Register changes when they affect review traceability:

- PRD, rules, prototype, flowchart, delivery note, or project status changes
- Review order changes
- Official entrance changes
- Status or version changes
- Significant prototype refinement that changes understanding, navigation, or state expression

Do not register pure formatting changes that do not affect review.

Each log item should include:

- Date
- Object
- Short change description
- Version or status when relevant

## Review Questions

- Can a reviewer enter the right project and then the right deliverable without guessing?
- Is the total directory only a project index?
- Does the project directory carry the official review entrances and update log?
- Are raw filenames hidden behind fixed Chinese labels?
- Are status, version, recent update, and update log consistent?
