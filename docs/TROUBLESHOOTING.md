# Troubleshooting by Symptom

Stop before repeating a failing command. Read `git status` and the first useful error line.

## `fatal: not a git repository`

Cause: the terminal is outside the repository.

Check:

```text
pwd
```

Fix: open the correct folder in VS Code or use `cd` to enter `CSC350_Git_Story_Lab`.

## Commit says “nothing to commit”

Possible causes:

- The file was not saved in VS Code.
- You edited a different copy of the repository.
- The content already matches the committed version.

Check `git status`, save the file, and confirm the VS Code window title shows the intended folder.

## Git asks for user name or email

Configure once:

```text
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

Then retry the commit.

## Push is rejected because the remote contains work you do not have

Your branch is behind its remote counterpart.

```text
git status
git pull
```

Resolve any conflict, verify the result, commit if Git requests it, then push again. Do not use force push in this introductory lab.

## `src refspec ... does not match any`

Common causes: the branch name is wrong or the repository has no commit yet.

```text
git branch --show-current
git log --oneline -1
```

Use the printed branch name and ensure at least one commit exists.

## Branch switching is blocked by local changes

Git is protecting unsaved work that would be overwritten.

Choose intentionally:

- Finish and commit the change.
- Discard a known unwanted file edit with `git restore FILE_NAME.md`.
- Ask the instructor about stashing; do not use it blindly.

## Merge conflict appears

This is a decision point, not a crash.

1. Run `git status` and open the named file.
2. Compare both intended changes.
3. Edit the file into the correct final version.
4. Remove all `<<<<<<<`, `=======`, and `>>>>>>>` markers.
5. Save and run `git add FILE_NAME.md`.
6. Run `git commit` if required.
7. Verify with `git status` and read the final file.

If you are unsure and have not started resolving:

```text
git merge --abort
```

## GitHub does not show the commit

A local commit is not automatically published.

```text
git status
git branch --show-current
git remote -v
git push -u origin YOUR_BRANCH_NAME
```

Refresh GitHub and select the correct branch.

## Source Control view looks different from the terminal

Save all files, then refresh Source Control. Both interfaces operate on the same repository state. Use **View → Output → Git** when VS Code hides a useful command error.

