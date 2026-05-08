# EXORA SOLUTIONS

Single-page agency website for EXORA SOLUTIONS, prepared for direct GitHub Pages hosting.

## Files

- `index.html` - complete React single-page website with inline CSS and Babel-powered React components.
- `README.md` - deployment instructions.

No build tools, package installation, or framework setup is required.

## Automatic Deploy With GitHub Actions

This repository includes `.github/workflows/deploy.yaml`, which deploys the static site to GitHub Pages whenever changes are pushed to `main`.

To enable it:

1. In GitHub, open the repository and go to `Settings > Pages`.
2. Under `Build and deployment`, set the source to `GitHub Actions`.
3. Push changes to the `main` branch, or manually run the `Deploy GitHub Pages` workflow from the `Actions` tab.

## Manual Deploy To GitHub Pages

1. Upload `index.html` and `README.md` to your GitHub repository:
   `https://github.com/SpandRagon98/Exora-Solutions`
2. Make sure both files are in the repository root, not inside a subfolder.
3. In GitHub, open the repository and go to `Settings > Pages`.
4. Under `Build and deployment`, set the source to `Deploy from a branch`.
5. Choose:
   - Branch: `main`
   - Folder: `/ (root)`
6. Save the settings.

GitHub Pages will publish the site at:

```text
https://USERNAME.github.io/REPOSITORY-NAME/
```

For this repository, the expected URL is:

```text
https://SpandRagon98.github.io/Exora-Solutions/
```

## Notes

- The site uses React, ReactDOM, and Babel from public CDNs, so it can run directly in the browser.
- Internal section links such as `#services`, `#cases`, `#estimator`, and `#contact` are supported.
- The website is intentionally kept as a single-file React page for simple GitHub Pages hosting.
