# git-repository-foss-template

Based on [Conventional Commits](https://github.com/angular/angular/blob/main/contributing-docs/commit-message-guidelines.md) and [Git Flow](https://about.gitlab.com/blog/what-is-gitflow/#what-is-gitflow).

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

- [git hooks](https://git-scm.com/docs/githooks)
- [pre-commit](https://pre-commit.com/)
- [Keep a CHANGELOG](https://keepachangelog.com/en/1.0.0/)
- [Git Flow Cheatsheet](https://danielkummer.github.io/git-flow-cheatsheet/)
- [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/#summary)
- [Angular's commit message guidelines](https://github.com/angular/angular/blob/22b96b96902e1a42ee8c5e807720424abad3082a/CONTRIBUTING.md#-commit-message-guidelines)
