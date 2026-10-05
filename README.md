# velartyler.github.io

This is the source for Kyler Laycock's academic website: [velartyler.github.io](https://velartyler.github.io)

Built using [Hugo](https://gohugo.io/) with the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme.

## Running locally

To run and test site locally:

```sh
cd path/to/top/directory
hugo server
```

open http://localhost:1313. should refresh as you edit files.

The theme is a Git submodule. On a fresh clone, get it with:

```sh
git clone --recurse-submodules https://github.com/velartyler/velartyler.github.io.git
```

or in existing clone:

```sh
git submodule update --init --recursive
```

## Publishing

Pushing to `main` builds and deploys the site through GitHub Actions (`.github/workflows/deploy2pages.yml`). Progress and errors show up under the repo's Actions tab.

## Where things are

| Path | What's there |
|---|---|
| `hugo.yaml` | Site settings, top menu, Google scholar and similar links, homepage text (subtitle, research areas, cards) |
| `content/profile.md` | About me page |
| `content/research.md` | Research page |
| `content/outreach/index.md` | Teaching & Outreach page |
| `content/cv/index.md` | CV page |
| `content/presentations/_index.md` |List of talks and presentations |
| `content/presentations/featured-*/` | One folder per presentation card for featured talks |
| `content/posts/` | Posts |
| `static/pdf/Laycock_CV.pdf` | CV PDF |
| `static/profile.png` | Headshot |
| `layouts/` | Template overrides (homepage layout, footer, 404 page, etc.) |
| `assets/css/extended/portfolio-redesign.css` | Custom styles and colors |

## Updating CV

1. Just replace `static/pdf/CV.pdf` (keep same file name).
2. Change "updated" line in `content/cv/index.md` to update date

## Adding presentation to card

1. Copy one of the `content/presentations/featured-*` folders and rename it.
2. In `index.md`, set `title` and change `weight` to set position
3. Put PDF of slides or poster in the folder. Download link and viewer should appear.
4. For thumbnail, put an image of the first slide in the folder as `thumbnail.png` and uncomment `image:` line in `index.md`.

## Adding blog posts

Add a .md file to `content/posts/` with `title` and `date` at the top

## "Under construction" banner

Wrote a thing that should let you change the value of `underConstruction: true` at the top of the a page's file to show or hide the banner (`static/under-construction.jpg`). Delete that line when a page is finished.
