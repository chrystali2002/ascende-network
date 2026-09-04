# Monthly Update Workflow

This project is updated monthly. Follow the steps below to prepare and publish each new session flyer and content.

---

## 1. Prepare the new flyer
- Export the raw flyer.
- Optimize it:
  - Resize to ~1000px width  
  - Compress to JPG at quality 82 (Pillow, LANCZOS resampling)  
  - Target file size: 150–250 KB  
- Name the file consistently (e.g., `oct-edition.jpg`, following the existing pattern:  
  `sept-edition.jpg`, `august-flyer.jpg`, etc.).

---

## 2. Upload the flyer to `assets/`
- Open the `assets/` folder in GitHub.
- Select **Add file → Upload files**.
- Drag in the optimized flyer and commit to `main`.

---

## 3. Update the “Next Session” hero section
In `index.html`:

- Locate the `<a>` and `<img>` tags near `id="session"`.
- Update the `src` and `href` attributes to the new filename.
- Update the `alt` text.
- Update the eyebrow text (e.g., “September edition” → “October edition”).

---

## 4. Update session details
Still in the `#session` section:

- Update the session title/theme.
- Update the speaker name and bio line.
- Update the host line.
- Update the Date and Time in the details list.
- Update the “Join the [Month] session” button text in the hero.
- Update the flyer download link.

---

## 5. Add the new flyer to the gallery
In the `#past` section:

- Add a new `<figure>` at the top (most recent first).
- Include the new image, correct `<time datetime>` value, and a short caption describing the session topic.

---

## 6. Update Event structured data (JSON‑LD)
In the `<head>`:

- Find the `<script type="application/ld+json">` block.
- Update:
  - `name`
  - `startDate` and `endDate`
  - `image` (new flyer path)
  - `description`
  - `performer`
- Ensure the data matches the current session so Google can display accurate rich results.

---

## 7. Update meta tags for search/social previews
Update:

- `<title>`
- Meta description
- Open Graph tags (`og:title`, `og:description`, `og:image`)
- Twitter card tags

These ensure correct previews when the link is shared.

---

## 8. Deploy and verify
- Commit `index.html` to `main`.
- Wait ~30–60 seconds for GitHub Pages to rebuild.
- Hard refresh (`Ctrl+Shift+R`) or use an incognito window to verify:
  - New flyer
  - Updated gallery
  - Updated session details
  - Correct social preview

---
