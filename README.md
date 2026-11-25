# rajasthan_helpline

One home for all my Material Design 2 apps (live site: https://anant0418.github.io/rajasthan_helpline/). Each app lives in its own folder under `apps/`.

| App | Kind | Folder | Status |
|---|---|---|---|
| Sugam Dial | Website (installable, works offline) | [`apps/sugam-dial`](apps/sugam-dial) | Live on GitHub Pages |
| Dialer | Android (Kotlin) | `apps/dialer` | To be moved in |
| ManualCam | Android (Kotlin, Camera2) | `apps/manualcam` | To be moved in |

## Websites

Every folder under `apps/` that has an `index.html` is published by
[`.github/workflows/pages.yml`](.github/workflows/pages.yml) to GitHub Pages at
`https://anant0418.github.io/rajasthan_helpline/<folder>/`.

One-time setup: **Settings → Pages → Build and deployment → Source: GitHub Actions**.

## Android apps

When Dialer and ManualCam move in, each keeps its own Gradle project inside its folder, and its
APK workflow builds only when files in that folder change (`paths: apps/<name>/**`).

## Adding an app

1. Create `apps/<name>/` with the app and a `README.md`.
2. Add a row to the table above.
