KeepFlame — Support & Privacy Site (source)

This directory contains the static pages shown to users for Support, Privacy Policy and Terms. The site is simple, fast, and free of tracking.

Links (examples)
- English: `/en/index.html`, `/en/privacy.html`, `/en/terms.html`
- 简体中文: `/zh-Hans/index.html`, `/zh-Hans/privacy.html`, `/zh-Hans/terms.html`
- 繁體中文: `/zh-Hant/index.html`, `/zh-Hant/privacy.html`, `/zh-Hant/terms.html`
- 日本語: `/ja/index.html`, `/ja/privacy.html`, `/ja/terms.html`

Contact: renqilian@gmail.com

---

Workflow (themes on index)
- The language home pages (en/zh-Hans/zh-Hant/ja) embed a "Themes & Animations" gallery that shows preview frames from built‑in video themes.
- Poster images live under `docs/public-site/docs/assets/themes/<Theme>/<FileBase>.jpg` and are generated from the first frame of the existing videos in `Art/ThemeVideo/`.

Generate posters (requires ffmpeg)
1) Install ffmpeg if missing: `brew install ffmpeg`.
2) Run: `bash scripts/generate_theme_posters.sh`
   - Outputs JPG files to `docs/public-site/docs/assets/themes/...`

Publish to your Pages repo
1) Sync the `docs/public-site/` folder to your external repo: `bash scripts/sync_support_site.sh`.
2) In the destination repo: `git add -A && git commit -m "docs: update support site (themes on index)" && git push`.

Notes
- We intentionally keep video previews as static frames for performance and bandwidth.
- If you change which clips to showcase, edit `scripts/generate_theme_posters.sh` (the PICK lists).
