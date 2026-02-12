# git-repository-foss-template

Based on [Conventional Commits](# https://github.com/angular/angular/blob/main/contributing-docs/commit-message-guidelines.md) and [Git Flow](# https://github.com/angular/angular/blob/main/contributing-docs/commit-message-guidelines.md).

It includes sanity checks for commit messages and branch names.

## Usage

```bash
git clone THIS_REPO ~/your-repo
git remove origin origin master
git origin add NEW_REPO
```

## Execute hooks

```bash
pre-commit run --all-files
```

## Auto CHANGELOG

```bash
docker run -t -v "$(pwd)":/app/ "orhunp/git-cliff:${TAG:-latest}"
```

This is batteries-included template. It leverages `pre-commit` to perform the following checks:

- json + yaml lint
- auto changelog
- dictionary

## Links & Resources

- [Git Flow Cheatsheet](https://danielkummer.github.io/git-flow-cheatsheet/)
- [Conventional Commits]()
- []()
