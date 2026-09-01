# Instructor Setup

Complete this before class. Allow 20–30 minutes the first time.

## 1. Verify local tools

In the VS Code terminal, run:

```text
git --version
git config --global user.name
git config --global user.email
```

Expected: Git prints a version, name, and email. If name or email is blank, configure it:

```text
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

Use an email associated with your GitHub account if you want GitHub to connect commits to your profile.

## 2. Inspect the supplied repository

Extract the ZIP, open the extracted `CSC350_Git_Story_Lab` folder in VS Code, and run:

```text
git status
git log --oneline --decorate --graph --all
```

Expected: the branch is `main`, the working tree is clean, and several preparation commits are visible.

## 3. Create the GitHub repository

On GitHub, create an empty repository named `CSC350-Git-Story-Lab`.

Important: do not initialize the GitHub repository with a README, license, or `.gitignore`; the supplied local repository already has history.

Connect and publish:

```text
git remote add origin YOUR_REPOSITORY_URL
git remote -v
git push -u origin main
```

Expected: GitHub displays the same Markdown files and `git status` reports that `main` is up to date with `origin/main`.

## 4. Choose a classroom collaboration model

### Recommended: teams in one repository

Add students as collaborators. Each pair creates a uniquely named branch such as `feature/team-03-attraction`. This gives the cleanest branch and Pull Request demonstration.

### Alternative: forks

Students fork the repository and open Pull Requests from their forks. Use this if you do not want to grant write access. The concepts are the same, but the GitHub screens contain an additional repository selector.

## 5. Protect the main branch if appropriate

For a real assignment, require Pull Requests before merging into `main`. For the first live demo, branch protection can add friction; enable it only after students understand the basic flow.

## 6. Prepare a conflict pair

Assign two pairs to Activity 06. Both must branch from the same current version of `main`. Pair A changes the opening ceremony time. Pair B changes the same opening ceremony line to a different time or location. Merge Pair A’s Pull Request first; Pair B’s Pull Request should then report a conflict.

## 7. Keep recovery options ready

- Preserve a clean browser tab on the GitHub repository.
- Keep one local clone only for the instructor demo.
- If the network fails, use the local merge alternative in [CLASSROOM_RUNBOOK.md](CLASSROOM_RUNBOOK.md).
- Never demonstrate destructive history rewriting on student work during this introductory class.

## Final pre-class check

- [ ] VS Code opens the repository root, not its parent directory.
- [ ] Source Control shows the repository.
- [ ] Terminal starts in the repository root.
- [ ] GitHub authentication works.
- [ ] Students have the repository URL and activity instructions.
- [ ] You can push a harmless test branch and delete it afterward.

