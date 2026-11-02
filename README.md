# Sridhar Lab website

A static, GitHub Pages-ready recreation of [vivekhsridhar.com](https://www.vivekhsridhar.com), preserving the current visual identity and content as the starting point for a new website.

The site includes Home, Team, Research, all 15 publication entries, the SciComm feed, and its five full articles. Photos, the Poppins font, research videos, the exhibition film, and the panel audio are hosted locally. YouTube videos use direct embeds and provide a link to watch on YouTube.

## Edit the site

- **Text, people, publications, and articles:** `content/site.json`. Rich text uses small HTML strings, so links, bold text, and italics are preserved.
- **Colors, spacing, fonts, and responsive layouts:** `assets/site.css`.
- **Navigation and shared page markup:** `scripts/build.py`.
- **Mobile menu:** `assets/site.js`.
- **Photos, video, and audio:** `assets/`.

The original image URLs are recorded in `content/asset-sources.json` for reference. The website does not fetch from those URLs at runtime.

## Preview on your computer

Python 3.10 or later is sufficient; no additional packages are required.

```bash
python3 scripts/build.py
python3 scripts/check.py
python3 -m http.server 8000 --directory dist
```

Visit `http://localhost:8000`. Re-run the build and refresh after editing.

## Publish with GitHub Pages

The included GitHub Actions workflow builds and deploys every push to `main`.

1. In the repository, open **Settings → Pages**.
2. Select **GitHub Actions** as the build and deployment source.
3. Run **Build and deploy GitHub Pages** from the Actions tab, or push an edit to `main`.

Relative links work both at `username.github.io` and under a project repository such as `username.github.io/sridhar-lab/`. The workflow sets canonical URLs and the sitemap from the configured Pages address.

No custom domain is configured by this project. To move the existing domain later, configure it in GitHub Pages and update the domain's DNS only once the new site is ready.

## Rights

Website text, images, logo, video, and audio retain their original ownership and credits. Their inclusion in this personal site does not grant permission for reuse. The MELA film's original non-commercial and protected-area footage notice is preserved in its article. Poppins is distributed under the SIL Open Font License, included in `assets/fonts/OFL.txt`.
