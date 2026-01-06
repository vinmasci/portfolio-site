# vincentmasci.dev

Personal portfolio site with interactive arcade games.

## Tech Stack

- HTML/CSS/JavaScript (single file)
- Firebase Firestore (contact form)
- Web Audio API (game sounds)
- Deployed on Vercel

## Features

- **3 Arcade Games**: Space Invaders, Pong, Snake
  - Desktop: Keyboard controls
  - Mobile: Touch controls with on-screen buttons
- **Contact Form**: Saves to Firebase Firestore
- **Fortune Cookie**: Random Chinese proverbs
- **Responsive**: Works on desktop and mobile

## Local Development

```bash
# Simple HTTP server
python3 -m http.server 8080

# Open http://localhost:8080
```

## Firebase Setup

The contact form uses Firebase Firestore. The config is already in the HTML pointing to the `cyaroutes` project.

Messages are saved to the `contact_messages` collection with:
- `name`
- `email`
- `message`
- `source`: "portfolio_site"
- `status`: "new"
- `createdAt`: timestamp

## Mobile Audio

iOS Safari requires user interaction to unlock audio. The site plays a silent buffer on first touch to unlock the AudioContext.

## Game Controls

### Space Invaders
- Desktop: Arrow keys / A,D to move, Space to fire
- Mobile: Left/Right buttons + Fire button

### Pong
- Desktop: W/S or Arrow Up/Down
- Mobile: Up/Down buttons

### Snake
- Desktop: Arrow keys or WASD
- Mobile: D-pad buttons

## Deployment

Hosted on Vercel, auto-deploys from GitHub.

```bash
git push origin main
```

## Domain

vincentmasci.dev (purchased via Vercel)
