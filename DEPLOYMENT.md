# Source and Deployment Strategy

This repository should use two branches with different responsibilities.

## Branches

- `source`: Hexo source branch. Keep `_config.yml`, `_config.fluid.yml`, `package.json`, `source/`, `scaffolds/`, and writing assets here.
- `master`: GitHub Pages publishing branch. Keep only generated static files from `public/` here.

A useful materials-science analogy: `source` is the complete experiment notebook, raw data, scripts, and interpretation; `master` is the exported figure set that readers see.

## First-time setup

```bash
npm install
npm run server
```

Open the local server and check the pages before publishing.

## Publishing workflow

Work from the `source` branch:

```bash
npm run check
npm run deploy
```

`hexo-deployer-git` will generate `public/` and push the static result to `master`.

## Rules of thumb

- Do not edit generated HTML in `master` by hand unless it is an emergency hotfix.
- Put new posts in `source/_posts/`.
- Put images referenced by configuration or posts in `source/img/` or each post asset folder.
- Keep `public/`, `.deploy_git/`, and `node_modules/` out of the `source` branch.
- Commit `package-lock.json` after `npm install` so future builds use the same dependency versions.
- Run `npm run check` before `npm run deploy`; treat build failures like failed data validation before plotting a final figure.
