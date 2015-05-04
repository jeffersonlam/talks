# Gitting More Out of Git
[Jordan Kasper (Strongloop)](http://jordankasper.com/)  
[Details](http://fluentconf.com/javascript-html-2015/public/schedule/detail/39088)  
[Slides](http://cdn.oreillystatic.com/en/assets/1/event/125/Gitting%20More%20Out%20of%20Git%20Presentation.pdf)  

Learn some tricks with Git to improve your daily workflow.  

## Notes

#### Branches and Remotes
`git branch -vv`  
Shows branches and remote branches  

`git remote -v`  

```
> git checkout -b new-feature
> git push -u origin new-feature
```
Create new branch and set upstream remote to that branch. The -u option sets the "upstream" remote repo to track.  

```
> git remote add (NAME) (URL)
> git remote -v
```
Add more remotes  

```
> git branch
> git branch --no-merge
```
Shows branches that haven't been merged into what they branched off of  


#### Diffs
`> git diff master stuff`  
Shows all differences now, between latest changes in master and changes in branch  

`> git diff master..stuff`  
If you add two periods, it shows differences the since when branch was created and the branch now  

`> git diff (commit hash) (commit hash)`  
Shows differences between two commits  


#### Git and Data Integrity
Git uses snapshots (versus file diffs)  
> "Every single commit is a single snapshot of every single thing in the repository at that time. Every space, every character, every line-break."
> "If anything changes, it knows that something is different."


#### Commit messages
You can ammend the previous commit message like so:  
```
git commit -m "This is teh best."
git comit --ammend -m "This is the best."
```

> "Git always only adds something. It is nearly impossible to remove something from git."

`> git log`
Show commit logs  
`> git reflog`
Show every single thing that you've done with Git  

If you forgot to add a file in a commit, add it in like so:  
```
git add forgotten.js
git commit --amend
```


#### "Atomic Commits"
> "Commits should be a unit of functionality."
> "You should be able to remove any commit and technically everything would be fine."


#### Undoing Changes
If you need to modify an older commit, everything that's built on top of that is also going to be affected.  
`git rebase --interactive HEAD^^^`  

`git revert`  
Undoes a commit  

`git reset`  
Resets your working/staging/remotes, depending on parameters  

`git reset --soft HEAD^`  
Resets staging. The caret says go back 1  

`git reset --mixed HEAD^`  
resets staging and working dir  

`git reset --hard HEAD^`  
resets staging, working, and remote  

What if you erased some work you needed?  
`git reflog`  
You can see the commit hash. The commit doesn't go away.  
`git reset --hard HEAD@{1}`  

`reflog` changes are only local.  


#### HEAD notation
- HEAD^
    - back 1 place
- HEAD^^
    - back 2 places
- HEAD~n
    - back n places
- HEAD@{i}
    - back to reflog index i


#### Stashes
> "When you change branches, anything that you were working on comes along for the ride."

`git stash --include-untracked`  
Stash your working files. This includes untracked files  

`git stash list`  
Show your stash  

`git stash apply`  
takes the top item in your stash. the 0 index  

`git stash pop`  
Applies the top item in your stash and removes it from the stash  


#### Logs
`git log --oneline`  
`git log --oneline --graph`  
`git log --no-merges`  
`git log --author="jakerella"`  


#### Pointing Blame
> Something's going wrong, and you want to determine who it is. Which it's usually yourself.

`git blame (filepath)`  
It'll show a line-by-line analysis of what commits changed what lines, who did it, and when.


#### Bisect
What if I don't know where/why/when things went wrong?  
`git bisect`  
Not a difficult tool to use, but  
> "If you don't use it, it goes away."

First, switch to a broken branch  
`git bisect start`  
`git bisect bad`  
`git bisect good (hash)`  
`git status`  
not currently on any branch. nothing to commit. (this is a detached state.)  
Remember, you're in a detached state so you won't be able to commit any changes. But, you can stash.  

#### Fast Forward
With no divergent changes, we can "fast forward"

```
git checkout master  
git merge feature  
    updating (commit)..(commit)  
fast forward  
```

No Fast Forward
```
git checkout master  
git merge feature --no-ff  
```
Because you lose branch-merge history with fast-forward!  


#### Conflicts
Who resolves conflicts? You do.  

```
common text...
<<<<<<< HEAD
text only in master
=======
same line, different text in branch
>>>>>>> feature
more common text...
```

1. Fix the conflict.
2. Save it
3. Stage the fixed file
    - git add (file)
4. Commit it
    - git commit (msg)
5. Remove the "orig"inal file from the branch...?
    - git rm README.orig.md

#### Rebasing
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
`git rebase --skip`
    probably a terrible idea
`git rebase --abort`
    abort the entire thing

"I don't always rebase, but when I do... I do it by default."

```
git pull --rebase
git config branch.master.rebase true
git config branch.some-other-branch.rebase true
git config branch.autosetuprebase always
```

> "If you're doing rebase, everyone should be doing rebase. If only one person is doing rebasing and everyone else is doing merges, you're all going to hate yourselves."

#### Cherry Picking
> "I need an individual commit. I have this old feature at the bottom and a new feature at the top. The old feature is dead, but that one commit has some choice changes in it."

Don't do a cherry pick if you're going to then merge in that old feature branch

## Action Items
- [ ] Review all the above, and utilize them regularly.
