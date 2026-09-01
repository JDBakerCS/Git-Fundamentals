# Assessment and Success Evidence

Grade observable evidence, not whether the student happened to avoid every error.

## Individual competency check: 10 points

| Evidence | Points | Success condition |
|---|---:|---|
| Repository state | 1 | Student identifies current branch and interprets `git status` correctly |
| Change inspection | 1 | Student shows the intended line in `git diff` before staging |
| Intentional staging | 1 | Only the requested file appears in `git diff --staged` |
| Commit | 2 | Commit exists and message describes the completed change |
| Branch | 1 | Work was completed on the assigned feature branch |
| Remote synchronization | 1 | Branch and commit are visible on GitHub |
| Pull Request | 1 | Correct base/compare branches and a meaningful description |
| Review | 1 | Student reviews the actual diff and gives a useful comment or approval |
| Final verification | 1 | Local `main` is updated and working tree is clean |

## Team conflict check: 4 points

- 1 point: team explains why both changes cannot be applied automatically.
- 1 point: team produces a deliberate final sentence rather than accepting blindly.
- 1 point: all conflict markers are removed.
- 1 point: resolved result is committed, pushed, and readable on `main`.

## Fast oral checks

Ask a student to point to the current location of a change:

1. Saved but not staged → working tree.
2. Staged but not committed → staging area/index.
3. Committed but not pushed → local repository.
4. Pushed feature branch but PR not merged → remote feature branch.
5. PR merged → remote target branch; classmates still need to pull locally.

## Common misconceptions worth partial credit

- “Commit sends the file to GitHub.” Ask the student to run `git remote -v` and distinguish local from remote.
- “Pull Request downloads changes.” Ask which command actually updates the local clone.
- “Conflict means one person is wrong.” Ask what overlapping edit made automatic combination unsafe.

## Instructor dashboard

For each team, record: branch name, latest commit ID, PR link, reviewer, merge status, and one observed misconception. This provides both completion evidence and a plan for the next lesson.

