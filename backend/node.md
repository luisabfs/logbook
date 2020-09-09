## [TIP] Node.js Port: kill server

### For Linux/Mac OS search (sudo) run:

```
lsof -i tcp:<port>
kill -9 <PID>
```

### On Windows:

```
netstat -ano | findstr :<port>
tskill <PID> 
```

**Obs.:** run `tskill /?` for help | change `tskill` for `taskkill` in **Git Bash**

[Link 1](https://stackoverflow.com/a/45130296/9725247)

## [ERROR] Express.js req.body undefined

There was an UPDATE in July 2020 and `express.bodyParser()` is no longer bundled as part of **express**. 
So, we need to:

### 1. Install it separately before loading:

```
yarn add body-parser
```
### 2. Configure two middlewares BEFORE defining our routes:

```
const express = require('express');
const bodyParser = require('body-parser');

const app = express();

// parse application/x-www-form-urlencoded
app.use(bodyParser.urlencoded({ extended: false }));
// parse application/json
app.use(bodyParser.json())
```

[Link 1](https://stackoverflow.com/questions/9177049/express-js-req-body-undefined)
