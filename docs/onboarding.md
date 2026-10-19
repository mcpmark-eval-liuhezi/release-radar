# Onboarding

Welcome to Release Radar. This guide gets you from zero to a merged change in a few minutes.

## 1. Clone the repository

```
git clone https://github.com/mcpmark-eval-liuhezi/release-radar.git
cd release-radar
```

If you plan to contribute regularly, [fork the repository](https://github.com/mcpmark-eval-liuhezi/release-radar/fork) first and clone your fork instead, then add the upstream remote:

```
git remote add upstream https://github.com/mcpmark-eval-liuhezi/release-radar.git
```

## 2. Work on a branch

Never commit directly to `main`. Start from a fresh, up-to-date branch:

```
git checkout main
git pull upstream main            # or: git fetch upstream && git rebase upstream/main
git checkout -b my-topic-branch
```

Keep one logical change per branch, and keep commits small and focused. Follow the style of the existing docs in `README.md` and `docs/`.

## 3. Open a pull request

Push your branch and open a pull request against `main`:

```
git push -u origin my-topic-branch
```

Then open the PR from the GitHub web UI. In the description, explain what changed and why, and reference the related issue (e.g. "Closes #6"). A reviewer will take a look, and the CI workflow will run on every push and pull request.

## 4. Review and merge

- Address review comments by pushing additional commits to the same branch — don't open a new PR.
- Once approved, the branch is merged into `main`.

## Where things live

- `README.md` — project overview and monitored-projects summary
- `docs/monitored-projects.md` — the list of upstream projects we track, with their latest releases
- `.github/workflows/ci.yml` — CI checks
- Backlog lives in GitHub issues (see the launch checklist umbrella issue)
