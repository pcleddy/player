# Local MP3 Player

## Goal

Provide a small, self-contained browser app for listening to a local audio file. The app runs directly from `index.html`; it does not need a Node server, account, or network connection.

## User experience

1. The user selects an audio file with the file picker or drops it onto the upload area.
2. The selected file name appears, and the user can play or pause it.
3. The user can seek on the timeline, jump backward or forward by a configurable number of seconds, and change playback speed.
4. Keyboard shortcuts support playback and skipping.

## Requirements

- Accept locally selected audio files, including MP3.
- Play and pause the loaded file.
- Show elapsed and total time and provide a seek slider.
- Provide backward and forward skip buttons with a configurable interval from 1 to 300 seconds.
- Offer playback rates from 0.5× through 2×.
- Support drag and drop in addition to the file picker.
- Provide accessible labels, status announcements, focus indicators, and responsive layout.
- Keep audio local to the browser using a temporary object URL and release it when replaced or when the page closes.
- Work as a static page opened in a modern browser.

## Implementation

The app is implemented in one `index.html` file with inline CSS and JavaScript. It uses the browser's `HTMLAudioElement` and File API. No build step or dependency installation is required.

## Keyboard shortcuts

- `Space`: play or pause
- `←`: skip backward by the selected interval
- `→`: skip forward by the selected interval

Shortcuts are ignored while the user is focused on an input, select, or button.

## Scope

The current version is a single-track player. It does not save a playlist or settings between sessions, edit audio, or upload files to a server.
