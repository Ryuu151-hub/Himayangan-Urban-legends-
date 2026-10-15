# Video Showcase – Dark Minimal

A ready-to-use Astro website that displays videos stored in the GitHub repository.  
**Title and date are editable** by simply changing a JSON file.

Based on the **Dark Minimal** design by Andres Hernandez / ThemeWagon.

---

## How it works

1. Put your `.mp4` files inside `public/videos/`
2. Edit `src/data/videos.json` (or the copy in `data/videos.json`) to set **title**, **date** and **description**
3. Push to GitHub → Vercel automatically rebuilds and deploys

---

## Quick start

```bash
# Install dependencies
npm install
# or
pnpm install

# Run locally
npm run dev
```

Open http://localhost:4321

---

## Adding / editing a video

### 1. Upload the video
Put the file here:

```
public/videos/my-video.mp4
```

### 2. Edit the metadata
Open `src/data/videos.json` and add (or change) an entry:

```json
[
  {
    "id": "my-video",
    "title": "My Awesome Video",
    "date": "2026-10-15",
    "description": "Optional short description that appears under the title.",
    "filename": "my-video.mp4"
  }
]
```

You can change the **title** and **date** anytime just by editing this file on GitHub.

### 3. Push
Commit & push. Vercel will redeploy automatically (usually < 1 minute).

---

## Deploy to Vercel

1. Create a new GitHub repository and push this project
2. Go to [vercel.com](https://vercel.com) → **New Project** → Import the repo
3. Framework Preset: **Astro** (auto-detected)
4. Click **Deploy**

Done. Every future push (new video or updated title/date) will update the live site.

---

## Project structure

```
├── public/
│   └── videos/              ← drop your .mp4 files here
├── src/
│   ├── data/
│   │   └── videos.json      ← edit titles & dates here
│   ├── components/
│   │   ├── videos.astro     ← the video gallery
│   │   ├── home.astro
│   │   ├── nav.astro
│   │   ├── contact.astro
│   │   └── footer.astro
│   ├── layouts/
│   └── pages/
└── ...
```

---

## Notes

- Keep individual video files under ~100 MB (GitHub soft limit).
- For very large videos later you can switch to a CDN or embed YouTube/Vimeo.
- Contact form uses Formspree – replace `YOUR_FORM_ID_HERE` in `src/components/contact.astro` with your own form ID.
- Design credit: Dark Minimal template by Andres Hernandez (ThemeWagon).
