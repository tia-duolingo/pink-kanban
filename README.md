# Pink Kanban ★

A retro-pink Kanban app — single-file HTML, no build step, no backend. Open `index.html` in a browser to use it.

## Features

- **Multiple boards** — switch via the tabs in the header. Comes seeded with **Work** and **Personal**.
- **Drag-and-drop cards** between columns (and within a column to reorder).
- **Customizable columns** — add, rename (click the title), and delete per board.
- **Card details** — click any card to set description, due date, and comma-separated tags. Due dates show as cyan; turn yellow when due within 2 days, red when overdue.
- **Export / Import** as JSON — backup, move between machines, or share a snapshot.
- **Local storage** — your data lives in your browser (key: `pink-kanban:v1`).

## Hosting on GitHub Pages

This is a static site, so GitHub Pages is free and quick. The page will be **view-only for visitors** (each visitor gets their own local copy of the data the moment they start interacting), which matches what you asked for.

```bash
cd "My Kanban"
git init
git add index.html README.md
git commit -m "Initial commit: Pink Kanban"
git branch -M main
# Create a repo at github.com/<you>/pink-kanban first, then:
git remote add origin https://github.com/<you>/pink-kanban.git
git push -u origin main
```

Then on GitHub:
1. Go to your repo → **Settings** → **Pages**.
2. Under **Source**, pick **Deploy from a branch** → **main** → **/ (root)** → **Save**.
3. After ~1 minute, your board is live at `https://<you>.github.io/pink-kanban/`.

Share that URL. Each visitor sees the seeded boards and can play with their own copy. To share *your* actual board content, hit **Export** to download a JSON file and send it; the recipient hits **Import** to load it.

## Notes

- Data is per-browser. Clearing site data wipes your boards — export every so often.
- All assets are bundled in one HTML file (only Google Fonts + the CSS/JS inline). Works offline after first load.
- Tested in modern Chrome, Safari, Firefox.
