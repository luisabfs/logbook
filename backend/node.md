## [TIP] Node.js Port: kill server

### For Linux/Mac OS search (sudo) run:

```
$ lsof -i tcp:<port>
$ kill -9 <PID>
```

### On Windows:

```
netstat -ano | findstr :<port>
tskill <PID> 
```

**Obs.:** run `tskill /?` for help | change `tskill` for `taskkill` in **Git Bash**

[Link 1](https://stackoverflow.com/a/45130296/9725247)
