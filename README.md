<p align="center">
<img width="128" src="https://github.com/enricocid/Music-Player-GO/blob/main/fastlane/metadata/android/en-US/images/icon.png">
</p>

<h1 align="center">Music Player GO - FORK ( Wear OS optimized )</h1>

Forked from: https://github.com/enricocid/Music-Player-GO

# Disclaimer: This is a quick and dirty solution - works for me - might work for you

# The problem

As of now, there seems to be no reasonably good music player for playing mp3 offline from local storage on Wear OS.

Samsung music cons:
- Only synchronizes up to 2 GB
- Can not play folders
- Requires playlists using Samsung Music

WearMedia cons:
- The only option on play store for now
- The main app on android asks for permission to share my data with tons of providers -> loosing trust
- Sometimes fails to play in the middle of a track. Important when using long titles to continue listening

# My attempt to solve

See what standard android app i can sideload and maybe modify a bit.
I dont need a beautiful UI for wear os, as long as it works.

Only the following roughly came close:
https://github.com/enricocid/Music-Player-GO

The only problem is, that its UI is obviously not optimized for wear os, but its not far from it.
I took only very few hours and removed / reordered a few UI components.

All changes can be found in the commit log:
https://github.com/frozen1c3/Music-Player-GO-WearOS/commits/main

Maybe someone else finds it useful as well, so here it is.

# How to use
- Download the apk from release (its actually only the debug apk and not a proper release)
- Sideload it to your watch using adb. For sideloading from Android, i recommend GeminiMan: https://play.google.com/store/apps/details?id=com.geminiman.wearosmanager&hl=en_US
- Transfer music to your phone using LocalSend - also required to be sideloaded via adb: https://f-droid.org/de/packages/org.localsend.localsend_app/
- Manage your music files (sideload via adb): https://f-droid.org/de/packages/com.martinmimigames.simplefileexplorer/
- Volume control:
  The volume control of the app seems to be an own one. With it you do NOT control the overall system sound volume, but only the player volume.
  So you might set your system volume to maximum, so that you have full control in the app. Otherwise you can only make it more quiet and not louder.
  System volume can be set by the included media control. To access it, start any song and switch to main menu. Once there hit the little icon, that indicates that music is playing. It opens the default media control, which allows to set the system wide volume.

# How to build (for non Android/Wear OS developers)
- Download Android Studio: https://developer.android.com/studio
- Clone the sources
- Open the subdirectory 'project/' in Android Studio
- Open the terminal IN Android studio and insert 'gradle clean build'
- Send the command with Ctrl+Enter
- Find the result in \project\app\build\outputs\apk\debug

