# Game Hub

A tiny arcade site. `index.html` is the home page with a card for each game;
each game lives in `/games` as its own self-contained HTML file.

## Put this live on GitHub Pages (one-time setup)

1. Go to github.com and create a free account if you don't have one.
2. Click **New repository**. Name it anything (e.g. `game-hub`). Keep it Public.
3. On the new repo's page, click **uploading an existing file** (or "Add file" →
   "Upload files").
4. Drag in everything from inside this folder — `index.html`, the `games`
   folder, and this `README.md` — keeping the same structure. Commit the
   changes.
5. In the repo, go to **Settings → Pages**.
6. Under "Build and deployment", set **Source** to "Deploy from a branch",
   branch = `main`, folder = `/ (root)`. Save.
7. Wait ~1 minute. Your site is now live at:
   `https://YOUR-USERNAME.github.io/game-hub/`
   (GitHub shows you the exact URL on that same Settings → Pages screen.)

No domain, no cost, no server to maintain.

## Adding a new game later

Two steps, every time:

1. Drop the new game's `.html` file into the `games` folder.
2. Open `index.html`, find the `GAMES` list near the top of the `<script>`
   section, and add one entry for it, e.g.:

   ```js
   {
     title: "Your Game Name",
     file: "games/yourgame.html",
     icon: "🎮",
     color: "#4FBDB4",
     desc: "One short line describing it."
   }
   ```

3. Upload/commit both the new file and the updated `index.html` to the repo
   (same "Add file → Upload files" flow, or drag the changed files into the
   repo on github.com — it'll ask if you want to replace `index.html`, say
   yes). GitHub Pages redeploys automatically within a minute or so.

That's it — no build step, no other files to touch.

## Notes

- Each game has a small "← Games" link in its top-left corner to get back to
  this home page.
- Every game saves its own progress/best-score locally in the visitor's own
  browser (nothing is shared between players, and nothing is stored on a
  server).
