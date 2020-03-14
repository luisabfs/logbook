## [ERROR] GPG Key: *failed to sign the data*

```
error: cannot run --add: No such file or directory
error: gpg failed to sign the data
fatal: failed to write commit object
```

### Resolution

1. **brew install gpg2**: installing the newest version of *gpg*
2. **echo "test" | gpg2 --clearsign**: to be sure that *gpg2* is working
3. **git config --global --unset-all gpg.program**: remove the wrong directory associated to *gpg.program* settings
4. **gpgconf --kill gpg-agent**: killing any agent that may be running

[Link 1](https://git-scm.com/docs/git-config/2.1.4) | [Link 2](https://stackoverflow.com/questions/41052538/git-error-gpg-failed-to-sign-data/41054093)

## [ERROR] Git push: *failed to push some refs*

```
![rejected] master -> master (fetch first)
error: failed to push some refs to <repository>
hint: Updates were rejected because the remote contains work that you do not have locally. 
This is usually caused by another repository pushing to the same ref. 
You may want to first integrate the remote changes(e.g., 'git pull ...') before pushing again.
```
Translating the error message above, the **remote** directory had updates the **local** didn't, which means they weren't in sync.

### Resolution

**New project**
```
git pull origin master --allow-unrelated-histories
```

This resulted in the following response: `All conflicts fixed but you are still merging.(use "git commit" to conclude merge)`. Then, I did `git commit` and `git push origin master`.

**Project that contain changes you would like to keep**

Instead of using -f or --force, you should use:

```
git push --force-with-lease
```
Why? Because it checks the remote branch for changes which is absolutely a good idea. Let's imagine that James and Lisa are working on the same feature branch and Lisa has pushed a commit. James now rebases his local branch and is rejected when trying to push. Of course James thinks this is due to rebase and uses --force and would rewrite all Lisa's changes. If James had used --force-with-lease he would have received a warning that there are commits done by someone else. I don't see why anyone would use --force instead of --force-with-lease when pushing after a rebase.

[Link 1](https://hiperbytes.com.br/erros-e-solucoes/erro-git-push-error-failed-to-push-some-refs/) | [Link 2](https://stackoverflow.com/a/37460330)


