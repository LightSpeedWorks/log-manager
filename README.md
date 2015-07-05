# log-manager.js

# LogManager {ログ管理}


## INSTALL:

[![NPM](https://nodei.co/npm/log-manager.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/log-manager/)
[![NPM](https://nodei.co/npm-dl/log-manager.png?height=2)](https://nodei.co/npm/log-manager/)


## EXAMPLES:

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


## LogManager and LogWriter

```js
var LogManager = require('log-manager');
var LogWriter = require('log-writer');

LogManager.setWriter(new LogWriter('log-manager-ex-%s.log'));
var log = LogManager.getLogger();

log.trace('test trace %s %d', 'arg1', 2);
log.debug('test debug %s %d', 'arg1', 2);
log.info('test info  %s %d', 'arg1', 2);
log.warn('test warn  %s %d', 'arg1', 2);
log.error('test error %s %d', 'arg1', 2);
log.fatal('test fatal %s %d', 'arg1', 2);
```
