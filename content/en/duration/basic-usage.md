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

**I don't want a duration class. It's a pain.**

Ok. Just use the `.json` property (a getter to be specific). It'll return a plain ol object.

## Get duration from a string
**What about when you said it can parse human-readable strings?**

Yes.

The `fromString` static method can construct a duration from such a string. 
However, it still has limitations (which I haven't found yet). 

```ts
const myString = "4090 sec 4939  days 7342  hour 2324milliseconds 4344 min"
Duration.fromString(); 
// Duration {d: 5246, h: 13, m: 52, s: 12, ms: 324 }
```

**Can it not read data from strings like `HH:MM:SS`?**

The code has no way of knowing what part of the string is what. 
Moreover, such a string can be easily passed by a user with the `string.split()` method.

**I don't want a duration class. It's a pain.**

Ok. Just use the `readString` static method. It'll return the same data `Duration.json` does.