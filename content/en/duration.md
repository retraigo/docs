---
title: Duration
description: 'Convert milliseconds or human-readable strings into time units and vice versa.'
position: 6
category: Duration
menuTitle: Introduction
features:
  - Lightweight
  - TypeScript
  - No Dependencies
  - Customizable Formatting
---

Duration is a single Class written in TypeScript. It can infer units of time
from milliseconds and human-readable strings and output desired formatted
strings too.

### Properties

```js
Duration {
    raw: 0 // Original milliseconds passed to the constructor
    d: 0, // Days
    h: 0, // Hours
    m: 0, // Minutes
    s: 0, // Seconds
    ms: 0 // Milliseconds
    us: 0 // Microseconds
    ns: 0 // Nanoseconds
};
```

**No weeks/months/years?**

Nah they're a pain. How'd the code even know how many days are there in that month? I kept `days` as the last one coz it'll be easy to translate into weeks and years easily, while weeks-years wouldn't be as accurate.

## Features

<list :items="features"></list>
