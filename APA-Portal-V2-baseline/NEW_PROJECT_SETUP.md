# APA Portal V2 — New Repository Baseline

This is an independent **starting point** copied from `Bodaga-main.zip` (source: `https://github.com/Bodaga/Bodaga`).

**Preservation:** All 49 original file entries are represented by 48 source files and one top-level directory in the uploaded source ZIP. All 48 non-directory files in this new ZIP have exactly the same contents (byte for byte) as the source. This copy contains one new documentation file (`NEW_PROJECT_SETUP.md`); no original file was edited. The original repository has not been touched.

## Create a separate GitHub repository

1. In GitHub, create a **new repository**, e.g. `APA-Portal-V2`, under your account. Do **not** fork the original repository. Avoid initializing it with a README, license, or .gitignore: they are included in this baseline as appropriate (the source already has `README.md` and `LICENSE`).
2. Download and **extract** `APA-Portal-V2-baseline.zip`. Upload its **contents** to the new repository, not the ZIP file itself. Ensure `index.html` is at the repository's top level.
3. Commit the uploaded files to the new repository's `main` branch.
4. Open repository **Settings → Pages**. For **Build and deployment**, select **Deploy from a branch**, branch **main**, folder **/(root)**, then save.
5. Once published, the site's URL should be `https://bodaga.github.io/APA-Portal-V2/` if you chose that exact name and use the Bodaga account.

The source `README.md` includes references to the original portal and still needs revising during the V2 development; it was deliberately not changed in this preservation-first baseline.

## Findings in the inherited code (to fix in later iterations)

- Static site: 46 HTML files, README and MIT license, no build pipeline or backend.
- Forms use test endpoint `https://httpbin.org/post` or show a local confirmation; submission does not store data in a private APA database.
- `intelligence.html` links to missing `file_media_suppression.html` and `submit_humint_sigint.html`.
- At least two location-brief pages link back to missing `logistics.html`; the actual logistics page is `site_logistics&engineering.html`.
- `stonehengeinarea.html` has malformed anchor markup.
- `biological_aberration_studies.html` and `project_felix.html` are just `TBA`.
- Some links are placeholders (`#`) and some requests are demonstrations rather than persistent records.
- Styling and navigation JavaScript are duplicated in individual pages, which makes larger changes hard to maintain.

**Security note:** GitHub Pages is a public static hosting service. The portal's `CLASSIFIED` / `UNAUTHORIZED ACCESS` language is fictional UI, not real authentication, security, or logging. Do not publish real secrets or sensitive personal data there.
