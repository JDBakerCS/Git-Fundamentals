# CSC350 Git Story Lab: Save the Byte City Festival

Byte City’s annual technology festival opens tomorrow, but the shared plan is incomplete. Your class is the release team. Each change to the festival plan becomes a reason to use Git: inspect a change, stage it, commit it, share it, review it, merge it, and sometimes resolve a conflict.

The repository contains no program code. Every tracked project file is Markdown, so students can focus on Git and GitHub rather than syntax or debugging.

## Mission

By the end of the lab, the class should have a reviewed and merged festival plan. Every student should be able to explain where a change currently lives and prove that a requested Git operation succeeded.

## Start here

- Instructor: read [docs/INSTRUCTOR_SETUP.md](docs/INSTRUCTOR_SETUP.md), then [docs/CLASSROOM_RUNBOOK.md](docs/CLASSROOM_RUNBOOK.md).
- Student: begin with [activities/00_PRECLASS_CHECK.md](activities/00_PRECLASS_CHECK.md), then complete the numbered activities.
- During an error: use [docs/TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md) before repeating commands.
- For commands: use [docs/GIT_CHEATSHEET.md](docs/GIT_CHEATSHEET.md).
- For grading: use [docs/ASSESSMENT.md](docs/ASSESSMENT.md).

## Story files students will change

- [FESTIVAL_PLAN.md](FESTIVAL_PLAN.md): schedule, attractions, accessibility, and contingency plans.
- [TEAM_ROLES.md](TEAM_ROLES.md): fictional festival team responsibilities.
- [DECISIONS.md](DECISIONS.md): short decision record used to practice small commits.
- [CHANGELOG.md](CHANGELOG.md): human-readable summary of accepted changes.

## Core workflow

1. Pull before starting shared work.
2. Create or switch to the correct branch.
3. Edit and save a Markdown file.
4. Inspect with `git status` and `git diff`.
5. Stage intentionally with `git add`.
6. Verify the staged snapshot with `git diff --staged`.
7. Commit with a specific message.
8. Push the branch.
9. Open a Pull Request, review, and merge.
10. Return to `main` and pull the accepted result.

## Definition of done

You are done only when all four statements are true:

- `git status` reports a clean working tree.
- `git log --oneline --decorate -5` shows your commit or the merged result.
- GitHub shows the expected branch or merged Pull Request.
- The final Markdown file contains the intended content and no conflict markers.

