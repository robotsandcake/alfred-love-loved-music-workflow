# Alfred Loved or Unloved Music Workflow #

This [Alfred.app](https://www.alfredapp.com/) [workflow](https://www.alfredapp.com/workflows/) for [macOS](https://www.apple.com/macos) makes it easy for the user to set the currently playing song to "Loved" or "Unloved", which when coupled with an [iTunes](https://www.apple.com/itunes/) [Smart Playlist](https://support.apple.com/kb/PH19487?locale=en_US) means you can avoid the [Barry Manilow](http://barrymanilow.com) and love the [Orbital](http://www.orbitalofficial.com/).

# Download #

You can [download the workflow here](https://github.com/robotsandcake/alfred-love-loved-music-workflow/blob/master/love-unloved-music.alfredworkflow?raw=true).

## Usage ##

When a song is playing in [iTunes](https://www.apple.com/itunes/) invoke [Alfred](https://www.alfredapp.com/) in your favourite way and simply type the words "Loved" or "Unloved" depending on your emotional attachment to that particular song.  Simples.

You will then be shown one of the following notifications depending on your choice:

### Loving Notification ###

![Loved Notification](https://github.com/robotsandcake/alfred-love-loved-music-workflow/blob/master/images/alfred-love-loved-music-workflow-loved-notification.png?raw=true)

### Unloving Notification ###

![UnLoved Notification](https://github.com/robotsandcake/alfred-love-loved-music-workflow/blob/master/images/alfred-love-loved-music-workflow-unloved-notification.png?raw=true)

## Alfred Preferences ##

When you first double-click and install the workflow you will see the following image:

![Alfred Preferences](https://github.com/robotsandcake/alfred-love-loved-music-workflow/blob/master/images/alfred-love-loved-music-workflow-preferences.png?raw=true)

### JavaScript/AppleScript Needed ###

The middle part of the workflow that does all of the work uses the following [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript), leveraging the __osascript__ tool in [AppleScript](https://developer.apple.com/library/content/documentation/AppleScript/Conceptual/AppleScriptX/AppleScriptX.html).


```javascript
(function() {
  var track = Application("iTunes").currentTrack();
  var trackLoved = track.loved();
  var notification = (trackLoved ? "UnLoved" : "Loved") + ": " + track.name();
  track.loved = !trackLoved;
  return notification;
})()
```