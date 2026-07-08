# Prototype Review Checklist

Use this checklist before and after refining an existing prototype for review.

## 1. Scope Guard

- Confirm the requested work is review refinement, not a new feature.
- Confirm the page already has a business structure.
- If the user is actually disputing page responsibility, field hierarchy, rule scope, status meaning, or flow order, stop and route back to structure/PRD discussion.

## 2. Page Body Admission

Only keep content in the page body if a real user would see or use it.

Allowed page-body content:

- Field values
- Status labels
- Buttons
- Lists, cards, tables, forms
- Empty, error, disabled, loading, completed, blocked states
- Short operation guidance that is necessary for the user to proceed

Move or delete:

- Rule explanations
- Review reminders
- Why-this-design explanations
- "For review" notes
- Duplicated helper copy
- Broad conceptual descriptions

## 3. Same-Type Consistency

Before editing one state or page variant, check same-type screens:

- Same module title should stay the same across states.
- Same field should keep the same label and position.
- State differences should appear through labels, values, visibility, or actions.
- Variants should only change necessary differences; they should not casually change the main page skeleton.

## 4. Redundancy Check

Delete or reduce content when:

- A title already says it.
- A status label already says it.
- A button already says it.
- The same count, progress, object name, rule, or action appears in multiple places.
- Left-side footer text repeats the right-side primary button action.
- A secondary button duplicates a whole-card click behavior without adding a distinct action.

## 5. Visual Weight

Use visual weight to express priority:

- Primary action: clear, singular, and aligned with current state.
- Secondary actions: lower contrast.
- Status: visible but not louder than the page title or primary action.
- Version and metadata: quiet.
- Review auxiliary controls: useful but not dominant.

Avoid:

- Heavy borders around every section.
- Too many filled pills.
- Large explanatory cards.
- Over-styled buttons for low-importance links.
- Decorative gradients, orbs, and presentation-site effects.

## 6. Style Standardization

Unify only the dimensions that affect review quality:

- Typography hierarchy
- Spacing rhythm
- Color semantics
- Form controls
- Button hierarchy
- Card/list/table density
- Disabled, error, empty, loading, success, and blocked states

Do not use review refinement as permission to redesign the product. If a visual change changes how the business should be understood, stop and route it back to PRD, rules, or structure discussion.

## 7. Platform Fit

For mini-program/mobile prototypes:

- Prefer mobile-native density, card rhythm, fixed bottom actions where appropriate, and stable navigation/header treatment.
- Do not make the page feel like a desktop backend shrunk into a phone.
- Use system fixed assets, such as mini-program capsule visuals, when already available.

For admin/web prototypes:

- Prefer scannable density, table/form clarity, restrained spacing, and stable toolbars.
- Do not over-card every region.
- Prioritize field comparison and operational efficiency over decorative hierarchy.

## 8. State Completeness

Check whether the page covers the states that matter for review:

- Empty
- Loading
- Error
- Disabled
- No permission
- Completed
- Blocked/unavailable
- Expired or out-of-count, when relevant

Only add states that are in scope; do not invent business states.

## 9. Robustness Check

Before finishing, check:

- Responsive layout
- Basic keyboard/focus visibility for interactive elements
- Long titles, long names, and long status labels
- Empty lists and sparse data
- Dense lists and high-count data
- Text clipping, overlap, and unstable layout shifts

Do not claim the prototype is review-ready if it only looks correct in the current viewport.

## 10. Directory Update

If review refinement changes review understanding, prototype navigation, status expression, or version, update the project directory page:

- Top-level recent update date if appropriate
- Update log entry with date, object, short change, and version/status

Do not register pure formatting changes that do not affect review traceability.
