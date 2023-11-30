# "Now Playing" for i3status bar

Adapted from [here](https://dimmaski.com/i3status/) and [here](https://www.reddit.com/r/i3wm/comments/sdzqn1/display_current_song_in_status_bar/).

Tested in:
- Firefox
  - Deezer, Spotify, Youtube
- Flatpak versions of Deezer and Spotify
- Freetube (flatpak package)
- Clementine
  - Local media
  - Online radio stations
  - Podcasts
- VLC
  - Local media

## Install playerctl package.

On Debian: `apt install playerctl`

## Changes in i3 configuration

Copy file i3status_now_playing.py to ~/.config/i3 folder and change the bar block in ~/.config/i3/config:

```
bar {
    status_command i3status | ~/.config/i3/i3status_now_playing.py
}
```

Restart i3 Window Manager ($mod+Shift+R).
