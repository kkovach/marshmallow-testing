# mashmallow-testing

Dagger 2 appears to break Android testing with the AndroidJUnitRunner. This repo consists of bare bones app and 2 Android libraries that have the same setup in an effort to figure out what the heck the difference is and how I can get it fixed.

* The only significant different other than the library names are the dependency on Dagger 2.0.2.
* Both libraries have the same simple test that does nothing.
* Running ./gradlew clean connectedCheck from the root causes the library with the Dagger dependency (library) to fail.
