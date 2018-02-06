# react-native-media

[![React Native Version](https://img.shields.io/badge/react--native-latest-blue.svg?style=flat-square)](http://facebook.github.io/react-native/releases)

![Logo](logo.png)

A react-native library to play and record audio on both iOS and android with no callbacks.

## Specifications

### iOS

* Built with AVAudioPlayer and AVAudioRecorder.
* Add `mute.caf` from the library to your project bundle
    * Project Navigator > [YOUR PROJECT NAME] > Build Phases > Copy Bundle Resources
* Add 'Local Authentication' framework
    * Project Settings > General and scroll down to the Linked Frameworks and Libraries section > Click on the + sign and add LocalAuthentication.framework.

### android

* Built with MediaPlayer and MediaRecorder.
* Add in the manifest.xml the permission:
    * 'android.permission.WAKE_LOCK'
    * 'android.permission.MODIFY_AUDIO_SETTINGS'
    * 'android.permission.USE_FINGERPRINT'

## Installation

Install the package:

```javascript
npm install react-native-media --save
```

or

```javascript
yarn add react-native-media
```

### Automatic

Link the native code with your RN application:

```javascript
react-native link react-native-media
```

### Manual

[TODO]

## Player

|Description|Android|iOS
---|---|---
|Load|✓|✓
|Play|✓|✓
|Load and Play|✓|✓
|Pause|✓|✓
|Resume|✓|✓
|Stop|✓|✓
|Seek Time|✓|✓
|Get Volume|✓|✓
|Set System Volume|
|Set Loops (-1 for infinite)|✓|✓
|Turn speakers on/off|✓|✓
|Set audio routes|✓|✓
|Mute|✓|
|Sleep mode on/off|✓|✓

## Recorder
Description ✓ | iOS | Android
---|---|---
Prepare (Bitrate, SampleRate, Channels, AudioQuality, AudioEncoding, Encoder)
Start
Stop


## Events
Description|Android|IOS
---|---|---
|Audio finished play|✓|✓
|Track current time|✓|✓
|Volume changed
|System volume changed
|Wired headset plugged/unplugged|✓|✓
|Audio focus changed
|Silent mode changed (iOS only)| |✓
|Dim screen by proximity on/off|✓|✓
