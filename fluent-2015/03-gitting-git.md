# Gitting More Out of Git
@jakerella

## Notes
> git branch -vv
> git remote -v

Tracking
    > git checkout -b new-feature
    > git push -u origin new-feature

The -u option sets the "upstream" remote repo to track

Other Remotes
    what about other repos? How is this distributed?
        > git remote add (NAME) (URL)
        > git remote -v

More Branches
    > git branch
    > git branch --no-merge
        shows branches that haven't been merged into what they branched off of
    
    > git diff master stuff
        shows all differences now, between latest changes in master and changes in branch
    > git diff master..stuff
        shows differences since when branch was created and changes made in branch
    > git diff (commit byte) (commit byte)

Git and Data Integrity
    Git uses snapshots (versus file diffs)
    "Every single commit is a single snapshot of every single thing in the repository at that time."
        every space
        every character
        every line-break
    "If anything changes, it knows that something is different."
    commit byte = hash. created with SHA1 hashing algorithm

Fixing commit messages
    > git commit -m "This is teh best."
    > git comit --ammend -m "This is the best."

    > git log
    "Git always only adds something. It is nearly impossible to remove something from git."
    > git reflog

What if I forgot a file?
    git add forgotten.js
    git commit --amend

The concept of an atomic commit
    "You can remove any commit and technically everything would be fine."
    Commits should be a unit of functionality.

What if I need to modify an older commit?
    Everything that's built on top of that is also going to be affected.
    You'll need to use `git rebase --interactive`

> git rebase --interactive HEAD^^^

Undoing Changes
> git reset
> git revert

> git reset --soft HEAD^
    the caret says go back 1
    resets staging

> git reset --mixed HEAD^
    resets staging and working dir

> git reset --hard HEAD^
    resets staging, working, and remote

What if you erased some work you needed?
> git reflog
    You can see the commit hash. The commit doesn't go away. 

> git reset --hard HEAD@{1}

Head notation
    HEAD^
        back 1 place
    HEAD^^
        back 2 places
    HEAD~n
        back n places
    HEAD@{i}
        back to reflog index i

the reflog changes are only local.


Stashes
"When you change branches, anything that you were working on comes along for the ride."
> git stash --include-untracked
    this includes untracked files
> git stash list

Recommendation: Don't use commit as a way to save your work. Use it as atomized pieces of work.
> git stash apply
    takes the top item in your stash. the 0 index

> git stash pop
    applies the top item in your stash and removes it from the stash


Logs
> git log --oneline
> git log --oneline --graph
> git log --no-merges
> git log --author="jakerella"


Pointing Blame
    something's going wrong, and you want to determine who it is. Which it's usually yourself.

> git blame (filepath)
    It'll show a line-by-line analysis of what commits changed what lines, who did it, and when.


What if I don't know where/why/when things went wrong?
    > git bisect
    Not a difficult tool to use, but "If you don't use it, it goes away."

First, switch to a broken branch
> git bisect start
> git bisect bad
> git bisect good (hash)
> git status
    not currently on any branch. nothing to commit. (this is a detached state.)

remember you're in a detached state so you won't be able to commit any changes. but, you can stash.

Fast Forward
with no divergent changes, we can "fast forward"
    > git checkout master
    > git merge feature
        updating (commit)..(commit)
    fast forward

No Fast Forward
    > git checkout master
    > git merge feature --no-ff
        because you lose branch-merge history with fast-forward!

Divergent Changes
    > git checkout master
    > git merge feature

Conflicts
    Who resolves conflicts? You do.

common text...

<<<<<<< HEAD
text only in master
=======
same line, different text in branch
>>>>>>> feature

more common text...

1. Fix the conflict.
2. Save it
3. Stage the fixed file
    git add (file)
4. Commit it
    git commit (msg)
5. Remove the "orig"inal file from the branch...?
    git rm README.orig.md

Rebasing on Master
    > git checkout feature
    > git rebase master

You can still get conflicts with Rebase!
> git rebase master
    says something about error patching

    1. fix the conflict in the file
    2. stage it
    3. > git rebase --continue

Too many conflicts?
> git rebase --skip
    probably a terrible idea
> git rebase --abort
    abort the entire thing

"I don't always rebase, but when I do... I do it by default."
> git pull --rebase

> git config branch.master.rebase true
> git config branch.some-other-branch.rebase true
>
> git config branch.autosetuprebase always

if you're doing rebase, everyone should be doing rebase. if only one person is doing rebasing and everyone else is doing merges, you're all going to hate yourselves.

Cherry Picking
"I need an individual commit. I have this old feature at the bottom and a new feature at the top. The old feature is dead, but that one commit has some choice changes in it."
- don't do a cherry pick if you're going to then merge in that old feature branch

## Action Items
