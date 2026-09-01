# Activity 05 — Propose, Review, and Merge

Goal: use a Pull Request as a review conversation around branch changes.

## Author

1. Open the repository on GitHub.
2. Create a Pull Request with `main` as **base** and your feature branch as **compare**.
3. Use this description:

```text
What changed:
Why it improves the festival:
How I verified it:
```

4. Request a reviewer.

## Reviewer

1. Open **Files changed**.
2. Confirm the change is in scope and readable.
3. Check that no unrelated lines were deleted.
4. Leave one specific comment or submit an approval.

## Author after feedback

If a change is requested, edit the same branch, commit, and push. The existing Pull Request updates automatically because it compares branches.

## Merge and synchronize

After approval, merge according to the instructor’s policy. Then every teammate runs:

```text
git switch main
git pull
git status
```

## Success evidence

- The PR has the correct base and compare branches.
- The reviewer inspected **Files changed**.
- GitHub marks the PR merged.
- Local `main` contains the accepted attraction and is clean.

