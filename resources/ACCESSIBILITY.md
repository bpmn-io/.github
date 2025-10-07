# Accessibility

We strive to make our tools usable for everyone.

## Formal Goal

Achieve and maintain [WCAG 2.1](https://www.w3.org/TR/WCAG21/) Level A compliance for the Desktop Modeler and core libraries.

## Limitations

As the most prominent tools produced by the team are visual, we accept that some users may not be able to fully use them. However, this does not undermine the goal of making the tools usable if it is possible.

## Helpful Tools

### [Axe devtools extension](https://www.deque.com/axe/devtools/chrome-browser-extension/)

Use axe in your browser to scan and debug accessibility issues in the application.

### [axe-core](https://github.com/dequelabs/axe-core)

Use axe-core in the CI pipeline to automatically detect issues in the project.

### Keyboard

Use TAB to move around the project with your keyboard. Some issues may slip under the radar of the automatic scanner but can be easily noticed by a user. For example, a `\<span>` element serving as a button via JavaScript handlers is not reachable with keyboard, and not reported by axe at the same time.
