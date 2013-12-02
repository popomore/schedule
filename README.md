# Timers

A tiny cron-like tools for humman, implement by Node.js

[![Build Status](https://travis-ci.org/popomore/timers.png?branch=master)](https://travis-ci.org/popomore/timers)
[![Coverage Status](https://coveralls.io/repos/popomore/timers/badge.png)](https://coveralls.io/r/popomore/timers)

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
