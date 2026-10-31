# AGENTS.md

Notes for AI coding agents working on this repository. Read this before making changes.

## What this is

This is the public template for Riverside Town, a Roku screensaver. People click "Use this template" to make their own repository, edit `town.json`, and download their screensaver from the "Build my town" workflow. The code that draws the town is in rorpage/riverside-town; this repository has no code of its own.

- `.github/workflows/build.yml` ("Build my town") runs on each push that changes `town.json` or the workflow. It builds the town with the `rorpage/riverside-town@v1` Action and attaches two downloads to the run: `riverside-town-roku` (the screensaver; it is uploaded to the Roku as it is, without unzipping) and `riverside-town-previews` (preview images). After the uploads, it deletes the downloads from earlier runs, so only the newest ones use storage space in the GitHub account. That step needs the `actions: write` permission; if the build fails, it does not run, and the last downloads that passed are kept.
- `README.md` is the guide for people who use the template. Keep it short, and link to the "town.json reference" in the README of rorpage/riverside-town for the details.
- `LICENSE` is The Unlicense, like rorpage/riverside-town.

## Rules

- Keep every file plain ASCII. Do not use em dashes or the Unicode ellipsis character.
- Use plain, literal language. Do not use idioms, figures of speech, or clever phrasing.
- `town.json` must be the same as the sample `town.json` in rorpage/riverside-town, except that this one uses `"location": { "zip": "46204", "country": "US" }` instead of lat and lon. When that file changes, copy it here and change the location and the `$schema` line (here it is the raw.githubusercontent.com URL of `tools/riverside/town.schema.json`).
- The sample town is generic on purpose: no real businesses, people, or references.
- Changes go straight to `main`; there are no pull requests in this repository.

## Using a new feature

The Action uses the published release of rorpage/riverside-town, so a `town.json` change that uses a new feature fails until that feature is released. Commit the change but do not push it. After the owner pushes the version tag and its `riverside-town-roku-generator` publish run passes, push the commit and check that the "Build my town" run passed and has both downloads.

## Testing

The owner tests every change on a Roku. Do not test on a Roku, and do not mention Roku testing in replies or commit messages.
