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
