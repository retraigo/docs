---
title: Setup - Duration
description: "A guide towards setting up Duration in your existing project."
position: 7
category: Duration
menuTitle: Setup
---

## Installation

Import `duration` in your project.

<code-group>
<code-block label = "deno" active>

```ts
import { Duration } from "https://deno.land/x/durationjs/mod.ts";
```

</code-block>
  <code-block label = "node">

```ts
import { Duration } from "@retraigo/duration.js";
```

</code-block>
</code-group>

For deno, it is recommended to centre your dependencies around a `deps.ts` file
for easier management of dependencies.

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
