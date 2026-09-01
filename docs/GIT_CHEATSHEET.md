# Git and GitHub Classroom Cheatsheet

Run commands from the repository root in the VS Code terminal.

## Inspect before acting

```text
git status
git diff
git diff --staged
git log --oneline --decorate --graph --all
git branch --show-current
git remote -v
```

## Create a local snapshot

```text
git add FILE_NAME.md
git commit -m "Describe one completed change"
```

## Synchronize with GitHub

```text
git pull
git push
git push -u origin BRANCH_NAME
```

`git pull` first obtains remote updates and then integrates the selected upstream branch. `git push` publishes reachable local commits to a remote branch.

## Work with branches

```text
git switch -c feature/SHORT-DESCRIPTION
git switch main
git branch
git merge BRANCH_NAME
```

Use `git switch` in this course because its purpose is explicit. You may see older materials use `git checkout` for both branch switching and file restoration.

## Safe beginner recovery

```text
git restore FILE_NAME.md
git restore --staged FILE_NAME.md
git merge --abort
git revert COMMIT_ID
```

- `git restore FILE_NAME.md` discards an uncommitted working-tree change. Confirm the exact file first.
- `git restore --staged FILE_NAME.md` unstages but keeps the working-tree edit.
- `git merge --abort` returns to the state before an unresolved merge attempt when Git can do so.
- `git revert COMMIT_ID` creates a new commit that reverses an earlier commit; it does not erase shared history.

## Pull Request workflow

1. Push the feature branch.
2. On GitHub, choose the feature branch as **compare** and `main` as **base**.
3. Write what changed, why, and how it was verified.
4. Request review.
5. Reviewer reads **Files changed**, comments, and approves or requests changes.
6. Merge only after the requested change is correct.
7. Locally switch to `main` and pull.

## Commit message pattern

Use an action plus a specific object:

- Good: `Add quiet-room location to accessibility plan`
- Good: `Correct opening ceremony time`
- Weak: `update`
- Weak: `changes`

