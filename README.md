# Mind Board

Mind Board is a private, local-first visual thinking board for notes, connected idea cards, nested workspaces, templates, images, search, undo/redo, and offline exporting.

It runs as a single `index.html` file in the browser. No server is required.

## Features

- Visual canvas with draggable notes and idea cards
- Connect cards with styled relationship lines
- Nested boards by opening a card as its own workspace
- Templates for brainstorming, project planning, research, Kanban, journeys, and decisions
- Local image attachments
- Search, minimap, keyboard shortcuts, auto-arrange, fit view, undo, and redo
- Export/import as JSON
- Download the current board or selected card workspace as a standalone HTML file
- Local-only Star button that can open your GitHub repo for a manual star

## Privacy

Mind Board is designed to be private by default.

- Your board is saved in your browser using `localStorage`.
- There are no analytics, trackers, cookies, hidden requests, WebSockets, or beacons.
- The Content Security Policy blocks network connections with `connect-src 'none'`.
- Images stay inside the local board data as browser data URLs.
- Exported HTML/JSON files contain the board data you choose to export.

Note: `localStorage` is not encrypted. Anyone with access to the same browser profile may be able to inspect saved boards.

## Use Locally

Download or clone this repository, then open:

```text
index.html
```

You can use it directly from your filesystem in a modern browser.

## Publish On GitHub

Put these files in the root of your GitHub repository:

```text
index.html
README.md
SECURITY.md
```

Before publishing, update the repository URL in `index.html`:

```js
const GITHUB_REPO_URL = 'https://github.com/your-username/mind-board';
```

Replace it with your real repo URL. The Star button cannot automatically star a repository, because GitHub requires the user to choose that action. It stores a small local like count and opens the repo so the user can star it manually.

## Recommended GitHub Pages Setup

1. Open your repository settings.
2. Go to **Pages**.
3. Set the source to your main branch.
4. Keep the root folder selected.
5. Save and open the generated GitHub Pages URL.

## Security

See [SECURITY.md](SECURITY.md) for the security and privacy notes.

## License

Add your preferred open-source license before publishing. MIT is a common choice for small browser tools.
