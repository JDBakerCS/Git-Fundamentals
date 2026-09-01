# Activity 07 — Practice Safe Recovery

Use a disposable branch so no shared work is at risk.

## A. Discard an unwanted unstaged edit

1. Create a branch: `git switch -c practice/recovery-YOUR-NAME`
2. Add the line `THIS LINE IS A MISTAKE` to `DECISIONS.md` and save.
3. Confirm it with `git diff`.
4. Discard only that file’s unstaged edit:

```text
git restore DECISIONS.md
```

Success: the mistake disappears and `git status` is clean.

## B. Unstage but keep an edit

1. Make a valid short decision entry and save.
2. Stage it with `git add DECISIONS.md`.
3. Verify it appears in `git diff --staged`.
4. Unstage it:

```text
git restore --staged DECISIONS.md
```

Success: the edit remains in the file, appears in `git diff`, and is no longer in `git diff --staged`.

## Reflection

Explain why `restore` and `restore --staged` have different results.

