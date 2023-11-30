# "Now Playing" for i3status bar

A Python  script to show media metadata (artist and title) in i3status bar. It requires `playerctl` to work.

![image](https://github.com/leandroembu/i3status_now_playing/assets/3253741/c8c87229-b307-4764-8de1-874b78a651dc)


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

Copy file [i3status_now_playing.py](i3status_now_playing.py) to ~/.config/i3 folder and change the bar block in ~/.config/i3/config:

```
bar {
    status_command i3status | ~/.config/i3/i3status_now_playing.py
}
```

Restart i3 Window Manager ($mod+Shift+R).
