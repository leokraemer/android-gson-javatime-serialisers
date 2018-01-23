# gson-javatime-serialisers

## What is it?

A set of [GSON][1] serialiser/deserialisers for dealing with [Java 8 `java.time` entities][2]. Portet to use org.threeten.bp.  Wherever possible, [ISO 8601 string representations](http://en.wikipedia.org/wiki/ISO_8601) are used.
Particularly useful to use in Android projects.

## Getting it

using [jitpack][4]

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

## Testing

Unrelated to `gson-javatime-serialisers` itself, but if you're working with Java 8 time, you may be interested in [`spencerwi/hamcrest-jdk8-time`][3]


[1]: https://code.google.com/p/google-gson/
[2]: http://docs.oracle.com/javase/8/docs/api/java/time/package-summary.html
[3]: https://github.com/spencerwi/hamcrest-jdk8-time
[4]: https://jitpack.io/
