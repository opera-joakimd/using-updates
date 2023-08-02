## What

Showing off auto updating detect-gpu along with self hosted benchmarks

## How

1. dependabot runs monthly checking for a new patch version of detect-gpu, if found it creates a PR updating `package.json` and `yarn.lock`
2. The workflow is triggered by an opened PR and runs if the PR author is dependabot.
3. A linear task is created
4. Git is set up
5. The newest minified benchmarks are downloaded and the changes are commited
6. The dependabot commit and the commit to update the benchmarks are squashed into a single commit and the commit message is prefixed with the linear task id
7. The PR title is updated

## Whats needed to add to another repo

- Copy `dependabot.yml` as is
- Copy `update-benchmarks.yml`
  1. change linear team name
- Generate a linear PAT
  1. Add this to github secrets as `LINEAR_API_KEY`

## Thoughts

- ???
  change
