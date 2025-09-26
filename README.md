# Hermes – Anime Tracker (A Next.js Web-App)

**Internal Name:** *Project Hermes*  
**Status:** Personal, open‑source web application (Next.js)

---

## Overview

Project Hermes is a lightweight, privacy‑first web app that lets anime fans keep track of what they’re watching. All data lives on a self‑hosted **Appwrite** backend running in Docker, and the front‑end is built with **Next.js** (React).

Key highlights:

- Delivered as a responsive website—no native mobile apps.  
- Synchronizes exclusively with **MyAnimeList (MAL)**.  
- Browser‑based push notifications for new episode releases.  
- Pulls rich metadata from **IMDB**, **Trakt**, and other public APIs.  

---

## Features

| Feature                     | Description                                                                 |
|-----------------------------|-----------------------------------------------------------------------------|
| **Anime progress tracking** | Mark episodes as watched, set status (watching, completed, on‑hold, dropped). |
| **MAL synchronization**    | Import/export your MAL list with a single click.                           |
| **Rich metadata**           | Retrieve titles, synopses, voice‑actor credits, release dates, and more from IMDB / Trakt. |
| **Custom collections**      | Build personal “playlists” of series, movies, or OVAs.                      |
| **Recommendations**         | AI‑driven suggestions based on your watch history.                         |
| **Browser push notifications** | Timely alerts for upcoming episode releases.                            |
| **Soundtrack info**         | View associated music tracks where available.                               |
| **Privacy‑first design**    | No third‑party analytics; all data stored on your own Appwrite instance.   |

---

## Tech Stack

- **Front‑end:** Next.js (React), TypeScript, Tailwind CSS  
- **Back‑end:** Appwrite (self‑hosted Docker container) – provides data storage, real‑time subscriptions, and push‑notification endpoints.  
- **Authentication:** Simple UUID‑based identity stored in `localStorage`; no passwords or emails.  
- **External APIs:** MyAnimeList (OAuth 2.0), IMDB, Trakt, TheMovieDB (supplementary info).  
- **Push service:** Web Push (VAPID keys generated on the Appwrite server).  

---

## Future Plans

- **Windows installer** – Package the web app as a standalone `.exe` using tools such as Electron or Tauri, giving Windows users a simple double‑click installation experience.  
- **Android wrapper** – Create an `.apk` that embeds the web app in a native WebView (e.g., via Capacitor or Cordova), allowing Android devices to run Hermes as if it were a native app while keeping the same codebase.  
