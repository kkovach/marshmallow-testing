# mashmallow-testing

Dagger 2 appears to break Android testing with the AndroidJUnitRunner. This repo consists of bare bones app and 2 Android libraries that have the same setup in an effort to figure out what the heck the difference is and how I can get it fixed.

* The only significant difference other than the library names is the dependency on Dagger 2.0.2.
* Both libraries have the same simple test that does nothing.
* Running ./gradlew clean connectedCheck from the root causes the library with the Dagger dependency (library) to fail.
* Tests successfully run on 18 and 19, but fail on 22 and 23 with the following error...

:library:connectedDebugAndroidTest
Tests on lollipop(AVD) - 5.1 failed: Instrumentation run failed due to 'java.lang.NoClassDefFoundError'

com.android.builder.testing.ConnectedDevice > No tests found.[lollipop(AVD) - 5.1] FAILED
No tests found. This usually means that your test classes are not in the form that your test runner expects (e.g. don't inherit from TestCase or lack @Test annotations).
:library:connectedDebugAndroidTest FAILED
