# Where The Trail Ends — docs

This repo is the documentation source for **Where The Trail Ends**, the game. Pages are written in Markdown/MDX and published through [ReadMe](https://readme.com). Every page here, including guides and API reference config, shows up on the docs site.

## Layout

- `docs/<Category>/*.md` — guide pages.
- `reference/ReadMeConfig/*.md` — API-page config stubs (frontmatter only).
- `_order.yaml` — sidebar order for its folder. One slug per line; each slug must match a filename (without `.md`) or folder name.

## Branches

`v1.0` is the default branch and the published version: ReadMe syncs docs version `v1.0` from it. `main` also exists on origin but is not the published version. Open pull requests against `v1.0`.

## Frontmatter cheatsheet

```yaml
title: Page title          # required, shown in the sidebar and page header
excerpt: One-line summary  # shown under the title
hidden: true               # true keeps the page off the published site
icon: icon-key1            # sidebar icon
link:
  new_tab: false           # open link pages in a new tab
```

## Commands

The easiest way to work on the docs locally is with the [`@readme/cli`](https://www.npmjs.com/package/@readme/cli).

Lint the docs (run this before every push; CI runs it too):

```sh
npx @readme/cli lint
```

Configure linting for every branch via GitHub Actions:

```sh
npx @readme/cli setup:github
```

Or view the full list. You can preview docs locally, validate your OAS specs and more:

```sh
npx @readme/cli --help
```
