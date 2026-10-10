# Usama & Kiran — Digital Nikah Invitation

A luxury, mobile-first interactive wedding invitation built with TanStack Start
(React 19 + Vite + Tailwind CSS v4).

## What's inside

- **Sealed envelope opener** — tap the gold wax seal, the flap flips back in 3D
  and the champagne curtains part to unveil the card.
- **Guest personalization** — read `?guest=` from the URL, e.g.
  `?guest=Auntie+Fatima+%26+Family`. Falls back to "Honored Guest & Family".
- **Scratch-to-reveal date** — a gold-leaf canvas you scratch with a finger.
- **Live countdown** — to Friday, October 30, 2026 at 03:00 PM PKT.
- **Venue link** — Bin Fida Palace Marquee with an "Open in Google Maps" button.
- **Mughal-inspired styling** — parchment and antique-gold palette, Cinzel /
  Cinzel Decorative / Alex Brush / Montserrat typography, pressed-flower corners.

## Run it locally

Requires Node.js 20+ and npm (or Bun).

```sh
npm install
npm run dev
```

Then open the printed local URL (usually http://localhost:8080).

For a personalized link, add the guest query parameter:

```
http://localhost:8080/?guest=Auntie+Fatima+%26+Family
```

## Build for production

```sh
npm run build
npm run preview
```

## Tests

```sh
npm test
```

## Project layout

```
src/
  routes/
    __root.tsx        # shared shell, fonts, error boundary
    index.tsx         # the invitation (envelope, card, curtains)
  components/
    invitation-interactions.tsx  # countdown + scratch-to-reveal canvas
    ui/                          # shadcn/ui primitives
  assets/            # couple portrait, curtain texture, floral corner
  styles.css         # Tailwind v4 theme + all invitation styling
```

## Deploying

The build targets Cloudflare Workers via Nitro. Any static/node host works too —
`dist/` is produced by `npm run build`.
