# Public Build Repo (Workflow Only)

This directory is a **template** for the public `BUILD_REPO` described in the “private source + public workflow” setup.

What goes into the public build repo:

- `.github/workflows/e2e-build.yml` (workflow_dispatch only)
- (optional) a short README like this

What must **not** go into the public build repo:

- source code
- submodules pointing to the private repo
- any secrets or logs containing secrets

The workflow clones the private source repo using a **read-only deploy key** stored in `BUILD_REPO` secrets as `SOURCE_REPO_SSH_KEY`.

