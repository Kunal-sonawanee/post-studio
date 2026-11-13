# Thought Post Studio

Free tool by **Kantex Technologies** (Nashik) to make Instagram "thought" posts: one photo + one strong line, in a brand's own look.

- 4 brands: Hotel New Sadguru, Pravin Caterers & Events, Kantex, plus **Your brand** (custom colours, logo, letter mark)
- 4 styles: Glass card, Editorial, Split, Paper note
- 3 sizes: 1080×1350 (4:5 post), 1080×1080 (square), 1080×1920 (story; text kept in Instagram's safe area)
- Marathi, Hindi and English fonts (Tiro Devanagari Marathi, Martel, Mukta, Kalam)
- Download PNG, or on phones: Share / Save to gallery
- 100% in the browser: photos never leave the device. Brand details are saved in the browser (localStorage).

## Stack

A single static `index.html`, no build step, no backend.

## Deploy (Cloudflare Pages)

Workers & Pages → Create → Pages → Connect to Git → pick this repo.

- Framework preset: **None**
- Build command: *(leave empty)*
- Build output directory: `/`

Every push to `main` redeploys automatically.

## Later

- AI line suggestions via a Pages Function (`/functions/api/suggest.js`) calling the Claude API, with rate limiting.
- Per-client brand presets loaded from a JSON file.
