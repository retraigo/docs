---
title: Methods - Duration
description: "All getters and methods in the Duration class."
position: 9
category: Duration
menuTitle: Methods
---

## get array()

An array of time units and their values.

    returns {KeyValue[]}
        - An array of unit types and their values

## get µs()

Alias for microseconds.

## get json()

Data in the class mapped as a JavaScript Object.

    returns {DurationObj}
        - Object with units as keys and their values as values.

## addDays(n: number)

Add more days to the duration.

    parameter {number} n
        - Number of days to add.

    returns {Duration}
        - The updated duration.

## addHours(n: number)

Add more hours to the duration.

    parameter {number} n
        - Number of hours to add.

    returns {Duration}
        - The updated duration.

## addMinutes(n: number)

Add more minutes to the duration.

    parameter {number} n
        - Number of minutes to add.

    returns {Duration}
        - The updated duration.

## addSeconds(n: number)

Add more seconds to the duration.

    parameter {number} n
        - Number of seconds to add.

    returns {Duration}
        - The updated duration.

## addMilliseconds(n: number)

Add more milliseconds to the duration.

    parameter {number} n
        - Number of milliseconds to add.

    returns {Duration}
        - The updated duration.

## addMicroseconds(n: number)

Add more microseconds to the duration.

    parameter {number} n
        - Number of microseconds to add.

    returns {Duration}
        - The updated duration.

## addNanoseconds(n: number)

Add more nanoseconds to the duration.

    parameter {number} n
        - Number of nanoseconds to add.

    returns {Duration}
        - The updated duration.

## setDays(n: number)

Set days of the duration.

    parameter {number} n
        - Number of days to set.

    returns {Duration}
        - The updated duration.

## setHours(n: number)

Set hours of the duration.

    parameter {number} n
        - Number of hours to set.

    returns {Duration}
        - The updated duration.

## setMinutes(n: number)

Set minutes of the duration.

    parameter {number} n
        - Number of minutes to set.

    returns {Duration}
        - The updated duration.

## setSeconds(n: number)

Set seconds of the duration.

    parameter {number} n
        - Number of seconds to set.

    returns {Duration}
        - The updated duration.

## setMilliseconds(n: number)

Set milliseconds of the duration.

    parameter {number} n
        - Number of milliseconds to set.

    returns {Duration}
        - The updated duration.

## setMicroseconds(n: number)

Set microseconds of the duration.

    parameter {number} n
        - Number of microseconds to set.

    returns {Duration}
        The updated duration.

## setNanoseconds(n: number)

Set nanoseconds of the duration.

    parameter {number} n
        - Number of nanoseconds to set.

    returns {Duration}
        - The updated duration.

## stringify(values: string[], shortandsweet)

Get a formatted, human-readable string of the duration.

    parameter {string[]} values
        - The values required to display.

    parameter {boolean} shortandsweet
        - If response should be a short string 
        (like using `m` instead of `minutes`).

    returns {string}
        - The formatted string result.

## getFormattedDuration(fromT, toT)

Get a duration formatted using colons (:).

    parameter {string} fromT
        - Unit to display from.

    parameter {string} toT
        - Unit to display upto.

    returns {string}
        - Formatted string.

## getSimpleFormattedDuration()

Get a simple formatted duration in the form dd:hh:mm:ss:ms

    returns {string}
        - Formatted string

## toString()

Extra filler function that returns the class data in a single short string.

    returns {string}
        - Dumb string

## reload()

Update data to match any modification to values.

    returns {<Duration>}

## static fromString(str: string, doNotParse)

Reads a given string and parses a duration from it.

    parameter {string} str
        - A string which could contain a duration

    parameter {string} doNotParse
        - Directly return the values read

    returns {<Duration>}

## static getCurrentDuration()

Get the duration till next midnight in milliseconds.

    returns {number}
        - Duration in milliseconds till the next midnight

## static readString(str: string)

Read duration data from a string.

    parameter {string} str
        - The string to read

    returns {DurationObj}
        - Object with days, hours, mins, seconds and milliseconds
