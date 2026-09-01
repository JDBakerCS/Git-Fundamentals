# Activity 02 — Publish and Synchronize

Goal: distinguish local history from the GitHub copy.

## Author

Publish the commit from Activity 01:

```text
git branch --show-current
git push
```

If the branch has no upstream, Git will suggest a command similar to:

```text
git push -u origin YOUR_BRANCH_NAME
```

Do not copy a branch name from a neighbor; use your printed current branch.

## Partner

After the author confirms the push, update your clone:

```text
git status
git pull
git log --oneline -3
```

## Success evidence

- Author sees the commit on GitHub.
- Partner sees the same commit ID after pulling.
- Both can explain why committing alone did not update the partner’s computer.

