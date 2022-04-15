---
title: Setup - Duration
description: "A guide towards setting up Duration in your existing project."
position: 7
category: Duration
menuTitle: Setup
---

## Installation

Import `duration` in your project.

```ts
import { Duration } from "https://deno.land/x/durationjs/mod.ts";
```

It is recommended to centre your dependencies around a `deps.ts` file for easier
management of dependencies.

<code-group>
<code-block label = "deps.ts" active>

```ts
export { Duration } from "https://deno.land/x/durationjs/mod.ts";
```

</code-block>
  <code-block label = "mod.ts">

```ts
import { Duration } from "./deps.ts";
```

</code-block>
</code-group>
