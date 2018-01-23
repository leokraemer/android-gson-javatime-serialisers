# gson-javatime-serialisers

## What is it?

A set of [GSON][1] serialiser/deserialisers for dealing with [Java 8 `java.time` entities][2] in Android. 
Created using the org.threeten.bp [port for android][5].  
Wherever possible, [ISO 8601 string representations](http://en.wikipedia.org/wiki/ISO_8601) are used.


## Getting it

use [jitpack][4]

TLDR;
add 
````
implementation 'com.github.leokraemer:gson-javatime-serialisers:2.1.2'
````
to your build.gradle

## Using it

````
final Gson gson = Converters.registerOffsetDateTime(new GsonBuilder()).create();
final OffsetDateTime original = OffsetDateTime.now();

final String json = gson.toJson(original);
final OffsetDateTime reconstituted = gson.fromJson(json, OffsetDateTime.class);
````


[1]: https://code.google.com/p/google-gson/
[2]: http://docs.oracle.com/javase/8/docs/api/java/time/package-summary.html
[3]: https://github.com/spencerwi/hamcrest-jdk8-time
[4]: https://jitpack.io/#leokraemer/gson-javatime-serialisers/2.1.2
[5]: https://github.com/JakeWharton/ThreeTenABP
