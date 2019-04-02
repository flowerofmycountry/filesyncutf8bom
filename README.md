# filesyncutf8bom
a appender for [log4js-node](https://github.com/log4js-node/log4js-node).
same as the core appender filesync, but encoding is utf8 with bom.

## installation

```bash
npm install filesyncutf8bom
```

## usage

```javascript
var log4js = require('log4js');

log4js.configure({
    appenders: {
        cheese: {
            type: 'filesyncutf8bom',
            filename: 'cheese.csv'),
            layout: {
                type: 'pattern',
                pattern: '%d{yyyy-MM-dd hh:mm:ss}\t%p\t%m'
            }
        }
    },
    categories: {
        default: { appenders: ['cheese'], level: "debug" }
    }
});

var logger = log4js.getLogger();
logger.level = 'debug';
logger.debug("Some debug messages");
```

## License
The original log4js was distributed under the Apache 2.0 License, and so is this. I've tried to keep the original copyright and author credits in place, except in sections that I have rewritten extensively.
