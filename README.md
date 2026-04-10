# WeatherWise

**WeatherWise** is a social, human-centered weather companion. It turns raw forecast data into **short, actionable tips**—not charts and numbers. Think: *Should I take an umbrella? What should I wear? Is now a good time to go outside?*

Built for hackathon demos and real daily use, with room to grow into a fuller social layer (friends’ conditions, shared tips, and personalized “should I?” answers).

## What it does

- Ingests weather from a public API and normalizes it into a stable internal shape.
- Runs a small **recommendation layer** (LLM-assisted prompts) to produce **1–3 concise tips** per request.
- Supports **tip categories**: Clothing, Umbrella, Go outside?, Travel, Evening plans.
- Plans for **“My Day”** (hourly one-liners + icons), **“Should I?”** quick queries, **user personas**, a **social feed**, and **graceful degradation** when data is partial.

## Tech stack

**To be decided** during implementation. Likely directions:

| Layer        | Options (pick one or combine)                          |
| ------------ | ----------------------------------------------------- |
| API / backend| Node (Express/Fastify), Python (FastAPI), or similar |
| Frontend     | React / Vue / Svelte, or a static + API split         |
| Weather      | [Open-Meteo](https://open-meteo.com/) (no key) or [OpenWeatherMap](https://openweathermap.org/api) |
| LLM          | Provider TBD (API key via env, never committed)     |
| Containers   | Docker + Compose for API + frontend + optional DB     |

The repo is intentionally **scaffolding-only** until the stack is chosen.

## Repository layout

```
weatherwise/
├── README.md           # This file
├── TODO.md             # Feature checklist (mirror for GitHub Project if you use one)
├── .gitignore
├── backend/            # REST API (placeholder)
├── frontend/           # Mini-app / widget (placeholder)
└── docker/             # Dockerfiles & compose (placeholder)
```

## Prerequisites

- **Git**
- **GitHub CLI** (`gh`) if you want one-command repo create/push (install: [cli.github.com](https://cli.github.com/))
- Runtime tooling will be listed here once the stack is fixed (e.g. Node ≥ 20, Python ≥ 3.11, Docker).

## Run locally

Not wired yet—folders are placeholders.

After you add a backend and/or frontend:

1. Copy `.env.example` (when added) to `.env` and fill API keys and base URLs.
2. Follow stack-specific steps in `backend/README.md` and `frontend/README.md` once those exist.
3. With Docker: `docker compose up` (after `docker-compose.yml` is added under `docker/` or repo root).

## Publishing to GitHub (with `gh`)

From this directory, after `gh auth login`:

```bash
git init   # skip if already initialized
git add .
git commit -m "chore: initial WeatherWise scaffold"
gh repo create weatherwise --public --source=. --remote=origin --push
```

Use another repo name or `--private` if you prefer.

### Optional: GitHub Project board

If your `gh` version supports projects:

```bash
gh project create --owner YOUR_GITHUB_USERNAME --title "WeatherWise"
```

Then add the same items as in `TODO.md` as board cards, or use **Projects → New project** in the GitHub UI and import tasks from this file.

## License

Add a `LICENSE` file before open-sourcing or submitting to a hackathon, if required.
