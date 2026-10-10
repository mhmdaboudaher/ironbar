# IronBar 💪

A calisthenics training web app with an AI coach.

**Live demo:** https://mhmdaboudaher.github.io/ironbar/


## Features

- Training programs for beginners to advanced
- AI coach: ask training questions and get short, safe answers
- Email login

## Tech Stack
- **Auth:** Firebase Authentication
- **Frontend:** HTML, CSS, JavaScript, hosted on GitHub Pages
- **AI coach:** Cloudflare Workers (proxy that keeps the API key secret) and the Groq API (OpenAI gpt-oss-120b)

## How the AI coach works

```
Browser → Cloudflare Worker → Groq API → reply → Browser
```

The browser never sees the API key. The key is stored as a secret in Cloudflare, and the Worker only accepts requests from this site's origin.

## What I learned

- Hiding API keys behind a serverless proxy
- Handling CORS and request validation
- Deploying a static site with Git and GitHub Pages

## Roadmap

- Rate limiting for the AI coach
- Login with Firebase Auth

## Author

Mhmd Aboudaher, [LinkedIn link when ready]