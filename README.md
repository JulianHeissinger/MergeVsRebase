# Merge: 

1. We created a new repo and added the file onMain.md. We opened the repo and used git add . and git commit / git push to save the file.
2. We used git checkout -b a-feature to create the branch and switch to it directly.
Then we created a new file called onBranch.md inside this branch.
3. We wrote some text into the file onBranch.md and committed it.
4. We used git log to look at the commit history of the feature branch.
5. We switched with git checkout main and then used git log again. On the main branch, we cannot see what happened on the feature branch because the commits are separate.
6. The main branch only contains the commits made on main.The feature branch contains additional commits, so the new File and its changes.
This happens because branches in Git move independently until they are merged.
7. We added more text to onMain.md, then used git add and git commit to save the changes.We repeated this step several times, so the main branch continued to move forward.
8. Running git log now shows more commits on the main branch.
9. The difference is that the work we did on the feature branch only exists in the feature branch.
10. We used git merge main, this brought all new changes from the main branch into the feature branch.
11. After the merge, the featur12.  branch  includes: the commits originally made in the feature branch, the new commits from the main branch and the merge commit itself. The histories are now combined, so the feature branch is up to date with main.
12. After switching to the feature branch and running git log, the history looks shows that the merge commit at the top, the main commits you added later, The feature commits (Add onBranch.md + Update onBranch.md) and The original first commit (Add onMain.md)

# Rebase:

We made the same steps till step 11

11.  We switched to the feature branch and used git rebase main. This moved our feature commits on top of the newest main commits. After the rebase, the history is clean and linear — first the main commits, then the feature commits, and no merge commit.
12.  Running git log on the feature branch shows a straight history: main’s commits first, followed by our feature commits. There is no merge commit because rebase rewrites the history.
