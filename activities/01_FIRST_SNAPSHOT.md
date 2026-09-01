# Activity 01 — Make the First Local Snapshot

Goal: add one festival slogan and prove where the change moves.

## Steps

1. Open `FESTIVAL_PLAN.md`.
2. Replace `Choose a festival slogan` with a slogan of 3–8 words.
3. Save the file.
4. Inspect:

```text
git status
git diff
```

5. Stage only the festival plan:

```text
git add FESTIVAL_PLAN.md
git diff --staged
```

6. Commit:

```text
git commit -m "Add festival slogan"
```

7. Verify:

```text
git status
git log --oneline -3
```

## Success evidence

- Before staging, `git diff` shows one intentional edited line.
- After staging, `git diff --staged` shows that line.
- After committing, the new commit appears at the top of the log.
- `git status` reports a clean working tree.

## Stop and diagnose if

- More than one file is staged.
- The diff contains accidental deletions.
- The commit message editor opens unexpectedly; ask before closing it.

