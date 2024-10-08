# Bit Node.js Tasks for Git CI/CD Pipelines
Node.js Tasks that you can use in Github Actions, Azure DevOps, GitLab and other CI/CD platforms.

## Setup Guide


1. You need to define the following environment variables in your CI platform and share them across the tasks.
    - `GIT_USER_NAME` - Your Git user name.
    - `GIT_USER_EMAIL` - Your Git email.
    - `BIT_CONFIG_ACCESS_TOKEN`([docs](https://bit.dev/reference/ci/other-ci#generating-an-access-token)).
    - `BIT_CONFIG_ANALYTICS_REPORTING` - `"false"`
    - `BIT_CONFIG_ANONYMOUS_REPORTING` - `"false"`
    - `BIT_CONFIG_INTERACTIVE` - `"false"`
2. You need to pass the workspace root directory `ws-dir` for all the tasks. If your Bit workspace is at the root level, pass `"./"`.

### Automating Component Release

| Task                        | Node.js Example                  |
|-----------------------------|---------------------------------|
| Initialize Bit          | [bit-init.js](/scripts/bit-init.js) |
| Bit Verify Components   | [verify.js](/scripts/verify.js) |
| Bit Tag and Export      | [tag-export.js](/scripts/tag-export.js) |
| Bit Pull Request Build  | [pull-request.js](/scripts/pull-request.js) |
| Bit Lane Cleanup        | [lane-cleanup.js](/scripts/lane-cleanup.js) |
| Commit Bitmap           | [commit-bitmap.js](/scripts/commit-bitmap.js) |

  :arrow_down: [Download Files](https://github.com/bit-tasks/nodejs/raw/main/downloads/automating-component-releases.zip)

### Update Workspace Components, External Dependencies and Envs
| Task                        | Node.js Example                  |
|-----------------------------|-------------------------------|
| Dependency Update           |  [dependency-update.js](/scripts/dependency-update.js) |

  :arrow_down: [Download Files](https://github.com/bit-tasks/nodejs/raw/main/downloads/dependency-update.zip)

### Sync Git Branches with Bit Lanes

| Task                        | Node.js Example                  |
|-----------------------------|---------------------------------|
| Branch Lane                 | [branch-lane.js](/scripts/branch-lane.js) |
| Lane Branch                 | [lane-branch.js](/scripts/lane-branch.js) |

  :arrow_down: [Download Files](https://github.com/bit-tasks/nodejs/raw/main/downloads/branch-lane.zip)

## Setup PNPM Caching
You can speed up the CI builds by caching the `pnpm store`. Refer to the official documentation for [continuous integration](https://pnpm.io/continuous-integration) by `pnpm`.


## References

### GitHub Actions

For more information refer [Create a javascript action](https://docs.github.com/en/actions/creating-actions/creating-a-javascript-action)

### GitLab CI/CD

For more information refer [Specify a custom CI/CD file](https://docs.gitlab.com/ee/ci/pipelines/settings.html#specify-a-custom-cicd-configuration-file)

### Azure DevOps

For more information refer [Add build task](https://learn.microsoft.com/en-us/azure/devops/extend/develop/add-build-task?view=azure-devops)

## Contributor Guide

To create zip files use the below commands.

```bash
chmod +x zip_files.sh
bash ./zip_files.sh
```
