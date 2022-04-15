---
title: Basic Usage - Duration
description: "Basic usage of fortuna to create a weighted gacha system."
position: 8
category: Duration
menuTitle: Basic Usage
---

```ts
new Duration(milliseconds);
```

The `milliseconds` parameter can be any valid `number`. Microseconds and
Nanoseconds are supported as long as they come after the decimal point (like
from `performance.now()`).

## Get the duration since midnight

```ts
new Duration(); // Get duration since midnight
```

This returns the amount of time passed since `00:00:00` that day. Can be used
for getting the current time too.

## Manually set the duration

Sometimes you do not have the milliseconds ready. But you got the right duration
in mind. Fortunately, the `Duration` class supports the reverse action too.

```ts
const myDuration = new Duration(0); // Initialize a 0 duration

myDuration.setHours(10); // Set the hours of the duration to 10

myDuration.setMicroseconds(34344334); // Set the microseconds of the duration to 34,344,334

myDuration.addMinutes(10); // Add 10 minutes to the duration

myDuration.setMinutes(100); // Overwrite the minutes to 100

console.log(myDuration);

/*
    Duration { 
        raw: 42034344.334, 
        d: 0, 
        h: 11, 
        m: 40, 
        s: 34, 
        ms: 344, 
        us: 334, 
        ns: 0 
    };
*/
```
<alert type = "warning">It is recommended to avoid using `setHours` and similar methods since they may result in unexpected behavior. It is better to use `addHours` and similar methods.</alert>

## Get formatted duration


```ts
const myDuration = new Duration(165684)
```

While such an object is quite neat for developers, it would be a pain when users see the same. There are methods for converting the any duration instance into a human-readable string.

### The DD:HH:MM:SS format

The `getFormattedDuration` method outputs a string in that format. Quite nice for timers and stuff.
```ts
myDuration.getFormattedDuration();
// `00:00:02:45:684`
```

**What if I don't want all of that? I just want a MM:SS timer!**
Ok sure. You can pass `from` and `to` parameters to the method to just get the duration between those two.
```ts
myDuration.getFormattedDuration("m", "s");
// `02:45`
```

### The word format

The `stringify` method outputs a string in that format. Quite nice for normal text that ain't timers and stuff.
```ts
myDuration.stringify();
// `0 days, 0 hours, 2 minutes, 45 seconds, 684 milliseconds 0, microseconds, 0 nanoseconds`
```

You can provide specific units if you don't want all units.
```ts
myDuration.stringify(["s", "h"]);
// `0 hours, 45 seconds`
```

Still too long? Fortunately, there's another parameter for the function to tell it to shrink the string!
```ts
myDuration.stringify(["s", "h"], true);
// `0h 45s`
```

**What if I want all units but I also want them short? Should I supply every unit in the first parameter?**

Nah. We have our friendly neighborhood `null` with us.
```ts
myDuration.stringify(null, true);
// `0d 0h 2m 45s 684ms 0us 0ns`
```
