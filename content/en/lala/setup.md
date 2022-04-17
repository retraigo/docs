---
title: Setup
description: "A guide towards setting up lala in your existing project."
position: 11
category: Lala
---


## Installation

Import `lala` in your project.

<code-group>
<code-block label = "deno" active>

```ts
import lala from "https://deno.land/x/lala/mod.ts";
```

</code-block>
  <code-block label = "node">

```ts
import lala from "@nekooftheabyss/lala";
```

</code-block>
</code-group>

For deno, it is recommended to centre your dependencies around a `deps.ts` file
for easier management of dependencies.

<code-group>
<code-block label = "deps.ts" active>

```ts
export { default as lala } from "https://deno.land/x/lala/mod.ts";
```

</code-block>
  <code-block label = "mod.ts">

```ts
import { lala } from "./deps.ts";
```

</code-block>
</code-group>