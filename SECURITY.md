# Mind Board Security & Privacy

Mind Board is designed to run locally in the browser.

## Privacy model

- Board data is saved only in the user's browser `localStorage`.
- The app has no analytics, trackers, cookies, `fetch`, WebSocket, or beacon calls.
- The Content Security Policy blocks network connections with `connect-src 'none'`.
- Images are stored as local data URLs after the user selects or drops them.
- Exported HTML/JSON files contain the board data the user chooses to export.
- `localStorage` is not encrypted; anyone with access to the same browser profile may be able to inspect saved boards.

## GitHub star button

GitHub stars cannot and should not be added automatically. The Star button only stores a local like count in the user's browser and, after `GITHUB_REPO_URL` is updated in `index.html`, opens the GitHub repository in a new tab so the user can star it manually.

Before publishing, replace:

```js
const GITHUB_REPO_URL = 'https://github.com/your-username/mind-board';
```

with your real repository URL.

## Reporting issues

If you find a privacy or security issue, please open a GitHub issue with clear reproduction steps and avoid posting private board data publicly.
