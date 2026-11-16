# Squad View

Watch several YouTube live streams at once. One stream fills the screen and the others float beside it as small windows. Tap a small window to make it the main one.

Live page: https://brandonoakley.github.io/squad-view/

## How to use it

1. Open each streamer's live stream on YouTube, tap **Share**, and copy the link.
2. Paste one or more links into the box at the top and tap **Add**.
3. Tap a small window to swap it into the main spot. Sound follows the main stream.

| Button | What it does |
| --- | --- |
| Sound on / off | Mutes or unmutes the main stream |
| −5s / +5s | Nudges the main stream to line it up with the others |
| Grid | Switches between the floating layout and an equal-size grid |
| Size | Changes the size of the small windows (S, M, L) |
| Remove main | Removes the main stream |
| Copy link | Copies a link that includes your stream list, for opening on another device |
| Full screen | Hides the browser chrome |

## Limits

- The page must be opened from a web address. YouTube refuses to play in a file opened directly from disk.
- Streamers who have turned off embedding will not load. The tile shows a link to open that stream on YouTube.
- Use the link of the stream itself, not the channel page.
- Ad-free playback with YouTube Premium depends on being signed in to YouTube in the same browser and on that browser's privacy settings.

## How it works

Everything is in `index.html`: plain HTML, CSS and JavaScript with no build step. It uses YouTube's official IFrame Player API. There is no server, no account and no API key. Your stream list is kept in the page's link and in your browser's local storage.

## Keeping secrets out

This repository is public, so nothing private belongs in it. The page needs no keys or passwords. If a later feature needs a YouTube API key, do not commit it: a key in a public page can be read by anyone. The `.gitignore` blocks common secret files such as `.env` as a backstop.
