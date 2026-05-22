# rowandempster.github.io

Personal site built with [Jekyll](https://jekyllrb.com/) and [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes), published via [GitHub Pages](https://pages.github.com/versions.json).

Source lives in `docs/`. No local Ruby install required—use Docker.

## Local development

**Prerequisites:** Docker and Docker Compose.

```bash
# Install gems from the committed lockfile (reproducible; run after lockfile changes)
docker compose build site

# Dev server (first run may take ~2 min while the remote theme downloads)
docker compose run --rm --service-ports site
```

Open http://localhost:4000 — stop with `Ctrl+C`.

The image runs `bundle install` at build time from `docs/Gemfile.lock`. Day-to-day dev does not re-resolve gems.

## Updating dependencies

Only when you change `docs/Gemfile` (e.g. bump `github-pages` per [versions.json](https://pages.github.com/versions.json)):

1. Edit `docs/Gemfile`.
2. Refresh the lockfile (writes to your repo via the `docs/` volume mount):

```bash
docker compose build site
docker compose run --rm site bundle update github-pages
```

For a **new** gem already listed in the Gemfile but not in the lockfile, use `bundle install` instead of `bundle update <gem>`.

3. Commit `docs/Gemfile` and `docs/Gemfile.lock`.
4. Rebuild the image: `docker compose build site`.

## Deploy to GitHub Pages

1. Commit and push on your default branch (e.g. `main`).
2. On GitHub: **Settings → Pages → Build and deployment**.
3. **Source:** Deploy from a branch → your default branch → folder **`/docs`**.

GitHub builds with the same `github-pages` stack. Do not commit `docs/_site/` (see `docs/.gitignore`).

## Project layout

| Path | Purpose |
|------|---------|
| `docs/` | Jekyll source (posts, pages, config, assets) |
| `docs/_config.yml` | Site configuration |
| `docker/Dockerfile.docs` | Dev image (`bundle install` from lockfile) |
| `docker-compose.yaml` | Local serve workflow |
