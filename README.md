<p align="center">
<img width="128" src="https://github.com/enricocid/Music-Player-GO/blob/main/fastlane/metadata/android/en-US/images/icon.png">
</p>

<h1 align="center">Music Player GO - FORK ( Wear OS optimized )</h1>

Forked from: https://github.com/enricocid/Music-Player-GO

# Fork details on Wear OS optimization

! Disclaimer: This is a quick and dirty solution, but it works for me and given the little time i had, its more than nothing. !

Current situation:

As of now, there seems to be no reasonably good music player for playing mp3 offline from local storage.

Samsung music:

    Only synchronizes up to 2 GB

    Can not play folders

WearMedia:

    The only option on play store for now

    The main app on android asks for permission to share my data with tons of providers -> loosing trust

    Sometimes fails to play in the middle of a track. Important when using long titles to continue listening

My attempt:

See what standard android app i can sideload and maybe modify a bit.
I dont need a beautiful UI for wear os, as long as it works.

Only the following roughly came close:
https://github.com/enricocid/Music-Player-GO

The only problem is, that its UI is obviously not optimized for wear os, but its not far from it.
I took only very few hours and removed / reordered a few UI components.

All changes can be found in the commit log:
https://github.com/frozen1c3/Music-Player-GO-WearOS/commits/main

Maybe someone else finds it useful as well, so here it is.

How to use:
- Download the apk from release (its actually only the debug apk and not a proper release)
- Sideload it to your watch using adb. For sideloading from Android, i recommend GeminiMan
- Transfer music to your phone using LocalSend - also required to be sideloaded via adb: https://f-droid.org/de/packages/org.localsend.localsend_app/

How to build (for non Android/Wear OS developers):
- Download Android Studio
- Clone the sources
- Open the subdirectory 'project/' in Android Studio
- Open the terminal IN Android studio and insert 'gradle clean build'
- Send the command with Ctrl+Enter
- Find the result in \project\app\build\outputs\apk\debug

