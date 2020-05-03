# Temporal Constants
Constants to compute with time units without magic numbers.

## Why?

How often do you have to do some calculations to convert seconds to milliseconds, hours to days,
or any number of others? Does everyone looking at your code understand why you are multipling
a number of days by 86400?

We use these constant values in computations all the time in code,
yet we also know that magic numbers are to be avoided:

> Unique values with unexplained meaning or multiple occurrences which could (preferably) be replaced with named constants
> -- [Wikipedia](https://en.wikipedia.org/wiki/Magic_number_(programming))

This tiny library defines those constants for you, so now instead of:

`Math.round(ms / 60000)`, you can write `Math.round(ms / MillisecondsInMinute)`
 
Or in place of: `setTimer(() => runMyFunction(), 24*60*60*1000)`

you get the clearer (and faster): `setTimer(() => runMyFunction(), MillisecondsInDay)`.

## Compatibility

Compatible with Javascript ES2015/ES6 and newer, as well as Typescript.

## FAQ

*Q:* Why should I introduce another dependency for a few constants that I can define myself?

*A:* Have you defined them? Did you make any mistakes computing them?

If you don't want a dependency, feel free to copy the lines into your own source.
In this case, the times they are **not** a-changin'. 

## See also....

- [temporal-types](https://github.com/kernwig/temporal-types) - Typescript types for time units
- [js-joda](https://js-joda.github.io/js-joda/) - Complete library for date and time representation and manipulation
 
