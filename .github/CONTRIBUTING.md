# How to Contribute

Great to see you! Help us out by [filing bugs or feature requests](#work-with-issues), assisting others in our [forums](https://forum.bpmn.io/) or by [contributing improvements](#contribute-an-improvement).


## Table of Contents

* [Work with Issues](#work-with-issues)
    * [Create an Issue](#create-an-issue)
    * [Help out](#help-out)
* [Contribute an Improvement](#contribute-an-improvement)
    * [Discuss Code Changes](#discuss-code-changes)
    * [Code Style](#code-style)
    * [Creat a Pull Request](#create-a-pull-request)


## Work with Issues

We use our [issue tracker](../issues) for project communication, discussion and planning.


### Create an Issue

Please use one of our provided issue templates if you plan to file an issue. This ensures you provide all the details necessary for us to understand and resolve your case.

If you have a question, please [turn to our community forum](https://forum.bpmn.io/) rather than filing an issue.


### Help Out

* Share your perspective on issues
* Be helpful and respect others when commenting


## Contribute an Improvement

Learn about how to discuss code changes, our code styles and how to file a pull request.


### Discuss Code Changes

Create a [pull request](#create-a-pull-request) if you would like to have an in-depth discussion about some piece of code.


### Code Style

Most of our code styles are automatically enforced via [lint rules](https://github.com/bpmn-io/eslint-plugin-bpmn-io) and automatically checked as you submit your PR.

Would you like to double check things locally? In this case our `lint` task is your friend:

```
npm run lint
```


### Create a Pull Request

We use pull requests for feature additions and bug fixes. If you are not yet familiar on how to create a pull request, [read this great guide](https://gun.io/blog/how-to-github-fork-branch-and-pull-request).

Some things that make it easier for us to accept your pull requests

* The code adheres to our conventions
    * spaces instead of tabs
    * single-quotes
    * ...
* The code is tested
* The `npm run all` build passes (executes tests + linting)
* The work is combined into a single commit
* The commit messages adhere to the [conventional commits guidelines](https://www.conventionalcommits.org)


We are happy to assist you if you do not get these things right in the first place.


:heart: from the bpmn.io team.
