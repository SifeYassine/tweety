# Tweety

A **Twitter (X) clone** built with **Vue 3** and **Tailwind CSS**, backed by a mock REST API powered by **json-server**. It recreates Twitter's dark home timeline: post tweets, like them, comment on them, search the feed, and browse trending topics.

## Features

- **Home timeline** of tweets with author name, handle, text, and optional image
- **Post a tweet** from the "What's happening?" bar
- **Like / unlike** tweets with live like counts
- **Comments**: open a tweet's comment form, read existing comments, and add new ones (comment counts update automatically)
- **Search** the timeline (press <kbd>Enter</kbd>)
- **Trending for you** sidebar with hashtags and compact tweet counts (`1.2K`, `3.4M`, …)
- Twitter-style navigation sidebar and dark theme

## Tech Stack

| Concern   | Technology |
| --------- | ---------- |
| Framework | Vue 3 (Vue CLI) |
| Styling   | Tailwind CSS |
| HTTP      | Axios |
| Mock API  | json-server (`db.json`) |

## Project Structure

```
tweety/
├── db.json                 # Mock database: Users, Posts, Comments, Trends
├── src/
│   ├── App.vue             # Layout: sidebar, timeline, search, trends
│   ├── components/
│   │   ├── SideBar.vue     # Navigation
│   │   ├── TweetBar.vue    # Compose a tweet
│   │   ├── Posts.vue       # Timeline, likes, search filtering
│   │   ├── CommentForm.vue # Comments for a tweet
│   │   ├── SearchField.vue
│   │   └── Trending.vue
│   ├── assets/             # Icons and images
│   ├── input.css           # Tailwind entry
│   └── style.css           # Compiled Tailwind
└── tailwind.config.js
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) and npm

### Installation

```bash
git clone https://github.com/SifeYassine/tweety.git
cd tweety
npm install
npm install --save-dev json-server concurrently
```

> `json-server` and `concurrently` are used by the npm scripts but aren't listed in `package.json`, so install them as shown above (or globally).

### Run

Start the Vue dev server, the Tailwind watcher, and the mock API together:

```bash
npm start
```

Or run them separately:

```bash
npm run jsonserver   # API at http://localhost:3000
npm run cssbuild     # Tailwind in watch mode
npm run serve        # App at http://localhost:8080
```

## Mock API

json-server exposes `db.json` as a REST API on port **3000**:

| Resource    | Endpoint |
| ----------- | -------- |
| Users       | `/Users` |
| Posts       | `/Posts` |
| Comments    | `/Comments` |
| Trends      | `/Trends` |

## Disclaimer

This is a learning project and is not affiliated with Twitter / X.

## Author

**Sifeddine Yassine** · [@SifeYassine](https://github.com/SifeYassine)
