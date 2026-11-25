# app-config

Public, read-only config files that the mobile apps fetch, served by GitHub Pages.

| App | File | URL |
|---|---|---|
| Water Sort Puzzle: Lagoon | `watersort/version.json` | https://parameswarisrk-lgtm.github.io/app-config/watersort/version.json |

## version.json
- `android.latestVersionCode`: newest versionCode live on Google Play. Installed builds below this get an optional "Update / Later" prompt.
- `android.minVersionCode`: installed builds below this get a forced update prompt. Only raise it for critical fixes.
- `ios.latestBuild` / `ios.minBuild`: the same for iOS build numbers.
- `message`: optional prompt texts.

**Release order:** publish the new build on Google Play, wait until it's live, and **then** raise the numbers here.
Never raise `min` before the build is live on Play. Changes reach the apps within ~10 minutes (Pages cache).

No secrets or private data belong in this repo.
