# AndroidStudioBenchmark (Firefox Focus for Android)

`AndroidStudioBenchmark` contains a large codebase to measure the compilation time in `Android Studio`.

You are probably familiar with the following question:

"Should I buy an i5, i7, or even i9 processor for Android development? How much RAM would be enough? How SSD/M.2/NVMe influence build time?".

`AndroidStudioBenchmark` is initially created for my personal youtube channel 
https://www.youtube.com/c/serhiyradkivskyi/about
to compare the performance of top laptops to choose the best system for `Android development`, because I hate to wait lot 
of time waiting project to be built. And if we are buying laptop for 1000+ USD we want to be sure that it will perform 
2x, 3x times faster than our current machine at least. But online shops in there most - don't give ability to make real world 
testing on your project to compare results. And most of reviewers describe laptops from designers/youtubers point of view, 
not that much information from real software developers.

I believe the results will help developers to make the right cost/performance trade-off decision when choosing their next Mac/PC.
If you are interested - just continue reading and if you'll find this test useful - it would be very cool if you can share your result 
and subscribe for my channel - it would be cool to have like minded audiance to share some more test on and get feedback on any 
professional stuff.


[![Build Status](https://travis-ci.org/mozilla-mobile/focus-android.svg?branch=master)](https://travis-ci.org/mozilla-mobile/focus-android)
[![Task Status](https://github.taskcluster.net/v1/repository/mozilla-mobile/focus-android/master/badge.svg)](https://github.taskcluster.net/v1/repository/mozilla-mobile/focus-android/master/latest)
[![codecov](https://codecov.io/gh/mozilla-mobile/focus-android/branch/master/graph/badge.svg)](https://codecov.io/gh/mozilla-mobile/focus-android/branch/master)

_Browse like no one’s watching. The new Firefox Focus automatically blocks a wide range of online trackers — from the moment you launch it to the second you leave it. Easily erase your history, passwords and cookies, so you won’t get followed by things like unwanted ads._ 

Firefox Focus provides automatic ad blocking and tracking protection on an easy-to-use private browser.

<a href="https://play.google.com/store/apps/details?id=org.mozilla.focus" target="_blank"><img src="https://play.google.com/intl/en_us/badges/images/generic/en-play-badge.png" alt="Get it on Google Play" height="90"/></a>
<a href="https://f-droid.org/en/packages/org.mozilla.klar/" target="_blank">
<img src="https://f-droid.org/badge/get-it-on.png" alt="Get it on F-Droid" height="90"/></a>

* [Google Play: Firefox Focus (Global)](https://play.google.com/store/apps/details?id=org.mozilla.focus)
* [Google Play: Firefox Klar (Germany, Austria & Switzerland)](https://play.google.com/store/apps/details?id=org.mozilla.klar)
* [Download APKs](https://github.com/mozilla-mobile/focus-android/releases)



# 1. Install Android Studio: https://developer.android.com/studio 
I was running test on `Android Studio 4.1.1`.

I was using default settings while installation almost for all my tests.

`Intel HAXM` also must be installed if you run on Intel chip.

I have set 4Gb RAM for my android virtual machine.

And please remember your Android SDK location.

# 2. Download API Level 28 SDK for this do next:
Go to: `Tools -> SDK Manager`

Choose Tab: `SDK Platforms`

Select: `Android 9.0 (Pie) API Level 28` and download it.

Close `Android Studio` after this.

# 3. Install JDK 8: https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html
I have installed: `Java SE Development Kit 8u271`

# 4. Set "JAVA_HOME" path in your Environment variables (System variables):
For me it was: `JAVA_HOME: C:\Program Files\Java\jdk1.8.0_271`

# 5. Download AndroidStudioBenchmark repository: https://github.com/yozhik/AndroidStudioBenchmark
This is a fork of opensource `Firefox browser for Android` (https://github.com/mozilla-mobile/focus-android). 

This is quite a big project (after all gradle modules downloaded it weights 6+Gb).

You can download it as zip file to you fast SSD location.

Unzip it.

# 6. Restart you system. 
Then make sure that no other programs/antivirus/browsers/big massive custom processes running.

Make sure that system is quite idle.

# 7. Open Android Studio.
Go to `File -> Open`: select Firefox Focus for Android project from your location and open it.

`Wait while all gradle files will be synced`, it can take up to 5-10 minutes.

# 8. Run next command to test speed of your machine doing next work:
Go to: `View -> Tools Windows -> Terminal`

Type command and press enter: 


Windows:
  ```shell
  gradlew clean assembleDebug
  ```
  
  MacOS/Linux:
  ```shell
  ./gradlew clean assembleDebug
  ```
  
Wait for assembling to complete. Run it 3 times in a row.

First time it will be your fresh build and it will take a little longer. Two next builds will be normal one.

After each build completes make a screenshot and save time result.

While system assembling watch for you `Task Manager` how `CPU` is processing, how much `RAM` is used, 
it would be cool if you can watch CPU temperature with some tool like `AIDA`: https://www.aida64.com/downloads

# 9. If you want to share result of your test with the community, 
please send it to my email: serhiyradkivskiy@gmail.com and I will add it here:

In such format:

Letter theme: `AndroidStudioPerformanceTest`

`Notebook model`: HP 250 G5 15.6"

`OS`: Windows/Linux/MacOS

`Android Studio version`: 4.1.1

`CPU model`: Intel Core i5-7200U 2.5GHz

`RAM`: 8Gb DDR4

`Hard disk`: SSD M.2 256Gb KINGSTON SUV400S37240G (or HDD disk model)

`Test results`: 8:28min, 5:43, 5:37. And screenshots for them.

`Additional comments`: you can write here whenever you want: The CPU was running all time 100%, laptop was extremely hot 
near the screen, ram was used for 80% etc, fans where running very hard etc..

`Contributor`: If you want to leave here a link to your youtube channel/linkedin/other contact info/alias etc - you are welcome, if not - it will be empty.


# 10. YouTubers and bloggers
You are free to use these results in your videos and articles as well as to run `AndroidStudioBenchmark` to compare Macs/PCs. 

If you decide to record video with this test - it would be very cool if you could upload it to youtube!

Please make sure to add the link to this repository: https://github.com/yozhik/AndroidStudioBenchmark

Please name it: `Android Studio Perfomance Test on <You machine name>`.

Hashtag: `#AndroidStudioPerformanceTest`

So everyone could find it and watch and your audiance could repeat steps after you and compare their machine results.

The results show relative performance of Android Studio, compared to other machines running under similar conditions.


## License


    This Source Code Form is subject to the terms of the Mozilla Public
    License, v. 2.0. If a copy of the MPL was not distributed with this
    file, You can obtain one at http://mozilla.org/MPL/2.0/
