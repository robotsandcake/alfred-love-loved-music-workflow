# Alfred Loved or Unloved Music Workflow #

This Alfred workflow for macOS makes it easy for the user to set the currently playing song to "Loved" or "Unloved", which when coupled with an iTunes Smart Playlist means you can avoid the Barry Manilow and love the Orbital.

# Download #

## Usage ##

When a song is playing in iTunes invoke Alfred in your favourite way and simply type the words "Loved" or "Unloved" depending on your emotional attachment to that particular song.  Simples.

You will then be shown one of the following notifications depending on your choice:

![Loved Notification]()
![UnLoved Notification]()

## Alfred Preferences ##

When you first double-click and install the workflow you will see the following image:

![Alfred Preferences]()

The middle part of the workflow uses the following JavaScript, leveraging the __osascript__ tool in macOS AppleScript.

<script src="https://gist.github.com/robotsandcake/2b61c73d3ff7e0de4b00e13a3fe9de92.js"></script>
```


Then shows a notification.

![iTunes Loved Screenshot](https://cloud.githubusercontent.com/assets/2381/8754422/6f486980-2c91-11e5-8f6a-6f40f3d82e48.png)

