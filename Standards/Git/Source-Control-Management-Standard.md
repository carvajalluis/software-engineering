[[_TOC_]]

## The Extent Of This Document

I’ll try to avoid talking about things already covered in many books and documentations as much as I can, but to cover the standard itself for our
team, some of this content will be directly copied from knowledgable sources.

Here you can find here all the required know-how and standards regarding Source Control Management (SCM) standards.

## Source Control Best Practices

[Please refer to this child document.](/Source-Control-Best-Practices)

## Repository Workflow

### Glossary
- A branch is a separate line of work.
- A public branch is one that more than one person pulls from.
- A topical branch (or feature branch) is a private branch that you alone are using, and will not be exposed in the public repository.
- A tracking branch is a local branch that knows where its remote is, and that can push to and pull from that remote.
### Git Feature Branch Workflow
The core idea behind the Feature Branch Workflow is that all feature development should take place in a dedicated branch instead of the master branch. This encapsulation makes it easy for multiple developers to work on a particular feature without disturbing the main codebase. It also means the master branch will never contain broken code, which is a huge advantage for continuous integration environments.

Encapsulating feature development also makes it possible to leverage pull requests, which are a way to initiate discussions around a branch. They give other developers the opportunity to sign off on a feature before it gets integrated into the official project. Or, if you get stuck in the middle of a feature, you can open a pull request asking for suggestions from your colleagues. The point is, pull requests make it incredibly easy for your team to comment on each other’s work.

to learn more into detail on how t works please refer to this [link](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow).

### Rebase workflow core
The fundamental idea of rebasing is that you make sure that your commits go on top of the "public" branch, that you "rebase" them so that instead of being related to some commit way back when you started working on this feature, they get reworked a little so they go on top of what's there now.

- Don't do your work on the public branch (Don't work on master or 6.x-1.x or whatever). Instead, work on a "topical" or "feature" branch, one that's devoted to what you want to do.
- When you're ready to commit something, you rebase onto the public branch, plopping your work onto the very tip of the public branch, as if it were a single patch you were applying.

```
1. git checkout 7.x-1.x  # Check out the "public" branch
2. git pull --rebase     # Get the latest version from remote
3. git checkout -b comment_broken_links_101026  # topical branch
4. ... # do stuff here... Make commits.. test...
5. git fetch origin      # Update your repository's origin/ branches from remote repo
6. git checkout 7.x-1.x  # Switch to the local tracking branch (repeat 6->11 every time you see new commits on public)
7. git pull --rebase
8. git checkout comment_broken_links_101026
9. git pull --rebase     # This won't result in a merge commit
10. git rebase 7.x-1.x.  # Plop our commits on top of everybody else's
11. git push -force      # Push the public branch back up, with my stuff on the top
```

At a high-level, the workflow can be described in a few steps:

1. Fetch upstream changes.
1. Create a branch.
1. Write code and commit to your branch as you go.
1. Fetch from upstream again (in case upstream master has had new commits since you started your branch).
1. Rebase and squash your branch against upstream/master, resolving any merge conflicts.
1. Push your branch.
1. Open a pull request.

