# Website

Personal website of Fionn Masuhr, built with [Jekyll](https://jekyllrb.com)
and deployed to AWS (S3 and CloudFront) by GitHub Actions on every push to `main`.

## Getting Started

### Requirements

- Ruby, in the version from [`.ruby-version`](.ruby-version)
- Node.js, in the version from [`.nvmrc`](.nvmrc) (only for linting)

### Dependencies

Install the dependencies via [Bundler](https://bundler.io) and npm:

```sh
bundle install
npm install
```

### Development

Build the site into `_site/`:

```sh
bundle exec jekyll build
```

During development it is useful to run a web server that rebuilds the site
on every change and reloads the browser:

```sh
bundle exec jekyll serve --livereload
```

### Linting

Lint the stylesheets with [Stylelint](https://stylelint.io):

```sh
npm run lint
```

The Markdown files are linted with
[markdownlint-cli2](https://github.com/DavidAnson/markdownlint-cli2) in CI,
configured in [`.markdownlint-cli2.yaml`](.markdownlint-cli2.yaml).
