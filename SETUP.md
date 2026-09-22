# GitHub Profile Redesign — Setup

## Files

- `README.md` — replacement profile README
- `assets/hero.gif` — self-hosted animated hero background
- `snake.yaml` — contribution snake workflow

## Install

Copy these into your profile repository:

```text
usman-dev-k/
├── README.md
├── assets/
│   └── hero.gif
└── .github/
    └── workflows/
        └── snake.yml
```

Rename `snake.yaml` to:

```text
.github/workflows/snake.yml
```

Then commit and push.

## Important

The animated hero is stored in your own repository, so it does not depend on a third-party banner service.

The snake workflow publishes its generated SVGs to the `output` branch. The README references:

```text
https://raw.githubusercontent.com/usman-dev-k/usman-dev-k/output/github-contribution-grid-snake-dark.svg
```

Run the workflow once manually from **Actions → Generate Contribution Snake → Run workflow**. After it succeeds, the snake image should appear.

## About "interactive" backgrounds

GitHub profile READMEs cannot run arbitrary JavaScript or CSS inside the rendered README. GitHub documents that SVGs on GitHub do not support inline scripting or animation.

So this design uses a subtle animated GIF for the hero instead of trying to inject JavaScript.

If you want true mouse-reactive particles, 3D effects, hover cards, scrolling animations, etc., put those on the portfolio website and keep the GitHub README as a polished, lightweight entry point.
