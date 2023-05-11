## What
Showing off auto updating detect-gpu along with self hosted benchmarks
## How
1. dependabot runs weekly checking for a new patch version of detect-gpu, if found it creates a PR updating `package.json` and `yarn.lock`
2. Workflow is triggered by PRs and runs if PR author is dependabot. The repo is checked out. A bash script downloads the newest benchmarks and places them in `public/benchmarks`. The changes are commited and pushed to the branch created by dependabot.
3. Then the PR will have 2 commits which together bumps detect-gpu and updates all the self-hosted benchmark files
## Thoughts
- The two commits could be squashed when merging so we have a single commit.
- ???