## Commit message standard
We will adhere to [conventional commits](https://www.conventionalcommits.org/en/v1.0.0-beta.4/). it is
> A specification for adding human and machine-readable meaning to commit messages The Conventional Commits specification is a lightweight convention on top of commit messages. It provides an easy set of rules for creating an explicit commit history; which makes it easier to write automated tools on top of. This convention dovetails with SemVer, by describing the features, fixes, and breaking changes made in commit messages.
```
<type>[optional scope]: <description>

[optional body]

[optional footer]
```
, for example, commit message with the description and breaking change in the body:

```
feat: allow the provided config object to extend other configs

BREAKING CHANGE: `extends` key in config file is now used for extending

other config files
```

for more details regarding this message standard please refer to https://www.conventionalcommits.org

## Pull Requests

### How it works

The general process is as follows:

1. A developer creates the feature in a dedicated branch in their local repo.
1. The developer pushes the branch to a public repository.
1. The developer files a pull request via Azure DevOps.
1. Some of the other team members review the code, discuss it, and alters it.
1. The code merges automatically when all the checks have passed, adding the feature into the official repository and closes the pull
1. request.
### Code Reviews

We will have a tool that automatically checks for style, compilation, syntax or semantic errors leaving us with the more juicy ones to discuss: Logical Errors.

At least one team member, preferably the code owner( meaning the person that previously worked on a particular piece of work, and you will be pointed out by Azure repos), must review your code prior to enable it to complete the merge.

Everyone is encouraged to participate in code reviews. It is the Publisher of the PR responsibility to gather the checks for their code to pass and to facilitate the understandability of what, why and how of their changes. It also is the team member's responsibility to be attentive and respond in a timely manner to code reviews or to note they won't be able to attend the request soon enough.

### Principles

- Technical facts and data overrule opinions and personal preferences.
- On matters of style, the style guide is the absolute authority. Any pure style point (whitespace, etc.) that is not in the style guide is a matter of personal preference. The style should be consistent with what is there. If there is no previous style, accept the authors.
- Aspects of software design are almost never a pure style issue or just a personal preference. They are based on underlying principles and should be weighed on those principles, not simply by personal opinion. Sometimes there are a few valid options. If the author can demonstrate (either through data or based on solid engineering principles) that several approaches are equally valid, then the reviewer should accept the preference of the author. Otherwise, the choice is dictated by standard principles of software design.
- If no other rule applies, then the reviewer may ask the author to be consistent with what is in the current codebase, as long as that doesn’t worsen the overall code health of the system.

### Resolving Conflicts

In any conflict on a code review, the first step should always be for the developer and reviewer to try to come to a consensus, based on the contents of this document and the other documents in The CL Author’s Guide and this Reviewer Guide.

When coming to consensus becomes especially difficult, it can help to have a face-to-face meeting or a video conference between the reviewer and the author, instead of just trying to resolve the conflict through code review comments. (If you do this, though, make sure to record the results of the discussion as a comment on the CL, for future readers.)

If that doesn’t resolve the situation, the most common way to resolve it would be to escalate. Often the escalation path is to a broader team discussion, having a Technical Lead (currently invested in the Solution’s Architect weigh in, asking for a decision from Product Owner, trying to reduce the time to solve these conflicts without spawning a full forum unless required.

Don’t let a change list (CL) sit around because the author and the reviewer can’t come to an agreement.

### What to look for in a code review

In doing a code review, you should make sure that:


```
- The code is well-designed.
- The functionality is good for the users of the code.
- Any UI changes are sensible and look good.
- Any parallel programming ( like multithreading, throw-away jobs, or using parallel computing libraries like Plinq) is done safely.
- The code isn’t more complex than it needs to be.
- The developer isn’t implementing things they might need in the future but doesn’t know they need it now.
- The code has appropriate unit tests. ([TBD]: is it part of  practices )
- Tests are well-designed.
- The developer used clear names for everything.
- Comments are clear, useful and mostly explain why instead of what.
- The code is appropriately documented. [TODO: not clear yet documentation at the time of writing this document]
- The code conforms to our style guides.
```
### Foster a positive code review culture

Peer review can put a strain on interpersonal team relationships. It ́s difficult to have every piece of work critiqued by peers. Therefore, in order for peer code review to be successful, it ́s extremely important that we create a culture of collaboration and learning in peer review.

While it ́s easy to see defects as purely negative, each bug is actually an opportunity for the team to improve code quality. Peer review also allows junior team members to learn from senior leaders and for even the most experienced programmers to break bad habits.

### On Pull Request notes

It is hard to accommodate all the detailed scenarios and human interactions you can encounter in a pull request. Please refer to [google’s engineering practices documentation](https://google.github.io/eng-practices/) as a source of truth.


