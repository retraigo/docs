---
title: Formatting - Duration
description: "Methods to format a duration into a string."
position: 9
category: Duration
menuTitle: Formatting
---

## Get formatted duration


```ts
const myDuration = new Duration(165684)
```

While such an object is quite neat for developers, it would be a pain when users see the same. There are methods for converting the any duration instance into a human-readable string.

### The DD:HH:MM:SS format

The `toTimeString` method outputs a string in that format. Quite nice for timers and stuff.
```ts
myDuration.toTimeString();
// `00:00:02:45:684`
```

**What if I don't want all of that? I just want a MM:SS timer!**

Ok sure. You can pass `from` and `to` parameters to the method to just get the duration between those two.
```ts
myDuration.toTimeString("m", "s");
// `02:45`
```

<alert type = "info">The `toString` method uses `toTimeString` to generate a `DD:HH:MM:SS`-like string.</alert>

### The word format

The `toWordString` and `toDescriptiveString` methods output a string in that format. Quite nice for normal text that ain't timers and stuff.
```ts
myDuration.toDescriptiveString();
// `0 days, 0 hours, 2 minutes, 45 seconds, 684 milliseconds, 0 microseconds, 0 nanoseconds`

myDuration.toWordString();
// `zero days, zero hours, two minutes, forty five seconds, six hundred and eighty four milliseconds, zero microseconds, zero nanoseconds`
```

You can provide specific units if you don't want all units.
```ts
myDuration.toDescriptiveString(["s", "h"]);
// `0 hours, 45 seconds`
```

Still too long? Fortunately, there's another method to generate a short string, `toShortString`!
```ts
myDuration.toShortString(["s", "h"]);
// `0h 45s`
```