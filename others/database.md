## [ERROR] Can't start Postgres on Mac M1
_FATAL ERROR lock file "postmaster.pid" already exists_

Just remove the file `postmaster.pid` at path `/opt/homebrew/var/postgresql@VERSION/postmaster.pid`

[Link](https://stackoverflow.com/a/68080130)
