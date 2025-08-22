
![[Fixing Git Commit message.png]]

So we want to modify `Aka daniels commit 1-1` to have only 
`Aka daniels commit 1`.

However, we have one commit already in front of it ... `stanos ...` both are located in origin.

What now?

Interactive rebase:
https://www.baeldung.com/ops/git-commit-message-changes

```shell
git rebase -i HEAD~2
```

![[Fixing Git Commit message - rebase.png]]

Changing my to reword

![[Fixing Git Commit message - reword.png]]
Now close it. You will get another windown, with possibility to change it.

![[Fixing Git Commit message  - changing naming.png]]


After saving will se changes to git structure
![[Fixing Git Commit message - flow change.png]]

As you can see the hashes will be changed .. that is expected -> Rebasing
What is left to push it with force

`git push --force` and you get this:

![[./Fixing Git Commit message - push.png]]
