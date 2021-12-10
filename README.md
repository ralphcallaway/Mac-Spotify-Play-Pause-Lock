# Description

Apple changed things at some point so that the play/pause buttons automatically launched itunes in most cases, or sends the commands to your browser window. I've already got the space bar for play pause on active windows, I'd like things to just always go to spotify. This does that but loses the functionality of the media keys for other applications.

# Usage

## Enable

- clone down this repo
- disable mac control of media keys `$ launchctl unload -w /System/Library/LaunchAgents/com.apple.rcd.plist`
- sym link the spotify_rewire.json into ~/.config/karabiner/assets/complex_modifications
- open karabiners and enable the "Spotify Rewire" rule
- add basic modifications for the "TouchBarUserDevice (Apple Inc.)" target device as follows
  - rewind -> f7
  - play_or_pause -> f8
  - fast_forward -> f9
- hopefully it works for you!

## Disable

- to give back mac control of media keys `$ launchctl load -w /System/Library/LaunchAgents/com.apple.rcd.plist`
- disable the "Spotify Rewire" rule in karabiner
- remove the simple modifications for the "TouchBarUserDevice" target device for the media keys

# Caveats

- This will break the media keys (play/pause/next) for all other applications
- The touch bar keys no longer work :-(

# DISCLAIMER

No warranties. This works for me, but who knows for you.
