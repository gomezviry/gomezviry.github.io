# Apps support site

A single GitHub Pages site that hosts support and privacy pages for all my
apps. Each app lives under its own path prefix.

## URLs

- `/` — landing, lists all apps
- `/moop/support/` — Moop support page
- `/moop/privacy/` — Moop privacy policy

## Adding a new app

1. Create a folder: `site/<appname>/`
2. Add `support.md` and `privacy.md` with permalinks `/<appname>/support/`
   and `/<appname>/privacy/`.
3. Add a `defaults` entry in `_config.yml` so the layout picks up the
   `app` + `app_title` variables:

   ```yaml
   defaults:
     - scope: { path: "<appname>" }
       values: { app: <appname>, app_title: <App Name> }
   ```

4. Link to the new app from `index.md`.

## Recommended hosting

Put this site in its **own** repository (e.g. `support` or
`<username>.github.io`), separate from each app's source repo. Pages from a
project repo will be served at:

```
https://<username>.github.io/<repo-name>/moop/support/
```

Or, if you push to a user-site repo (`<username>.github.io`), simply:

```
https://<username>.github.io/moop/support/
```

## Publish

From the support-site repo root:

```bash
# Copy the contents of this site/ folder to the repo root, then:
git add .
git commit -m "Publish"
git push
```

Enable Pages in **Settings → Pages**, source `main` branch `/ (root)`.

## Preview locally

```bash
cd site
bundle init && echo 'gem "jekyll"' >> Gemfile && bundle install
bundle exec jekyll serve
```
