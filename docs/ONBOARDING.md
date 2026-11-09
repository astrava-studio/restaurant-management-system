# Onboarding — Restaurant Menu & Management System

Welcome. This repository contains an ASTRAVA demonstration project for a customer-facing digital menu and practical restaurant workflows.

## 1. Before you start

1. Make sure you have access to the astrava-studio/restaurant-management-system repository.
2. Install Git and the editor/runtime required by the stack once it is selected.
3. Clone the repository and open the repository root in your editor.
4. Read these files in order:
   - README.md
   - docs/PROJECT_CONTEXT.md
   - docs/ASTRAVA_STUDIO_STANDARD.md

## 2. First AI-agent session

Use the coding agent and skills already installed on your machine. Do not install or copy another skill pack into this repository.

Paste this as the first task:

~~~text
You are joining the ASTRAVA Restaurant Menu & Management System project.

First inspect the entire repository. Read README.md, docs/PROJECT_CONTEXT.md, docs/ASTRAVA_STUDIO_STANDARD.md, and docs/ONBOARDING.md.

Do not modify files, scaffold an app, install dependencies, or choose a framework yet.

Report:
1. What exists in the repository and what is missing.
2. The target users and the two experiences: public digital menu and private management area.
3. The MVP candidates and product decisions that remain unresolved.
4. Existing technical decisions and unresolved decisions.
5. A proposed implementation plan in small milestones.
6. Questions that need the project owner's decision.

Pay particular attention to authorization boundaries: public customers must never gain access to management functions. Protect admin/staff operations on the server as well as in the UI. Do not collect or store payment-card data. Do not invent restaurant business rules.

Follow the ASTRAVA Studio Working Standard. Use skills already installed in this environment; do not duplicate skills or agent configuration in the repository.
~~~

## 3. Agree the product scope before coding

The project owner should resolve at least:
- Single restaurant or multiple restaurants.
- Browse-only menu or customer ordering.
- Whether QR codes are in the first release.
- Dine-in, takeaway, or both.
- Order states and who can change them.
- Whether table management is required.
- Whether taxes, discounts, modifiers, or add-ons are in scope.
- How menu images are stored and managed.
- Whether kitchen display or printing is needed.

Keep the public menu and private management experience clearly separated. Do not add payment processing unless the team explicitly approves a suitable provider and implementation plan; never store card data.

## 4. First implementation milestones

1. Agree on MVP, roles, workflows, stack, and architecture; record decisions.
2. Define the data model and authorization boundaries.
3. Build the public menu experience with responsive layouts.
4. Build protected menu-management workflows.
5. Add ordering, table association, and operational views only if included in the agreed MVP.
6. Test public/private access boundaries, input validation, order-state transitions, and error handling.
7. Document setup, demo data, and verification steps.
8. Review with another founder before merging and demonstrating.

## 5. Before opening a pull request

Follow the shared definition of done in docs/ASTRAVA_STUDIO_STANDARD.md. Include tests actually run and explain any known limitations.

**Current status:** repository setup and planning. Confirm the actual MVP and stack before scaffolding.
