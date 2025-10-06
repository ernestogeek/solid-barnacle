<div align="center">

# [![Slync](logo.svg)](https://github.com/nktnet1/slync)

[![pipeline](https://github.com/nktnet1/slync/actions/workflows/pipeline.yml/badge.svg)](https://github.com/nktnet1/slync/actions/workflows/pipeline.yml)
&nbsp;
[![codecov](https://codecov.io/gh/nktnet1/slync/branch/main/graph/badge.svg?token=RAC7SKJTGU)](https://codecov.io/gh/nktnet1/slync)
&nbsp;
[![Maintainability](https://api.codeclimate.com/v1/badges/1ae83ff4c0c0c8fc4a17/maintainability)](https://codeclimate.com/github/nktnet1/slync/maintainability)
&nbsp;
[![Snyk Security](https://snyk.io/test/github/nktnet1/slync/badge.svg)](https://snyk.io/test/github/nktnet1/slync)
&nbsp;
[![GitHub top language](https://img.shields.io/github/languages/top/nktnet1/slync)](https://github.com/search?q=repo%3Anktnet1%2Fslync++language%3ATypeScript&type=code)

[![NPM Version](https://img.shields.io/npm/v/slync?logo=npm)](https://www.npmjs.com/package/slync?activeTab=versions)
&nbsp;
[![install size](https://packagephobia.com/badge?p=slync)](https://packagephobia.com/result?p=slync)
&nbsp;
[![Depfu Dependencies](https://badges.depfu.com/badges/6c4074c4d23ad57ee2bfd9ff90456090/overview.svg)](https://depfu.com/github/nktnet1/slync?project_id=39032)
&nbsp;

[![GitHub issues](https://img.shields.io/github/issues/nktnet1/slync.svg?style=social)](https://github.com/nktnet1/slync/issues)

[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=nktnet1_slync&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=nktnet1_slync)
&nbsp;
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/af0385991c474ca692e8c7f85321e26a)](https://app.codacy.com/gh/nktnet1/slync/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade)
&nbsp;
[![DeepSource](https://app.deepsource.com/gh/nktnet1/slync.svg/?label=active+issues&show_trend=true&token=r1frerF1-N2Mhrc7ZXIC1uNa)](https://app.deepsource.com/gh/nktnet1/slync/)
&nbsp;
[![codebeat badge](https://codebeat.co/badges/5f4be12d-b0fd-4aab-92e9-5d70999ee489)](https://codebeat.co/projects/github-com-nktnet1-slync-main)
&nbsp;
[![GitHub stars](https://img.shields.io/github/stars/nktnet1/slync.svg?style=social)](https://github.com/nktnet1/slync/stargazers)

[![Downloads Total](https://badgen.net/npm/dt/slync)](https://moiva.io/?npm=slync)
&nbsp;
[![Downloads Yearly](https://badgen.net/npm/dy/slync)](https://moiva.io/?npm=slync)
&nbsp;
[![Downloads Monthly](https://badgen.net/npm/dm/slync)](https://moiva.io/?npm=slync)
&nbsp;
[![Downloads Weekly](https://badgen.net/npm/dw/slync)](https://moiva.io/?npm=slync)
&nbsp;
[![Downloads Daily](https://badgen.net/npm/dd/slync)](https://moiva.io/?npm=slync) 

---

0 dependencies event-loop blocking synchronous sleep

sleep + sync = slync

modelled after [atomic-sleep](https://github.com/davidmarkclements/atomic-sleep)

[![Try with Replit](https://replit.com/badge?caption=Try%20with%20Replit)](https://replit.com/@nktnet1/slync-example#index.js)

</div>

---

- [1. Installation](#1-installation)
- [2. Usage](#2-usage)
- [3. License](#3-license)
- [4. Limitations](#4-limitations)
- [5. Caveats](#5-caveats)

## 1. Installation

```
npm install slync
```

## 2. Usage

Try with [Replit](https://replit.com/@nktnet1/slync-example#index.js).

```javascript
slync(ms) // where ms is the number of milliseconds
```

Example usage of synchronously sleeping for 2 seconds:
```javascript
// import slync from 'slync';
const slync = require('slync');

console.log(`0. Current time: ${new Date()}`);

setTimeout(() => {
  console.log(`2. Prints second because slync blocks: ${new Date()}`);
}, 100);

slync(2000);

console.log(`1. Prints first after 2000 milliseconds: ${new Date()}`);
```


## 3. Limitations

There are currently no known limitations.

## 4. Caveats

**slync** is modelled after [atomic-sleep](https://github.com/davidmarkclements/atomic-sleep), with some minor differences:
- **slync** is written in [TypeScript](https://www.typescriptlang.org)
- **slync** only accepts 'number' for the ms parameter whereas [atomic-sleep](https://github.com/davidmarkclements/atomic-sleep) also accepts 'bigint'
- **slync** will determine which sleep method to use (atomic vs naive) at runtime

For synchronous non-blocking sleep, look into [deasync](https://github.com/abbr/deasync).
