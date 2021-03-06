Code Review
===========

A guide for reviewing code and having your code reviewed.

Everyone
--------

* Accept that many programming decisions are opinions. Discuss tradeoffs, which
  you prefer, and reach a resolution quickly.
* Ask questions; don't make demands. ("What do you think about naming this
  `:user_id`?")
* Ask for clarification. ("I didn't understand. Can you clarify?")
* Avoid selective ownership of code. ("mine", "not mine", "yours")
* Avoid using terms that could be seen as referring to personal traits. ("dumb",
  "stupid"). Assume everyone is attractive, intelligent, and well-meaning.
* Be explicit. Remember people don't always understand your intentions online.
* Be humble. ("I'm not sure - let's look it up.")
* Don't use hyperbole. ("always", "never", "endlessly", "nothing")
* Don't use sarcasm.
* Keep it real. If emoji, animated gifs, or humor aren't you, don't force them.
  If they are, use them with aplomb.
* Talk in person if there are too many "I didn't understand" or "Alternative
  solution:" comments. Post a follow-up comment summarizing offline discussion.

Having Your Code Reviewed
-------------------------

* A picture, or better, a gif (use <a href="http://www.cockos.com/licecap/">LiceCap</a>), goes a long way. Make your PR sexy.
* If a picture does not work, a short explanation of what the PR does is necessary. Give some context and don't assume the reviewer knows the project from head to toe.
* Be grateful for the reviewer's suggestions. ("Good call. I'll make that
  change.")
* Don't take it personally. The review is of the code, not you.
* Explain why the code exists. ("It's like that because of these reasons. Would
  it be more clear if I rename this class/file/method/variable?")
* Extract some changes and refactorings into future tickets/stories. As much as possible, a PR should either be a feature, or a technical PR, not both.
* Link to the code review from the ticket/story. ("Ready for review:
  https://github.com/organization/project/pull/1")
* Push commits based on earlier rounds of feedback as isolated commits to the
  branch. Do not squash until the branch is ready to merge. Reviewers should be
  able to read individual updates based on their earlier feedback.
* Seek to understand the reviewer's perspective.
* Try to respond to every comment.
* Wait to merge the branch until Continuous Integration (TDDium, TravisCI, etc.)
  tells you the test suite is green in the branch.
* Merge once you feel confident in the code and its impact on the project. It is your responsibility to merge, not the reviewer's.
* No 'WIP' commits in the history when PR is ready to be reviewed. Rebase/amend your commit(s).
* Don't forget the changelog !

Reviewing Code
--------------

Understand why the change is necessary (fixes a bug, improves the user
experience, refactors the existing code). Then:

* Communicate which ideas you feel strongly about and those you don't.
* Identify ways to simplify the code while still solving the problem.
* If discussions turn too philosophical or academic, move the discussion offline
  to a regular Friday afternoon technique discussion. In the meantime, let the
  author make the final decision on alternative implementations.
* Offer alternative implementations, but assume the author already considered
  them. ("What do you think about using a custom validator here?")
* Seek to understand the author's perspective.
* Sign off on the pull request with a :thumbsup: or "Ready to merge" comment.
* A PR can be perfect, but usually it's not. Please take the time, if possible, to run the code on your machine, and understand critical parts of the code that have been changed added.

Style Comments
--------------

Reviewers should comment on missed [style](../style)
guidelines. Example comment:

    [Style](../style):

    > Order resourceful routes alphabetically by name.

An example response to style comments:

    Whoops. Good catch, thanks. Fixed in a4994ec.

If you disagree with a guideline, open an issue on the guides repo rather than
debating it within the code review. In the meantime, apply the guideline.

Automatic Reviews
--------------

Where possible integrate relevant code checking tools into the review process in order to automate parts of it.

Ruby
 - [`rubocop`](https://github.com/bbatsov/rubocop) for checking formatting and code style. To add it to a Rails project, you need to add `gem 'rubocop', require: false` to the Gemfile. Running the command `rubocop` will then list all violations of the default rules. To override the rules with project / team - specific ones, add a `.rubocop.yml` file. Here's an [example](https://github.com/Vizzuality/emissions-scenario-portal/blob/develop/.rubocop.yml)
 - [Hound CI](https://houndci.com/configuration) can run the rubocop checks upon submitting a pull request through a github web hook. It supports other linters as well and the linters to be run are controlled via a `.hound.yml` file.
 - [Code Climate](https://codeclimate.com) is a static code analyser which can detect many code smells like code duplication and complex methods. In the paid version it can also detect common security vulnerabilities. Works via a webhook.
