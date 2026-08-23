# Contributing

Thanks for contributing! This project follows [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/#summary) and [Git Flow](https://about.gitlab.com/blog/what-is-gitflow/#what-is-gitflow).

## Before you commit

Install the git hooks once per clone:

```bash
pre-commit install
```

This wires up both the `pre-commit` and `commit-msg` hook stages, which run automatically on every commit and check:

- JSON/YAML validity, trailing whitespace, end-of-file newlines, oversized files, missing shebangs, and accidental AWS credentials
- Spelling, via [cspell](https://cspell.org/), against both changed files and your commit message
- Commit message format, via [conventional-pre-commit](https://github.com/compilerla/conventional-pre-commit), enforced with `--strict`

You can run all hooks against the whole repo at any time with:

```bash
pre-commit run --all-files
```

## Commit messages

Use the Conventional Commits format: `type(scope): message`.

Allowed scopes are: `feat, fix, refactor, tests, build, ci, changelog, docs, perf`.

If cspell flags a legitimate word (a tool name, proper noun, or project-specific term), add it to the `words` list in `cspell.json` rather than rewording around it.

## Changelog

`CHANGELOG` is generated, not hand-written. Regenerate it from commit history with [git-cliff](https://git-cliff.org/):

```bash
docker run -t -v "$(pwd)":/app/ "orhunp/git-cliff:${TAG:-latest}"
```

See `cliff.toml` for how commits are grouped into sections.

## Pull requests

Please fill out the PR template, including the PR checklist and PR type. Make sure your commits pass the hooks above before opening a PR.
