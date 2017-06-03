[![NPM](https://nodei.co/npm/krtp.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/krtp/)

[![Travis branch](https://img.shields.io/travis/1995parham/krtp/master.svg?style=flat-square)](https://travis-ci.org/1995parham/krtp)
[![GitHub stars](https://img.shields.io/github/stars/1995parham/krtp.svg?style=flat-square)](https://github.com/1995parham/krtp/stargazers)
[![npm](https://img.shields.io/npm/v/krtp.svg?style=flat-square)]()

# KRTP

- [Introduction](#introduction)
- [Example](#example)
- [Protocol Documentation](https://github.com/1995parham/krtp/blob/master/docs/RTP.md)

## Introduction
RealTime Protocol implementation based on [RFC 3550](https://tools.ietf.org/html/rfc3550) in NodeJS.

## Example
```javascript
const RTPSession = require('krtp').RTPSession;

const s = new RTPSession(1373);

s.on('message', (msg) => {
  console.log(msg);
  s.close();
});

s.send(Buffer.from('Hello world'));
```
