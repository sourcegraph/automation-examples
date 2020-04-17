# Migrate from Travis CI to GitHub Actions

> NOTE: Sourcegraph Campaigns require the [Sourcegraph CLI](https://github.com/sourcegraph/src-cli) be [installed](https://github.com/sourcegraph/src-cli#installation) and [configured](https://github.com/sourcegraph/src-cli#setup) to point at your [Campaigns enabled](https://docs.sourcegraph.com/user/automation#configuration) Sourcegraph instance.

This examples migrates from Travis CI to GitHub Actions for Go projects.

What this does:
1. Delete `.travis.yml` file if exists.
2. Copy over the template `go.yml` to `.github/workflows/go.yml` (contains jobs for linting and testing).

---

Save as `action.json` and execute

```
src -v actions exec -f action.json -create-patchset
```
