# Truss pre-commit hooks

<!-- toc -->

* [circleci-validate](#circleci-validate)
* [gen-docs](#gen-docs)
* [markdown-toc](#markdown-toc)
* [mdspell](#mdspell)

Regenerate with "pre-commit run -a markdown-toc"

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

## markdown-toc

Generate a Table of Contents using [markdown-toc](https://www.npmjs.com/package/markdown-toc). It will modify files
with comments in it per the docs on that module.

## mdspell

Run spellcheck on markdown files using [markdown-spellcheck](https://www.npmjs.com/package/markdown-spellcheck). It
will ignore words listed in a `.spelling` file in your repo.
