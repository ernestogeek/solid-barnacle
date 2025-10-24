<div align="center">


0 dependencies event-loop blocking synchronous sleep

sleep + sync = slync

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
- **slync** will determine which sleep method to use (atomic vs naive) at runtime

For synchronous non-blocking sleep, look into [deasync](https://github.com/abbr/deasync).
