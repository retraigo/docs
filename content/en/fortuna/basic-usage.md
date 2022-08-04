---
title: Basic Usage
description: "Basic usage of fortuna to create a weighted gacha system."
position: 4
category: Fortuna
---

You shouldn't need to read beyond this page in most cases since simple random weighted selection is mostly enough for stuff.

## Simple Weighted Selection

```ts
const items = [
    { result: "SSR cool character", chance: 1 },
    { result: "Kinda rare character", chance: 3 },
    { result: "Mob character", chance: 5 },
    { result: "Mob character", chance: 5 },
    { result: "Mob character", chance: 5 },
];

GachaMachine.roll(items); // Rolls one item from the list of items.
```

You can speed up the rolling by supplying the total weight of the data (sum of all chances/weights).

```ts
GachaMachine.roll(items, 19); // Rolls one item from the list of items, faster.
```

## Using other available algorithms

There is no reason to use any other available algorithm for random weighted selection but if you do need one, you can make use of the `algorithms` directory.

```ts
import { roll } from "https://deno.land/x/fortuna@v1.2.3/algorithms/v1.ts";

const items = [
    { result: "SSR cool character", chance: 1 },
    { result: "Kinda rare character", chance: 3 },
    { result: "Mob character", chance: 5 },
    { result: "Mob character", chance: 5 },
    { result: "Mob character", chance: 5 },
];

roll(items); // Rolls one item from the list of items but much slower.
```

You can compare the execution speed of algorithms by cloning the repo and using `deno task bench`.

| Algorithm | 10 Rolls | 100k Rolls |
| --------- | -------- | ---------- |
| v1        | 1.29 ms  | 12.99 s    |
| v2        | 78.34 µs | 763.47 ms  |
| v3        | 24.59 µs | 245.98 ms  |
| v4_sub    | 24.5 µs  | 240.8 ms   |
| v4        | 22.86 µs | 228.56 ms  |
