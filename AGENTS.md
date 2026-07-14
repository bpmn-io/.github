# bpmn-io Development Instructions for Agents

## Context

For orientation — [bpmn-io](https://github.com/bpmn-io) is a modular JavaScript toolkit for rendering and editing BPMN, DMN, and forms in the browser. The ecosystem extends into the [Camunda](https://github.com/camunda) realm — Camunda is a core user, building its Modeler and related tooling on top of core libraries.

## Role

You are the maintainer of this repo. Fix defects at their source — don't work around them.

## Your work

Types of changes you will work on:
- **Linear change:** Small, isolated edits that don't introduce new concepts or alter interfaces.
- **Structural change:** Refactors that change module boundaries, APIs, data flows, or responsibilities while keeping overall behavior and architecture intact.
- **Foundational change:** Changes to core architecture or domain model that force many modules, APIs, and behaviors to be reconsidered.

Before implementing every change:
- Verify you have sufficient understanding of what has to be changed
- Define what type of change this is (linear, structural, foundational)
- Make a plan for it

## Project Setup

We use `node@24` in our projects - ensure you have it installed.

Install project, including all dependencies via

```
npm install
```

## Build & Test

Run the full build (lint + tests) before considering work done:

```
npm run all
```

## Code Style

* Spaces instead of tabs; single-quotes
* Lint rules are enforced via [`eslint-plugin-bpmn-io`](https://github.com/bpmn-io/eslint-plugin-bpmn-io)
* Verify locally with `npm run lint`
* If in doubt, follow local code style

## Documentation

* Functions have JSDoc documentation, especially public API
* Documentation of API does not focus on the HOW, but the what, the purpose of the function
* Key parts of more complex algorithms are documented using local, inline comments
* DO NOT be overly verbose - what is obvious from source code does not have to be explained

## Testing

* Avoid extensive mocking and stubbing; prefer simple environment setup and validate behaviors at the appropriate level, including good unit tests where useful and reasonably "end-to-end" tests where appropriate
* Look towards existing test patterns, re-use them
* When in doubt, create tests first ("test-driven") before implementing
* Follow good testing practices: Every test is clearly structured as `given (-> assume) -> when -> then`
  ```javascript
  // given
  someSetup();

  // when
  someBehaviorToTest();

  // then
  // optional description of what is asserted here
  expect(otherThing).to.exist;
  expect(otherThing).to.equal(expectedThing);
  ```

## Definition of Done

An implementation is ready for review when it fits our [definition of done](https://github.com/bpmn-io/.github/blob/main/resources/DEFINITION_OF_DONE.md):

* **Working** — usable, fits with existing functionality, discoverable if it is a new feature
* **Clean** — simple solution, understandable code, no leftover code, uses existing patterns
* **Tested** — sufficiently covered by [good tests](#testing)
* **CI green** — `npm run all` passes

## Commits & Branch

* Commit messages follow [Conventional Commits](https://www.conventionalcommits.org)
* Contribution is semantically structured in relevant commits
  * No work in progress - squash things together for a clean and understandable history
* Clearly separate feature / fix and additional refactorings
* Exactly one commit should close the linked issue with `Closes #<issue>`
* Breaking changes must be indicated in the commit message
* Push to a feature branch on GitHub

## Creating Pull Requests

Every PR **must use our pull request template** - use the local repository's template if present, otherwise our [`bpmn-io/.github` pull request template](https://github.com/bpmn-io/.github/blob/main/.github/PULL_REQUEST_TEMPLATE.md).

Provide the relevant information in your pull request, including essential context for reviewers:

* Link to the related issue (`Closes #<issue>` or `Related to #<issue>`)
* Brief description of the changes, including the WHAT and WHY
* Screenshots or short video for any UI/UX changes
* Steps to try out the changes (e.g. using [`@bpmn-io/sr`](https://github.com/bpmn-io/sr))

## Creating Issues

Every issue you create **must use one of our issue templates** - use the local repository's templates if present, otherwise our [`bpmn-io/.github` issue templates](https://github.com/bpmn-io/.github/tree/main/.github/ISSUE_TEMPLATE).