# Project Roadmap

Pick a topic, build a project, tick it off. 600+ projects across web, backend, DevOps, data, AI, mobile, security and more, each with a full spec (requirements, sample code and expected output).

**Live site: https://sourabhrustagi.github.io/roadmap/**

## Features

- Topics sidebar with role filter, star and delete (double confirmation, restorable)
- Level filter, search, starred projects, delete projects you don't want to build
- Progress tracking, saved in your browser (localStorage)

## Run locally

Open `index.html` directly, or serve the folder (recommended):

```
python3 -m http.server
```

then visit http://localhost:8000.

## Data

Projects live in `projects.json`. `projects.js` is a copy of the same data that lets the page work when opened from a file; keep them in sync (CI fails if they differ).

## Deployment

Every push to `main` deploys to GitHub Pages through `.github/workflows/pages.yml`. The workflow first checks that `projects.json` is valid and that `projects.js` matches it.

One-time setup: in the repository go to **Settings → Pages → Build and deployment → Source** and choose **GitHub Actions**.
