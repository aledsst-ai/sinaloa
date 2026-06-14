---
name: sinaloa-rebrand
description: Rebrand the entire Sinaloa project to a new FiveM illegal faction name
---

## Overview
This skill guides the complete rebranding of the Sinaloa dashboard to a new FiveM illegal faction. Follow every step below.

## Steps

### 1. Copy the project
- Create a new folder for the new faction (e.g., `CartelNorte`)
- Copy all files from the Sinaloa project to the new folder
- Remove `.git` directory from the copy
- Remove `SETUP_INSTRUCTIONS.md` from the copy

### 2. Firebase project
- Create a new Firebase project (e.g., `cartel-norte-mtp`)
- Enable Authentication with Email/Password
- Create admin and members accounts with the new domain email
- Create a Realtime Database in test mode initially
- Copy the new Firebase config (apiKey, authDomain, databaseURL, etc.)

### 3. Configuration files to update
- `js/config.js` — Firebase config, `dbPath`, localStorage key prefix, site name
- `gallery.html` — Firebase config, og:url, og:image, title
- `apreensoes.html` — Firebase config, og:url, og:image, title
- `index.html` — Firebase config, og:url, og:image, title
- `database.rules.json` — Update email domain rule to new domain

### 4. Text rebranding
- `FACÇÃO` → new faction name (e.g., `CARTEL`)
- `Membro` → new member title (e.g., `Sicário`)
- `Veículos` → if needed
- `Operações` → if needed
- Admin panel texts in `js/admin.js`, `ui.js`, `app.js`
- UI labels, placeholders, alerts, confirm dialogs

### 5. Logo
- Update logo path/URL to the new faction logo
- Change references in `sections/header/header.html`, `sections/sobre/sobre.html`, and all standalone HTML files

### 6. Branding properties
- Colors: update CSS variables in `style.css` if the new faction has different colors
- og:url — set to the new deploy URL
- og:image — set to the absolute URL of the new logo

### 7. Deploy
- Set up git for the new project
- Create a new Cloudflare Pages project (or Workers)
- Push and configure auto-deploy

### 8. Verification
- Run `build.ps1` to rebuild `index.html`
- Search for any remaining references to the old name with `grep`
- Open each HTML file and verify Firebase config matches the new project
