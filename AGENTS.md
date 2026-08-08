# Local development

This is a Jekyll site. Run the commands below from the repository root.

## Writing style

Avoid em dashes and semicolons in site prose wherever possible. Prefer periods, commas, or a sentence rewrite instead.

## First-time setup

Install the Bundler version required by `Gemfile.lock`, then install the site's gems:

```sh
gem install bundler:2.4.14
bundle install
```

If the system Ruby cannot install gems, use a current Ruby installation (for example via `rbenv` or Homebrew) and repeat the commands above.

## Run locally

Start Jekyll with automatic rebuilds and live reload:

```sh
bundle exec jekyll serve --livereload
```

Open <http://localhost:4000/> in a browser. Keep the terminal running while testing; edit Markdown, HTML, SCSS, or configuration files and refresh when needed.

To serve the generated site without live reload:

```sh
bundle exec jekyll serve
```

## Build/check the site

Build the production output into `_site/`:

```sh
bundle exec jekyll build
```

The build command is the basic local validation check. If it fails, read the first error in the terminal; common causes are missing gems, invalid front matter, or malformed Liquid/SCSS.

## Useful options

Use a different port if port 4000 is occupied:

```sh
bundle exec jekyll serve --livereload --port 4001
```

Use `--drafts` to preview posts stored in `_drafts/`:

```sh
bundle exec jekyll serve --livereload --drafts
```
