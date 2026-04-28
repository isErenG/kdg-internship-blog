# KdG Internship Blog

A static Hugo blog tracking my KdG internship on CAN bus reverse engineering. Built with the [Blowfish](https://blowfish.page/) theme and deployed to GitHub Pages via GitHub Actions.

Live site: <https://isErenG.github.io/kdg-internship-blog/>

## Project layout

```
.
├── config/_default/         # site, language, params and menu config
├── content/posts/           # one markdown file per blog entry
├── themes/blowfish/         # Blowfish theme (git submodule)
├── .github/workflows/hugo.yml  # build + deploy workflow
└── README.md
```

## Local development

Prerequisites: Hugo extended (>= 0.157.0) and git.

```bash
# clone with the theme submodule
git clone --recurse-submodules https://github.com/isErenG/kdg-internship-blog.git
cd kdg-internship-blog

# run the dev server (live reload at http://localhost:1313)
hugo server

# or include drafts
hugo server -D
```

If you cloned without `--recurse-submodules`:

```bash
git submodule update --init --recursive
```

To build the static site into `public/`:

```bash
hugo --gc --minify
```

## First-time GitHub Pages setup

1. Create a new **public** repository named `kdg-internship-blog` on GitHub under the `isErenG` account.
2. Push this directory to it:
   ```bash
   git remote add origin https://github.com/isErenG/kdg-internship-blog.git
   git push -u origin main
   ```
3. In the repo on GitHub, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **GitHub Actions**.
5. The workflow at `.github/workflows/hugo.yml` will run on the next push and publish the site.

The first deploy can take a couple of minutes. After it finishes, the site will be live at <https://isErenG.github.io/kdg-internship-blog/>.

## Adding a new post

```bash
hugo new posts/2026-05-01-some-title.md
```

Edit the frontmatter (set `draft: false` when ready) and the body, then:

```bash
git add content/posts/2026-05-01-some-title.md
git commit -m "Add post for 2026-05-01"
git push
```

The push to `main` triggers the `Deploy Hugo site to Pages` workflow, which rebuilds the site and pushes the new artifact to GitHub Pages automatically.

## Updating the theme

Blowfish is pinned via a git submodule. To pull the latest version:

```bash
git submodule update --remote themes/blowfish
git add themes/blowfish
git commit -m "Update Blowfish theme"
git push
```

## Configuration

All Hugo configuration lives in `config/_default/`:

- `hugo.toml` — site-wide settings (baseURL, theme, taxonomies)
- `languages.en.toml` — site title, author block, language settings
- `params.toml` — Blowfish theme parameters (homepage layout, article options)
- `menus.en.toml` — main and footer menus
- `markup.toml` — markdown rendering options

## References

- Hugo docs — <https://gohugo.io/documentation/>
- Hugo on GitHub Pages — <https://gohugo.io/host-and-deploy/host-on-github-pages/>
- Blowfish theme docs — <https://blowfish.page/docs/>
