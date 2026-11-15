# Best Man Games

Documentation site for the annual Best Man Games, built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and published with GitHub Pages.

## Layout

| Folder | What lives there |
| --- | --- |
| `docs/rules/` | Rules that apply all weekend: scoring, teams, bonus chugs, power plays, tie breaker, last place |
| `docs/games/` | The **game pool**: one page per game, grouped by `individual/`, `two-player/`, `five-player/` |
| `docs/years/` | One page per year: event details, the lineup actually played, and any rule changes for that year |

## Preview locally

```bash
pip install -r requirements.txt
```

```bash
mkdocs serve
```

Then open http://127.0.0.1:8000.

## Add a new game to the pool

1. Copy an existing page from the matching format folder in `docs/games/`.
2. Fill in setup, rules, and supplies.
3. Add it to the table in `docs/games/index.md` and to `nav:` in `mkdocs.yml`.

## Add a new year

1. Copy `docs/years/2025.md` to `docs/years/<year>.md`.
2. Update the event details and the lineup table, linking each game to its pool page.
3. Add the year to `docs/years/index.md` and to `nav:` in `mkdocs.yml`.
4. Add the year to the "Played" line on each game page and in `docs/games/index.md`.

## Publish

Pushing to `main` runs `.github/workflows/deploy.yml`, which builds the site and deploys it to GitHub Pages (repo Settings → Pages → Source: GitHub Actions).
