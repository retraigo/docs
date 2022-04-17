---
title: Lala - Usage
menuTitle: Usage
description: "Guide to usage of Lala."
position: 12
category: Lala
---

<!-- STRING -->

## Generate String

### Format
```ts
generateString(length: number)
```

### Returns
An alphanumeric string.

### Example
```ts
import { generateString } from "xxx" // xxx being wherever you import lala from

generateString(10) // 203ewDHWCZ

// or 

import lala from "xxx"

lala.generateString(10) // 5yecgVNVou
```


<!-- NAME -->


## Generate Name

### Format
```ts
generateName(length: number)
```

### Returns
An uppercase name you can probably pronounce.

### Example
```ts
import { generateName } from "xxx" // xxx being wherever you import lala from

generateName(10) // FIAODILEVA

// or 

import lala from "xxx"

lala.generateName(10) // WOEVRUXEGR
```