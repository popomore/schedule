# Timers

A tiny cron-like tools for humman, implement by Node.js

---

## Install

```
$ npm install timers
```

## Usage

```
var every = require('timers').every;
every('2s').do(function() {
  // do your job 
});
```

You can stop interval when some exception

```
var every = require('timers').every;
var ins = every('2 seconds').do(cb);

process.on('uncaughtException', function() {
  ins.stop();
})
```

## Format

- ms, millisecond, milliseconds
- s, second, seconds
- m, minite, minites
- h, hour, hours
- d, day, days

## Lisence

MIT
