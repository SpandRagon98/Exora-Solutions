# EXORA SOLUTIONS

Single-page agency website for EXORA SOLUTIONS, prepared for direct GitHub Pages hosting.

## Files

- `index.html` - complete React single-page website with inline CSS and Babel-powered React components.
- `.github/workflows/deploy.yml` - GitHub Actions workflow for GitHub Pages deployment.
- `README.md` - deployment instructions.

No build tools, package installation, or framework setup is required.

## Automatic Deploy With GitHub Actions

This repository includes `.github/workflows/deploy.yml`, which deploys the static site to GitHub Pages whenever changes are pushed to `main`.

The workflow creates a clean `public` folder during the GitHub Actions run and copies only `index.html` plus a `.nojekyll` marker into it before deploying.

To enable it:

1. In GitHub, open the repository and go to `Settings > Pages`.
2. Under `Build and deployment`, set the source to `GitHub Actions`.
3. Push changes to the `main` branch, or manually run the `Deploy GitHub Pages` workflow from the `Actions` tab.

If GitHub Actions shows `Get Pages site failed`, Pages is not enabled for Actions yet. Go back to `Settings > Pages`, confirm the source is set to `GitHub Actions`, save the setting, then rerun the workflow.

Optional: to let the workflow enable GitHub Pages automatically on a brand-new repository, add a repository secret named `PAGES_ADMIN_TOKEN` with a token that has Pages write permission. The default `GITHUB_TOKEN` cannot enable Pages on a repository that has Pages turned off.

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
