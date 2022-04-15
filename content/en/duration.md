---
title: Introduction
description: 'Convert milliseconds or human-readable strings into time units and vice versa.'
position: 6
category: Duration
features:
  - Lightweight
  - Typescript
  - No Dependencies
  - Customizable Formatting
---

Duration is a single Class written in Typescript. It can infer units of time
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

## Features

<list :items="features"></list>
