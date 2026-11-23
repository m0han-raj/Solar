# Solar

A Gemini-style chat interface built with React and Vite, powered by the Google Generative AI (Gemini) API.

## Overview

Solar is a single-page chat app modelled on the Gemini web UI. Users type a prompt (or pick a suggested one), the app sends it to the Gemini API, and the reply is streamed onto the screen word by word.

## Features

- Chat with Gemini (`gemini-1.0-pro`) through `@google/generative-ai`
- Suggested prompt cards on the landing screen
- Word-by-word rendering of responses, with bold text formatting
- Collapsible sidebar with a list of recent prompts that can be re-run
- "New Chat" action to reset the conversation view

## Project Structure

```
Solar/
├── index.html
├── package.json
├── vite.config.js
├── public/
│   └── solar_icon.png
└── src/
    ├── main.jsx              # App entry point
    ├── App.jsx               # Root layout (Sidebar + Main)
    ├── assets/               # Icons and asset exports
    ├── config/gemini.js      # Gemini API client and chat call
    ├── context/Context.jsx   # Global chat state and response handling
    └── Components/
        ├── Main/             # Chat area and suggestion cards
        └── Sidebar/          # Navigation and recent prompts
```

## Setup

Requires Node.js 18 or newer.

```bash
git clone https://github.com/m0han-raj/Solar.git
cd Solar
npm install
```

Create a Gemini API key at [Google AI Studio](https://aistudio.google.com/) and set it as `API_KEY` in `src/config/gemini.js`. Do not commit a real key to a public repository.

## Usage

```bash
npm run dev       # start the dev server
npm run build     # production build
npm run preview   # preview the production build
npm run lint      # run ESLint
```

## Tech Stack

React 18, Vite 5, Google Generative AI SDK, ESLint.

## License

Released under the [MIT License](LICENSE).
