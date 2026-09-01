# Activity 03 — Build on an Isolated Branch

Goal: add an attraction without changing `main` directly.

## Steps

1. Start from updated `main`:

```text
git switch main
git pull
```

2. Create a unique branch. Replace `03` with your team number:

```text
git switch -c feature/team-03-attraction
```

3. Add one attraction to `FESTIVAL_PLAN.md` and explain it with one sentence.
4. Inspect, stage, and commit:

```text
git status
git diff
git add FESTIVAL_PLAN.md
git diff --staged
git commit -m "Add team 03 festival attraction"
```

5. Publish the branch:

```text
git push -u origin feature/team-03-attraction
```

## Success evidence

- `git branch --show-current` prints the feature branch.
- GitHub shows both `main` and the feature branch.
- `main` does not yet contain the new attraction.

