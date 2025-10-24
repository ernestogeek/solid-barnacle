# 💤 solid-barnacle

### 0️⃣ Dependencies • 🌀 Event-loop Blocking • 🕒 Synchronous Sleep

---

**sleep + sync = slync**

[![npm version](https://img.shields.io/npm/v/slync.svg?style=flat-square&color=blue)](https://www.npmjs.com/package/slync)
[![npm downloads](https://img.shields.io/npm/dt/slync.svg?style=flat-square&color=success)](https://www.npmjs.com/package/slync)
[![License](https://img.shields.io/github/license/nktnet1/slync?style=flat-square&color=orange)](./LICENSE)
[![Made with TypeScript](https://img.shields.io/badge/Made%20with-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org)

---

## 🚀 Installation

```bash
npm install slync
```

Or using pnpm:

```bash
pnpm add slync
```

---

## 🧠 Usage

Try instantly on **[Replit →](https://replit.com/@nktnet1/slync-example#index.js)**

```javascript
slync(ms) // where ms is the number of milliseconds
```

### Example — Synchronously sleeping for 2 seconds

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

---

## ⚙️ Limitations

There are currently **no known limitations**.

---

## ⚠️ Caveats

**slync** is modeled after [atomic-sleep](https://github.com/davidmarkclements/atomic-sleep), with a few improvements:

- 🧩 **Written in [TypeScript](https://www.typescriptlang.org)**
- ⚙️ **Auto-selects** the best sleep method (atomic vs naive) at runtime

> 💡 For synchronous *non-blocking* sleep, check out [deasync](https://github.com/abbr/deasync).

---

## 🧪 Example Environments

| Platform | Status |
|-----------|---------|
| Node.js | ✅ Supported |
| Deno | ⚠️ Not tested |
| Browser | ❌ Not supported |

---

<div align="center">

### 🧰 Built with ❤️ using TypeScript

[![Code Style: Prettier](https://img.shields.io/badge/Code_Style-Prettier-ff69b4?style=flat-square&logo=prettier&logoColor=white)](https://prettier.io/)
[![Open Source](https://img.shields.io/badge/Open%20Source-💖-purple?style=flat-square)](https://github.com/nktnet1/slync)

---

**Fast. Simple. Synchronous.**

</div>
