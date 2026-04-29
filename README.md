# BlastCAD Documentation

This repository contains the source for **[docs.blastcad.com](https://docs.blastcad.com)** — the official documentation website for [BlastCAD](https://blastcad.com).

The site is built with [Jekyll] using the [Just the Docs] theme and is published automatically to GitHub Pages via GitHub Actions.

## Site Structure

| File / Directory | Description |
|:-----------------|:------------|
| `index.md` | Home page |
| `getting-started.md` | Installation and first-steps guide |
| `user-guide/` | In-depth user guide (workspace, tools, file formats) |
| `changelog.md` | Version history |
| `_config.yml` | Jekyll site configuration |
| `CNAME` | Custom domain (`docs.blastcad.com`) |

## Contributing to the Docs

1. Fork or clone this repository.
2. Run `bundle install` to install dependencies.
3. Run `bundle exec jekyll serve` to preview at `localhost:4000`.
4. Edit or add Markdown files, then open a pull request.

## Building Locally

Requires [Ruby] and [Bundler]:

```bash
bundle install
bundle exec jekyll serve
```

The built site is stored in `_site/`.

## Deploying

Every push to `main` triggers the [GitHub Actions workflow](.github/workflows/pages.yml), which builds the site and deploys it to GitHub Pages at [docs.blastcad.com](https://docs.blastcad.com).

## License

Content is licensed under the [MIT License](LICENSE).

[Jekyll]: https://jekyllrb.com
[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[Ruby]: https://www.ruby-lang.org/
[Bundler]: https://bundler.io

