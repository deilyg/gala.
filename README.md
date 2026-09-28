# Gala — Travel Social Website Prototype

Gala is a responsive travel social network prototype combining social feed, short travel videos, destination discovery, maps, Travelers Hub, trips, journeys, groups, saved places, and memories.

## Run locally

No framework or build step is required.

### Option 1 — VS Code
Open this folder and use any static server extension, then open `index.html`.

### Option 2 — Python
```bash
python -m http.server 8080
```
Open `http://localhost:8080`.

### Option 3 — Node.js
```bash
npx serve .
```

## GitHub Pages

1. Create a GitHub repository, e.g. `gala-travel-social-web`.
2. Upload `index.html`, `README.md`, `.gitignore`, and `LICENSE`.
3. Go to **Settings → Pages**.
4. Choose **Deploy from a branch**.
5. Select `main` and `/root`.
6. Save. GitHub will publish the website.

## Responsive design

The UI adapts between desktop, tablet, and mobile layouts:

- Desktop: left navigation + central feed + right sidebar
- Tablet: left navigation + main content
- Mobile: full-width content + fixed bottom navigation
- Touch-friendly buttons and cards
- Responsive maps, reels, trip cards, and dialogs

## Prototype status

This is a front-end interaction prototype. Data is mock/in-memory and does not yet persist to a database.

Planned production integrations:

- Authentication
- PostgreSQL/PostGIS
- Real map provider
- GPS/background location
- Photo/video storage and playback
- Real-time buddy locations
- Notifications
- Recommendation engine
- Business/creator accounts

## Repository structure

```text
.
├── index.html
├── README.md
├── LICENSE
└── .gitignore
```
