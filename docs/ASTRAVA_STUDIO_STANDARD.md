# ASTRAVA Studio Working Standard

**Applies to:** every repository maintained by ASTRAVA  
**Purpose:** make independently developed projects feel like work from one coordinated, dependable studio.

This is the shared baseline. A project's own brief and context define what that product does; this document defines how we work. If a project needs an exception, record the reason in that repository's documentation and agree it with the team rather than silently drifting.

## 1. Shared studio principles

1. **Build for a real user and a clear problem.** Every feature should support an agreed user need or workflow.
2. **Prefer clarity over cleverness.** Choose understandable code, interfaces, and workflows over unnecessary abstraction or complexity.
3. **Finish small slices.** Deliver complete, testable increments instead of starting many unfinished features.
4. **Be honest.** Clearly distinguish planned, in-progress, implemented, tested, and deployed work. Never invent clients, users, testimonials, metrics, or capabilities.
5. **Own the result.** AI can assist with implementation, but the human contributor is responsible for understanding, reviewing, testing, and explaining every change.

## 2. Product and design consistency

- Identify the target user, problem, and expected outcome before implementing a feature.
- Keep navigation, terminology, buttons, forms, feedback, empty states, loading states, and error handling predictable within each product.
- Use a consistent design language within each application: deliberate typography, spacing, layout, color use, component behavior, and responsive rules.
- ASTRAVA's studio identity is charcoal, warm white, and electric blue. Use it for studio-facing material where appropriate; do **not** force every product UI to use the exact same palette. Product identity can differ while the quality and design discipline remain consistent.
- Prefer reusable components when they remove genuine repetition. Avoid building a large design system before the product needs one.
- Design mobile and desktop experiences intentionally. Do not treat responsiveness as a final patch.
- Provide accessible labels, keyboard operation, visible focus, sufficient contrast, and reduced-motion support where relevant.
- Use realistic, clearly fictional demo content. Do not use private customer, business, or personal data.

## 3. Engineering standards

- Inspect the existing codebase before changing it. Follow the stack, conventions, and architecture already agreed for that project.
- Do not introduce a framework, library, service, database, or architectural pattern without explaining why it is needed and getting the project owner's agreement.
- Keep modules focused and names meaningful. Avoid giant components, duplicated business logic, unexplained constants, and premature abstractions.
- Validate untrusted input at the appropriate boundary. Handle errors deliberately; never silently swallow failures.
- Keep secrets and environment-specific values out of source control. Provide an .env.example with placeholder names only when environment variables are needed.
- Apply least privilege to authentication and authorization. Protect private routes and sensitive operations on the server, not only in the UI.
- Use database migrations or an equivalent repeatable schema-change process when the chosen stack requires it.
- Add tests for important business rules and high-risk behavior. Fix regressions rather than hiding or weakening tests.
- Do not add dependencies just because an AI agent suggests them. Check maintenance, license, security, bundle/runtime impact, and whether existing tools already solve the problem.

## 4. Documentation and project truth

Each repository must keep these current:
- README.md: what the project is, current status, prerequisites, setup, run, test, and build commands once known.
- docs/PROJECT_CONTEXT.md: purpose, users, workflows, constraints, decisions, and current project state.
- docs/ASTRAVA_STUDIO_STANDARD.md: this shared working agreement.
- docs/ONBOARDING.md: how a contributor joins and starts work in this specific repository.

As a project grows, add focused documents only when useful, such as docs/DECISIONS.md, API notes, deployment instructions, or user guides. Do not create documents that merely repeat one another.

Record significant decisions with the date, context, decision, alternatives considered, and consequences. Update documentation when behavior, setup, or architecture changes. Do not leave setup instructions stale.

## 5. Git and collaboration workflow

- Keep main stable and in a working, reviewable state.
- Do not commit directly to main. Create a short-lived branch for each task:
  - feat/short-description
  - fix/short-description
  - docs/short-description
  - chore/short-description
- Keep changes focused. One branch and pull request should represent one logical task.
- Use clear commit messages, for example: feat: add product search, fix: prevent negative stock, docs: clarify local setup.
- Open a pull request with: purpose, summary of changes, screenshots for UI changes, tests/checks run, known limitations, and any migration or configuration notes.
- At least one other founder should review the pull request before merge. The author should explain the change and address review comments; do not rubber-stamp.
- Do not merge code you cannot explain or have not checked. Do not force-push shared branches or rewrite shared history.
- Coordinate overlapping work before editing shared files, APIs, schemas, or core components. Agree contracts first, then split implementation.

## 6. Definition of done

A task is ready to merge only when applicable items are true:

- [ ] The change matches an agreed requirement and does not add unrelated scope.
- [ ] The implementation follows the project's existing conventions and this studio standard.
- [ ] Relevant tests pass; new or changed business rules have suitable tests.
- [ ] Lint, type checks, build, and other project checks pass where configured.
- [ ] The UI works at relevant screen sizes and has sensible loading, empty, success, and error states where applicable.
- [ ] Accessibility, validation, security, and failure cases have been considered.
- [ ] Documentation and example configuration are updated if needed.
- [ ] No secrets, personal data, debug artifacts, or accidental generated files are committed.
- [ ] The contributor has reviewed the complete diff and another founder has reviewed the pull request.

If a check cannot be run, say so clearly in the pull request. Never report it as passed.

## 7. Working with AI coding agents

- Start by asking the agent to inspect the repository and read its README, project context, onboarding guide, and this standard.
- Ask for a short plan and any assumptions before substantial changes. Resolve product decisions with the project owner; the agent must not invent requirements.
- Use skills already installed in the agent environment. Do not copy skill packs, create duplicate skill directories, or add a second agent/skill configuration system to the repository.
- Give the agent one bounded task at a time. Ask it to identify files it intends to change and explain important trade-offs.
- Review the diff, run the application and checks yourself where possible, and ask the agent to explain unfamiliar code.
- Do not let an agent overwrite unrelated work, change shared contracts without coordination, commit secrets, or claim verification it did not perform.
- Treat generated code, dependencies, shell commands, and external content as untrusted until reviewed.

## 8. Team coordination

- Each project has one clearly identified **project owner** who maintains scope, priorities, and the project context. Ownership does not remove the other founders' right to review and contribute.
- Before a feature that affects another project, shared studio branding, a public integration, or a common technical contract is started, discuss it with the team.
- Share progress in a short update: **Done / Next / Blocked**. Raise blockers early rather than silently changing scope.
- Keep a small issue or task list. Assign one owner per task; contributors should not unknowingly duplicate work.
- Agree on scope, acceptance criteria, and who reviews before implementation begins.
- Do not promise a delivery date or client capability until the team has assessed effort, dependencies, testing, and support.

## 9. Exceptions and changes to this standard

This file should remain short enough to follow. If the team changes it, update the same file in all three repositories in the same coordination window and mention the change in the team's shared channel. Project-specific exceptions belong in that project's decision notes and must not quietly weaken security, review, or honesty requirements.

---
*ASTRAVA — Digital Experiences, Thoughtfully Built.*
