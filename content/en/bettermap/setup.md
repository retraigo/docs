---
title: Setup
description: "A guide towards setting up bettermap in your project."
position: 14
category: BetterMap
---

## Installation

Import `BetterMap` in your project.

```ts
import { BetterMap } from "https://deno.land/x/bettermap/mod.ts";

const b = new BetterMap<string, unknown>();
```

It is recommended to centre your dependencies around a `deps.ts` file for easier
management of dependencies.

<code-group>
<code-block label = "deps.ts" active>

```ts
export { BetterMap } from "https://deno.land/x/bettermap/mod.ts";
```

</code-block>
  <code-block label = "mod.ts">

```ts
import { BetterMap } from "./deps.ts";
```

</code-block>
</code-group>
