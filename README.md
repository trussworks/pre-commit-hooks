# Truss pre-commit hooks

<!-- toc -->

* [circleci-validate](#circleci-validate)
* [gen-docs](#gen-docs)
* [goreleaser-check](#goreleaser-check)
* [markdown-toc](#markdown-toc)
* [mdspell](#mdspell)
* [spelling-sort](#spelling-sort)
* [hadolint](#hadolint)

<!-- Regenerate with "pre-commit run -a markdown-toc" -->

<!-- tocstop -->

## circleci-validate

Validate CircleCI config yaml located in `.circleci/config.yml`. In order for this to run you will need to install
the `circleci` CLI tool locally with:

```sh
brew install circleci
```

The script will not run the validation if the environment variable `CI` is set, which means you can safely run this
on CircleCI and it will be a no-op.

## gen-docs

Generate a Docs Index using [adr-log](https://www.npmjs.com/package/adr-log). It will modify files with comments in it
per the docs on that module.

By default it will only look in the `docs/` directory of your repo. You can pass in different directories by using
the `args` parameter like this: `args: ["docs/adr", "docs/rfc"]`

## goreleaser-check

Validate goreleaser config yaml located at `.goreleaser.yml`. In order for this to run you will need to install
the `goreleaser` CLI tool locally with:

```sh
brew install goreleaser
```

## markdown-toc

Generate a Table of Contents using [markdown-toc](https://www.npmjs.com/package/markdown-toc). It will modify files
with comments in it per the docs on that module.

## mdspell

Run spellcheck on markdown files using [markdown-spellcheck](https://www.npmjs.com/package/markdown-spellcheck). It
will ignore words listed in a `.spelling` file in your repo.

## spelling-sort

Run `sort` on the `.spelling` file used by the `markdown-spellcheck` tool. This keeps the file tidy as it is used.

## hadolint

Run the [hadolint](https://github.com/hadolint/hadolint) Dockerfile linter
