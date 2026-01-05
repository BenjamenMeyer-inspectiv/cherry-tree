# cherry-tree
Learning Cherry-Picking

This is a little tool to walk through the concept of cherry picking with git.

Each branch will create a description of a type of Cherry Tree.
All aspects use for the descriptions are part of the `aspects` branch.
You can use `git log aspects` to review the commits.

## Notes

- Be careful to pay attention to the logs and ordering. Cherry picking commits requires attention to detail or the commit will not apply correctly.
- While this repositories has all the necessary commits in a branch, the only requirement by git is that the commit be in the `reflog` (reference log).
  That is - when no branch references a commit it is still kept in the history data until git performs its cleanup operations; git still knows about
  the changes during that time and so long as git knows about the commit it the cherry-pick operation can be used to pull the commits into a branch.
- Commits might get lost this way due to rebasing, squashing, branch deletions, and more. The `git reflog` command can be used to find commits.

## Commands

Remember that `git help <command>` can be used to get help information on a command at any time.

### Branches
You already likely know how to move between branches:
```
$ git checkout branch-name
```
or creating a new branch with:
```
$ git checkout -b branch-name
```

For these tasks you should not need to create *new* branches, just checkout existing branches.

### Log Data

Log data can be retrieved with `git log`.

### Commit Data

Reference log data can be retrieved using `git reflog`.

The `git rev-list` command can also be useful. While this provides a simpler list of commit data, you will likely want to 
pair it with the `git show -p <commit>` command to see the changes.

### Cherry-picking

Cherry picking is done using using `git cherry-pick <commit hash>`.
More than one commit hash can be given at a time.

## Tasks

1. Please fork this repository into your own github profile.
2. See the `INSTRUCTIONS.md` file in each branch for what to do.
3. Enjoy!
