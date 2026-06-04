# dream-recorder

## Overview

capturing user input, editing and saving the dream text, submitting it to a backend generation service, tracking asynchronous task status, and previewing the generated video once available.

## Key Features

* Voice-based dream recording using browser speech recognition
* Text-based dream input and editing
* Local dream entry storage in the browser
* Calendar-style dream record browsing
* Dream statistics such as total records, streaks, and lucid dream count
* Configurable Dream-to-Video backend API connection
* Automatic submission of dream text to a video-generation endpoint
* Task polling for video generation progress
* Status display for pending, generating, completed, and failed tasks
* Generated video preview inside the dream entry interface
* JSON export for dream records

## Workflow

1. The user records or types a dream.
2. The dream text is edited and saved as a local entry.
3. If a backend API is configured, the frontend submits the dream text to `/api/generate`.
4. The backend returns a task ID.
5. The frontend polls `/api/tasks/{taskId}` to track generation progress.
6. When a video URL is returned, the entry updates and displays the generated video preview.


## Tech Stack

* React 18
* HTML / CSS / JavaScript
* Babel standalone for browser-based JSX prototyping
* Web Speech API for voice transcription
* LocalStorage for browser-side persistence
* REST API integration for backend video generation
* GitHub Pages-compatible single-file frontend prototype

## What I Learned

Through this project, I practised:

* Building an interactive single-page web prototype
* Designing a user flow around low-friction dream capture
* Using browser speech recognition for voice-to-text input
* Managing local state and local persistence
* Designing an asynchronous AI workflow with task submission and polling
* Thinking about how generative AI tools can be integrated into user-facing products
* Balancing creativity, usability, and workflow reliability

## Current Limitations

* The repository currently contains the frontend prototype only.
* The video generation model/backend is expected to be connected separately.
* API keys should not be exposed in a production frontend; a real deployment should use a secure backend proxy and proper authentication.
* The project is an early prototype, not a production-ready application.

## Future Improvements

* Add a secure backend service for API key management
* Improve backend integration and error handling
* Add authentication and cloud sync
* Add better prompt construction for dream-to-video generation
* Add video generation history and retry controls
* Add privacy controls for sensitive dream content
* Create a cleaner project structure using a modern React build tool
* Add screenshots and a short demo video

## Status

Early-stage personal prototype for learning and experimentation in AI workflows, generative media, HCI, and personal informatics.
