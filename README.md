# velartyler.github.io

This is the source for Kyler Laycock's academic website: [velartyler.github.io](https://velartyler.github.io)

Built using [Hugo](https://gohugo.io/) with the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme.

## Running locally

To run and test site locally:

```sh
cd path/to/top/directory
hugo server
```

Then open http://localhost:1313. The page reloads as files are saved.

The theme is a Git submodule. On a fresh clone, get it with:

```sh
git clone --recurse-submodules https://github.com/velartyler/velartyler.github.io.git
```

or, in an existing clone:

```sh
git submodule update --init --recursive
```

## Publishing

Pushing to `main` builds and deploys the site through GitHub Actions (`.github/workflows/deploy2pages.yml`). Progress and errors show up under the repo's Actions tab.

## Where things are

| Path | What it holds |
|---|---|
| `hugo.yaml` | Site settings, top menu, social links, and the homepage text (subtitle, research areas, cards) |
| `content/profile.md` | Profile page |
| `content/research.md` | Research page |
| `content/outreach/index.md` | Teaching & Outreach page |
| `content/cv/index.md` | CV page |
| `content/presentations/_index.md` | Full list of talks and presentations |
| `content/presentations/featured-*/` | One folder per featured presentation card |
| `content/posts/` | Posts |
| `static/pdf/Laycock_CV.pdf` | CV PDF |
| `static/profile.png` | Headshot |
| `layouts/` | Template overrides (homepage layout, footer, 404 page, etc.) |
| `assets/css/extended/portfolio-redesign.css` | Custom styles and colors |

## Updating the CV

1. Replace `static/pdf/Laycock_CV.pdf`, keeping the same file name.
2. Change the "updated" line in `content/cv/index.md`.

## Adding a featured presentation

1. Copy one of the `content/presentations/featured-*` folders and rename it.
2. In its `index.md`, set the `title` and change `weight` to set its position (lower numbers come first).
3. Put the PDF in the folder. The download link and viewer appear on their own.
4. For a thumbnail, put an image of the first slide in the folder as `thumbnail.png` and uncomment the `image:` line in `index.md`.

## Adding a post

Add a Markdown file to `content/posts/` with a `title` and `date` at the top. See the existing posts for the format.

## "Under construction" banner

Pages with `underConstruction: true` at the top of their file show the banner (`static/under-construction.jpg`). Delete that line when a page is finished. It's currently on `content/research.md`, `content/posts/_index.md`, and `content/presentations/_index.md`.
