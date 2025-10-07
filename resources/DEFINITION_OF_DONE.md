# Definition of Done

Issues may enter the _needs review_ stage once their implementation conforms to our definition of done:

* signed-off by you from _user perspective_
  * usable, cf. [design principles](https://github.com/bpmn-io/design-principles)
  * discoverable (if feature)
  * accessible, cf. [accessibility](./ACCESSIBILITY.md)
  * fits with regards to existing functionality
* signed-off by you from _maintainer perspective_
  * simple solution
  * understandable
  * sufficiently and well tested (cf. [good unit tests](https://gist.github.com/nikku/1dc2edb553565238c7bf))
  * code is _clean_
  * satisfies our code standards (cf. [automatically enforced lint rules and code style](../.github/CONTRIBUTING.md#Code-Style))
* signed-off by CI
  * continuous integration passes
* available as feature branch on GitHub
  * contains the cleaned up commit history
  * commit messages satisfy our [commit message guidelines](https://www.conventionalcommits.org)
  * one commit on the branch closes the issue via a `Closes #issuenr` statement in the body

For addititional details, refer to the [contributing guidelines](../.github/CONTRIBUTING.md#create-a-pull-request).
