# EXORA SOLUTIONS

Single-page agency website for EXORA SOLUTIONS, prepared for direct GitHub Pages hosting.

## Files

- `index.html` - complete React single-page website with inline CSS and Babel-powered React components.
- `.github/workflows/deploy.yml` - GitHub Actions workflow for GitHub Pages deployment.
- `README.md` - deployment instructions.

No build tools, package installation, or framework setup is required.

## Automatic Deploy With GitHub Actions

This repository includes `.github/workflows/deploy.yml`, which publishes the static site to a `gh-pages` branch whenever changes are pushed to `main`.

The workflow creates a clean deployment folder during the GitHub Actions run and publishes only `index.html` plus a `.nojekyll` marker to the `gh-pages` branch.

To enable it:

1. In GitHub, open the repository and go to `Settings > Pages`.
2. Under `Build and deployment`, set the source to `Deploy from a branch`.
3. Choose:
   - Branch: `gh-pages`
   - Folder: `/ (root)`
4. Save the settings.
5. Push changes to the `main` branch, or manually run the `Deploy GitHub Pages` workflow from the `Actions` tab.

If the `gh-pages` branch is not available in the Pages settings yet, run the `Deploy GitHub Pages` workflow once from the `Actions` tab. The workflow creates the branch.

If GitHub Actions cannot push the `gh-pages` branch, go to `Settings > Actions > General > Workflow permissions` and select `Read and write permissions`.

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
