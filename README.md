# Apps support site

Static Jekyll site for GitHub Pages. Hosts homepage, support, and privacy
pages for all my apps under per-app path prefixes.

## URLs

- `/` — top-level landing, lists all apps
- `/moop/` — Moop homepage *(the page to submit to Google OAuth verification)*
- `/moop/support/` — Moop support / FAQ
- `/moop/privacy/` — Moop privacy policy

## Adding a new app

1. Create a folder: `site/<appname>/`
2. Add `index.md`, `support.md`, `privacy.md` with the matching permalinks
   `/<appname>/`, `/<appname>/support/`, `/<appname>/privacy/`.
3. Add a `defaults` block in `_config.yml`:

   ```yaml
   - scope: { path: "<appname>" }
     values: { app: <appname>, app_title: <App Name> }
   ```

4. Link the new app from the top-level `index.md`.

## Hosting

Put this site in its own dedicated repo (e.g. `<username>.github.io` or a
project repo named `support`). For Google OAuth verification, the homepage
URL you submit on the consent screen must match the privacy policy URL's
domain — using one site for both is the simplest way to satisfy that.

```
https://<username>.github.io/moop/            # homepage
https://<username>.github.io/moop/privacy/    # privacy policy
```

## Publish

From the support-site repo root:

```bash
# Copy contents of this site/ folder to the repo root.
git add .
git commit -m "Publish"
git push
```

Then enable Pages in **Settings → Pages**, source `main` branch, `/ (root)`.

## Preview locally

```bash
cd site
bundle init && echo 'gem "jekyll"' >> Gemfile && bundle install
bundle exec jekyll serve
```
