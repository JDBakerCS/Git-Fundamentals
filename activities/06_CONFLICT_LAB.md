# Activity 06 — Resolve an Intentional Conflict

Goal: make a human decision when two branches change the same plan line.

## Setup

Both teams start from the same updated `main`.

### Team A

Create `conflict/team-a-opening` and change this line:

`Opening ceremony: 10:00 AM at the Innovation Atrium`

Change the time to 9:30 AM, then commit, push, and open a Pull Request.

### Team B

Create `conflict/team-b-opening` from the same original `main`. Change the same line so the ceremony begins at 10:30 AM in the Library Commons. Commit, push, and open a Pull Request.

## Instructor action

Merge Team A first. Team B’s branch now competes with the accepted line.

## Team B resolution

Update the branch using the instructor’s chosen method. In a local resolution:

```text
git switch conflict/team-b-opening
git fetch origin
git merge origin/main
git status
```

Open `FESTIVAL_PLAN.md`. Decide the final time and location with the instructor. Remove all conflict markers and leave one correct opening-ceremony line.

```text
git add FESTIVAL_PLAN.md
git commit -m "Resolve opening ceremony schedule conflict"
git push
```

## Success evidence

- The final file contains exactly one opening-ceremony line.
- No `<<<<<<<`, `=======`, or `>>>>>>>` markers remain.
- `git status` is clean after the resolution commit.
- The Pull Request becomes mergeable and explains the chosen resolution.

