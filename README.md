# Cordova Android Volume Plugin

Very self-explanatory. Allows you to get and set the volume for Android devices in a Cordova app.

# API

## Get Functions

`success` is a callback called to return the volume. The first parameter is the volume level.

`error` is a callback called if anything goes wrong. (Optional)

```js
// Get the alarm volume level
window.androidVolume.getAlarm(success, error);

// Get the DTMF volume level
window.androidVolume.getDTMF(success, error);

// Get the music/media volume level
window.androidVolume.getMusic(success, error);

// Get the notification volume level
window.androidVolume.getNotification(success, error);

// Get the ringer volume level
window.androidVolume.getRinger(success, error);

// Get the system volume level
window.androidVolume.getSystem(success, error);

// Get the voice call volume level
window.androidVolume.getVoiceCall(success, error);
```

## Set Functions

`volume` is an integer between 0 and 100.

`success` is a callback called whenever the volume is changed. The first parameter is the new volume value. (Optional)

`error` is a calback called if anything goes wrong. (Optional)

```js
// Set all different types of volume to the same level
window.androidVolume.set(volume, success, error)

// Set the alarm volume level
window.androidVolume.setAlarm(volume, success, error)

// Set all different types of volume to the same level
// Alias for `set`
window.androidVolume.setAll(volume, success, error)

// Set the DTMF volume level
window.androidVolume.setDTMF(volume, success, error)

// Set the music/media volume level
window.androidVolume.setMusic(volume, success, error)

// Set the notification volume level
window.androidVolume.setNotification(volume, success, error)

// Set the ringer/ringtone volume level
window.androidVolume.setRinger(volume, success, error)

// Set the system volume level
window.androidVolume.setSystem(volume, success, error)

// Set the voice call volume level
window.androidVolume.setVoiceCall(volume, success, error)
```

## Events

To get updates whenever the volume of the device changes, you may register for `volume` updates

```js
window.addEventListener('volume', function(ev) {
    console.log("type " + ev.volumeType + ", level " + ev.volumeLevel);
}, false);
```