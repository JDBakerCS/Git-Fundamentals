# Activity 02 — Publish and Synchronize

Goal: distinguish local history, the GitHub repository, and a partner’s local copy.

## Part 1 — Publish the completed Activity 1 repository

Choose one student as the **Author**. The Author continues using the repository in which the pair completed Activity 1\.

The other student is the **Partner**.

### Author

Create one empty GitHub repository for the pair. Do not initialize it with a README, `.gitignore`, or license.

Confirm the local repository is ready:

git status

git branch \--show-current

git remote \-v

Expected:

- The current branch is `main`.  
- The working tree is clean.  
- `git remote -v` may display nothing because the ZIP repository was not connected to GitHub.

If no remote is displayed, connect the repository:

git remote add origin GITHUB\_REPOSITORY\_URL

Replace `GITHUB_REPOSITORY_URL` with the HTTPS URL copied from the pair’s GitHub repository.

Verify the connection:

git remote \-v

Publish the existing commits, including the Activity 1 slogan commit:

git push \-u origin main

Open the repository on GitHub and confirm that the Activity 1 commit appears.

Record its short commit ID:

git log \--oneline \-3

Activity 1 commit ID: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

### Partner

Keep your previous Activity 1 folder as a backup. Do not use that folder for this activity.

Move outside the existing project folder and clone the pair’s GitHub repository into a new folder:

cd ..

git clone GITHUB\_REPOSITORY\_URL CSC350\_Git\_Story\_Lab\_partner

cd CSC350\_Git\_Story\_Lab\_partner

Verify the clone:

git status

git log \--oneline \-3

Expected:

- The working tree is clean.  
- The partner sees the same Activity 1 commit ID as the Author.

Partner’s Activity 1 commit ID: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Part 2 — Author creates and pushes a new commit

The Author opens `DECISIONS.md`.

Under `Accepted decisions`, add:

\- Decision: Use high-contrast signs at festival entrances.

\- Reason: Improve readability for visitors.

\- Contributor: YOUR\_PAIR\_NAMES

Replace `YOUR_PAIR_NAMES` with the partners’ names.

Save the file and inspect the change:

git status

git diff

Confirm that the diff contains only the intended decision entry.

Stage and review the file:

git add DECISIONS.md

git status

git diff \--staged

Commit the change locally:

git commit \-m "Record accessibility decision"

Verify the local commit:

git status

git log \--oneline \-3

At this point, the Author has committed but has not yet pushed.

Ask the Partner:

> Does your repository contain the new decision commit?

Expected answer: No. A local commit does not automatically update GitHub or the partner’s computer.

Publish the new commit:

git push

Verify that `Record accessibility decision` appears on GitHub.

Author’s new commit ID: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Part 3 — Partner pulls the new commit

Before pulling, the Partner runs:

git status

git log \--oneline \-3

Expected:

- The working tree is clean.  
- `Record accessibility decision` does not appear yet.

Now update the partner’s local repository:

git pull

git log \--oneline \-3

Open `DECISIONS.md` and confirm that the new accessibility decision appears.

Partner’s new commit ID: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Success evidence

- The Author sees both the Activity 1 commit and the new decision commit on GitHub.  
    
- The Partner’s clone initially contains the Activity 1 commit.  
    
- Before `git pull`, the Partner does not have the new decision commit.  
    
- After `git pull`, the Partner sees the new decision and the same commit ID as the Author.  
    
- Both students can explain:  
    
  - `git commit` records a change in the local repository.  
  - `git push` publishes local commits to GitHub.  
  - `git pull` obtains and integrates remote commits into the partner’s current branch.

## Stop and ask for help if

- `git remote -v` displays an unexpected repository.  
- The Partner is working inside their old Activity 1 folder.  
- `git status` shows unfinished changes before pulling.  
- Git reports divergent branches or a merge conflict.  
- Git requests a force push.

Do not use force push.  
