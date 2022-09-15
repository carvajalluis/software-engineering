Please refer to the source for more detailed information. This document distills the best practices to those best suited to a corporate professional
environment, in my experience.
[[_TOC_]]
## Do read about git

Knowing where to look is half the battle. I strongly urge everyone to read (and support) the Pro Git book. The other resources are highly
recommended by various people as well.

- [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials)
- [Pro Git](https://git-scm.com/book/en/v2)
- [Git for Computer Scientists](https://eagain.net/articles/git-for-computer-scientists/) 
- [Git from the Bottom Up](https://jwiegley.github.io/git-from-the-bottom-up/)
- [The Git Parable](https://tom.preston-werner.com/2009/05/19/the-git-parable.html)
- [Other resources](https://git-scm.com/doc)
- [Git wiki](https://git.wiki.kernel.org/index.php/Main_Page)

## Learn more than the basics of Git SCM

there comes the time when you will be required to find a bug in history, do some repository BI for the team administrators, recover some lost code, kt someone else on your software or resolve recursive conflicts. those skills will come handy.

## Commit related changes

A commit should be a wrapper for related changes. Small commits make it easier for other team members to understand the changes and roll them back if something went wrong. With tools like the staging area and the ability to stage only parts of a file, Git makes it easy to create very granular commits.

## Commit often

Committing often keeps your commits small and, again, helps you commit only related changes. Moreover, it allows you to share your code more frequently with others. That way it’s easier for everyone to integrate changes regularly and avoid having merge conflicts. Having a few large commits and sharing them rarely, in contrast, makes it hard both to solve conflicts and to comprehend what happened.

## Don’t commit half-done work

You should only commit code when it’s completed. This doesn’t mean you have to complete a whole, large feature before committing. Quite the contrary: split the feature’s implementation into logical chunks and remember to commit early and often. But don’t commit just to have something in the repository before leaving the office at the end of the day. If you’re tempted to commit just because you need a clean working copy (to check out a branch, pull in changes, etc.) consider using Git’s “Stash” feature instead.

## Test before you commit

Resist the temptation to commit something that you “think” is completed. Test it thoroughly to make sure it really is completed and has no side effects (as far as one can tell). While committing half-baked things in your local repository only requires you to forgive yourself, having your code tested is even more important when it comes to pushing/sharing your code with others.

## Write good commit messages

Begin your message with a short summary of your changes (up to 50 characters as a guideline). Separate it from the following body by including a blank line. The body of your message should provide detailed answers to the following questions: What was the motivation for the change? How does it differ from the previous implementation? Use the imperative, present tense (“change“, not “changed“ or “changes“) to be consistent with generated messages from commands like git merge. more detail on that with the conventional commits

## Version control is not a backup system

Having your files backed up on a remote server is a nice side effect of having a version control system. But you should not use your VCS like it was a backup system. When doing version control, you should pay attention to committing semantically (see “related changes”) – you shouldn’t just cram in files.

## Use branches

Branching is one of Git’s most powerful features – and this is not by accident: quick and easy branching was a central requirement from day one. Branches are the perfect tool to help you avoid mixing up different lines of development. You should use branches extensively in your development workflows: for new features, bug fixes, experiments, ideas...

## Don't panic

As long as you have committed your work (or in many cases even added it with git add) your work will not be lost for at least two weeks unless you really work at it (run commands that manually purge it).

See on undoing, fixing, or removing commits in git if you want to fix a particular problematic commit or commits, as opposed to attempting to locate lost data. When attempting to find your lost commits, first make sure you will not lose any current work.

## Don’t change shared history

Once you merge/rebase (terms defined in the git tutorials) a pull request to a public branch to the authoritative upstream repository, making the commits or tags publicly visible, you should ideally consider those commits etched in diamond for all eternity. If you later find out that you messed up, make new commits that fix the problems (possibly by revert, possibly by patching, etc).

## Do divide work into repositories

Repositories sometimes get used to store things that they should not, simply because they were there. Try to avoid doing so.

- One conceptual group per repository. Does this mean one per product, program, library, class? the team must decide.
- Read access control is at the repo level
- Separate repositories for files that might be needed by multiple projects. This promotes sharing and code reuse and is highly recommended.
- Use Git LFS for handling large files in different storage than your repository to avoid repository speed issues.

## Hide the sausage-making

A good reason to hide the sausage-making[¹](https://sethrobertson.github.io/GitBestPractices/#sausage_metaphor) is if you feel you may be cherry-picking commits a lot (though this too is often a sign of bad workflow).

Another good reason is to ensure each commit compiles and/or passes regression tests, and represents a different easily understood concepts. The former allows git-bisect to choose any commit and have a good chance of that commit doing something useful. Proponents claim it is all about leaving a history others can later use to understand why the code became the way it is now, to make it less likely for others to break it.![image.png](/.attachments/image-da2924ac-77a6-4dfa-a0c9-3dae778971c2.png)


## Do keep up to date

- Pulling with rebase:
   Whenever I pull, under most circumstances I git pull --rebase. This is because I like to see a linear history (my commit came after all commits that were pushed before it, instead of being developed in parallel). It makes history visualization much simpler and git bisect easier to see and understand.

- Rebasing:
   Whenever I have a private branch that I want to update, I use rebase (for the same reasons as above). History is clean and simple. However, if you share this branch with other people, rebasing is rewriting public history and must be avoided. You may only rebase commits that no-one else has seen (which is why git pull --rebase is safe).