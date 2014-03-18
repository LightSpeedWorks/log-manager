# log-manager.js

# LogManager {ログ管理}

```js
var LogManager = require('log-manager');
var log = LogManager.getLogger();

var log = LogManager.getLogger('className1');

var log = require('log-manager').getLogger();

log.trace(msg, arg1, arg2, ...);
log.debug(msg, arg1, arg2, ...);
log.info(msg, arg1, arg2, ...);
log.warn(msg, arg1, arg2, ...);
log.error(msg, arg1, arg2, ...);
log.fatal(msg, arg1, arg2, ...);

LogManager.setLevel('TRACE'); // all
LogManager.setLevel('DEBUG');
LogManager.setLevel('INFO'); // default
LogManager.setLevel('WARN');
LogManager.setLevel('ERROR');
LogManager.setLevel('FATAL'); // FATAL only

var mgr = new LogManager();
mgr.setLevel('DEBUG');
var log = mgr.getLogger();
log.setLevel('WARN');
```
