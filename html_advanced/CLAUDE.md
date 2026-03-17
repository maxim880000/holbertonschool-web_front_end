# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Workspace Structure

This is a multi-project home directory. Each subdirectory is an independent project:

| Directory | Type | Stack |
|-----------|------|-------|
| `pixel-agents/` | VS Code extension | TypeScript, React (Vite), VS Code API |
| `WebNovate/` | Web agency booking site | Node.js, vanilla JS, SQLite, Vercel |
| `holbertonschool-hbnb/` | REST API (3 parts) | Python, Flask, Flask-RESTX |
| `holbertonschool-higher_level_programming/` | Python exercises | Python |
| `holbertonschool-low_level_programming/` | C exercises | C |
| `holbertonschool-web_front_end/` | Frontend exercises | HTML, CSS |
| `ARDET/` | Static site | HTML, CSS, JS |
| `course/` | Web course exercises | HTML, CSS, JS |

---

## pixel-agents — VS Code Extension

See `pixel-agents/CLAUDE.md` for the full reference. Summary:

### Commands
```sh
# Install dependencies (both extension + webview)
npm install && cd webview-ui && npm install && cd ..

# Build (type-check → lint → esbuild + vite)
npm run build

# Type-check only
npm run check-types

# Lint
npm run lint          # extension src/
npm run lint:webview  # webview-ui/

# Format (Prettier)
npm run format

# Dev watch mode
npm run watch

# Press F5 in VS Code to launch Extension Development Host
```

### Architecture
- `src/` — Extension backend (Node.js, VS Code API): agent/terminal management, JSONL file watching, asset loading
- `webview-ui/src/` — React + TypeScript (Vite): pixel art canvas, game loop, layout editor, character FSM
- Communication via `postMessage` between extension host and webview
- Layout persisted to `~/.pixel-agents/layout.json` (user-level, shared across workspaces)
- Agent state tracked by tailing `~/.claude/projects/<hash>/<session>.jsonl` transcripts

---

## WebNovate — Booking Site

### Commands
```sh
cd WebNovate
npm install

# Local development server (http://localhost:8000)
npm run dev
# or
node scripts/dev-server.js

# Deploy to Vercel
bash scripts/deploy.sh
# or
vercel deploy --prod
```

### Architecture
- `src/index.html` + `src/style.css` + `src/script.js` — Single-page site with booking calendar UI
- `api/bookings.js` — Vercel serverless function: handles `POST /api/bookings`, sends confirmation emails via Gmail (nodemailer)
- `data/bookings.db` — SQLite (dev only; Vercel functions are ephemeral)
- Environment variables: `GMAIL_USER`, `GMAIL_PASSWORD` (Gmail App Password) — see `config/.env.example`
- `vercel.json` — Routes `api/bookings` to the serverless handler

---

## holbertonschool-hbnb — Flask REST API

Three progressive parts (part1: design/UML, part2: Flask API, part3: Flask + SQLAlchemy).

### Commands
```sh
cd holbertonschool-hbnb/part2   # or part3

# Install dependencies
pip install -r requirements.txt

# Run development server
python run.py
# Serves on http://localhost:5000

# Run curl test suite
bash curl_tests.sh
```

### Architecture (part2/part3)
- `run.py` — Entry point: `create_app()` → Flask dev server
- `app/` — Application package with Flask-RESTX namespaces (users, places, reviews, amenities)
- `config.py` — Environment-based configuration
- part3 adds SQLAlchemy models and a real database backend
