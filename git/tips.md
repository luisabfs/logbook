
## [TIP] Delete local and remote branch

### Local branch 

```git branch -d <local_branch>```: the `-d` flag tells Git to delete the branch passed in the argument. 

```git branch -D <local_branch>```: the `-D` flag forces the deletion (i.e. `--delete --force`). 

### Remote branch

```git push <remote_repo> --delete <remote_branch>```

Once the branch is deleted from the remote repository, other machines involved in the project must be locally updated as well. It can be done by running the command:

```git fetch --all --prune```

The `--prune` flag tells Git to remove all remote references (our branches) that no longer exist in the remote repository. When it comes to *flags*, we can use `--prune-tags`.
