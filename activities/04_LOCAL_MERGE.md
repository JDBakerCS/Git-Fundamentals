# Activity 04 — Understand a Local Merge

This instructor-led activity is useful before GitHub Pull Requests.

## Predict

Before running the merge, answer:

- Which branch should receive the feature?
- Where should `HEAD` point before the merge?

## Steps

```text
git switch main
git merge feature/team-03-attraction
git log --oneline --decorate --graph --all -8
```

## Success evidence

- `main` contains the attraction.
- The graph shows the feature commit reachable from `main`.
- Git reports either a fast-forward or a merge commit; both can be valid depending on history.

Do not perform this merge on the shared classroom `main` if the instructor is teaching a Pull Request-only policy. The instructor may demonstrate it in a separate clone.

