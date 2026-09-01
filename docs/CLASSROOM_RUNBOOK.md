# Classroom Runbook

This is a compact backup to the speaker notes in the lecture deck.

## Suggested timing: 110 minutes

| Segment | Time | Instructor action | Student action |
|---|---:|---|---|
| Mental model | 15 min | Explain Git, GitHub, VS Code, and the three local areas | Predict where a change lives |
| First local snapshot | 20 min | Demonstrate edit → diff → stage → commit | Complete Activity 01 |
| Remote synchronization | 15 min | Demonstrate remote, push, pull | Complete Activity 02 |
| Branch and merge | 20 min | Demonstrate branch isolation and local merge | Complete Activities 03–04 |
| Pull Request review | 20 min | Demonstrate PR creation and review | Complete Activity 05 |
| Conflict and recovery | 15 min | Merge competing edits and resolve | Complete Activity 06 |
| Assessment | 5 min | Run exit checks | Complete Activity 08 |

## Teaching pattern for every command

1. Predict: ask what students expect to change.
2. Execute: run one command only.
3. Read: interpret the first useful line of output.
4. Verify: run `git status`, inspect the file, or check GitHub.

## High-value questions

- If a file is saved in VS Code, has Git saved a version? No; it is only in the working tree.
- If a file is staged, is it on GitHub? No; staging is local preparation.
- If a change is committed, can classmates pull it? Only after it is pushed to a reachable remote branch.
- Does a Pull Request move files from a laptop? No; push publishes commits, then the PR proposes merging branches.
- Is a merge conflict a broken repository? No; Git has paused and needs a human decision.

## Network-failure alternative

Skip GitHub-specific screens but preserve the concepts locally:

1. Create two local branches from `main`.
2. Commit a different change on each branch.
3. Merge both into `main`.
4. Use the second merge to demonstrate a conflict.
5. Explain that a GitHub Pull Request adds hosted comparison, discussion, review, and a merge decision around the same branch relationship.

