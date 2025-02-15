# StumbleTube

The **StumbleTube** is a UserScript written in JavaScript designed to enhance the user experience on **StumbleChat**, a web-based chat platform. It enables users to play YouTube videos directly from the chat box by processing specific commands and converting various YouTube URL formats into a standardized format for playback.

The script modifies the behavior of WebSocket communication to intercept and manipulate messages. It establishes a WebSocket connection with the chat server and overrides the `send` method to intercept outgoing messages, allowing for dynamic responses and actions based on user input.

---

## Features

- **YouTube Playback**: Play YouTube videos directly from the chat box using commands like `.youtube`, `.video`, `.play`, or `.yt`.
- **URL Conversion**: Automatically converts various YouTube URL formats (e.g., `youtu.be`, `youtube.com/watch?v=`) into a standardized format for seamless playback.
- **Search Support**: Allows users to search for YouTube videos by entering a query directly after the command.

---

## How It Works

1. **WebSocket Override**: The script overrides the WebSocket `send` method to attach a custom message handler. This ensures that all incoming messages are processed for YouTube-related commands.
2. **Message Handling**: When a message is received, the script checks if it starts with a predefined keyword (e.g., `.youtube`, `.yt`). If a match is found, the script extracts the query or URL from the message.
3. **URL Conversion**: The script uses a regular expression to extract the video ID from various YouTube URL formats and converts it into a standardized `https://www.youtube.com/watch?v=` format.
4. **Playback**: The standardized YouTube link or search query is sent back to the chat server, triggering the playback of the video in the chat room.

---

## Commands

Here are the supported commands for playing YouTube videos:

- **`.youtube [query or URL]`**: Play a YouTube video. Example: `.youtube https://www.youtube.com/watch?v=dQw4w9WgXcQ`
- **`.video [query or URL]`**: Play a YouTube video. Example: `.video dQw4w9WgXcQ`
- **`.play [query or URL]`**: Play a YouTube video. Example: `.play https://youtu.be/dQw4w9WgXcQ`
- **`.yt [query or URL]`**: Play a YouTube video. Example: `.yt rick roll`

---

## Installation

The script is available on **GreasyFork**:  
[Install StumbleTube](https://greasyfork.org/en/scripts/523602-stumbletube)

