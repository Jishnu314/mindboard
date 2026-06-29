# Mind Board Security & Privacy

Mind Board is designed to run locally in the browser.

## Privacy model

- Board data is saved only in the user's browser `localStorage`.
- The app has no analytics, trackers, cookies, `fetch`, WebSocket, or beacon calls.
- The Content Security Policy blocks network connections with `connect-src 'none'`.
- Images are stored as local data URLs after the user selects or drops them.
- Exported HTML/JSON files contain the board data the user chooses to export.
- `localStorage` is not encrypted; anyone with access to the same browser profile may be able to inspect saved boards.


## Reporting issues

If you find a privacy or security issue, please open a GitHub issue with clear reproduction steps and avoid posting private board data publicly.
