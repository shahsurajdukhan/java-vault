That's a great idea. Having a Git cheat sheet will save you a lot of time at work. Here's a practical list of the Git commands you'll use most often as a software engineer.

Git Cheat Sheet (Developer Reference)

1. Check Repository Status

git status

Shows the current status of your repository.

Displays modified, staged, and untracked files.

Use: First command to run before doing anything.




---

2. Clone Repository

git clone <repository-url>

Downloads a remote repository to your computer.

Use: When working on a project for the first time.



Example:

git clone https://github.com/company/project.git


---

3. Check Current Branch

git branch

Lists all local branches.

The * indicates your current branch.




---

4. View Remote Branches

git branch -r

Shows branches available on the remote repository.




---

5. View All Branches

git branch -a

Shows both local and remote branches.




---

6. Create a New Branch

git branch <branch-name>

Creates a new branch.

Does not switch to it.



Example:

git branch feature/login


---

7. Switch Branch

git checkout <branch-name>

Switches to an existing branch.



OR (recommended)

git switch <branch-name>

Modern way to switch branches.




---

8. Create and Switch Together

git checkout -b <branch-name>


OR

git switch -c <branch-name>

Creates a new branch and switches to it immediately.




---

9. Delete Local Branch

git branch -d <branch-name>

Deletes a merged branch.


git branch -D <branch-name>

Force deletes a branch.




---

10. Rename Branch

git branch -m new-name

Renames the current branch.




---

Working with Files

11. Stage All Changes

git add .

Stages all new and modified files.




---

12. Stage One File

git add filename

Stages only a specific file.




---

13. Unstage a File

git restore --staged filename

Removes a file from the staging area.




---

14. Discard Local Changes

git restore filename

Discards changes made to a file.




---

Commit

15. Commit Changes


git commit -m "Your message"

Saves staged changes into Git history.



Example:

git commit -m "Fix login validation"


---

16. Amend Last Commit

git commit --amend

Modify the last commit message or include forgotten changes.




---

Remote Repository

17. View Remote

git remote -v

Shows remote repository URLs.




---

18. Add Remote

git remote add origin <url>

Connects your local repository to a remote.




---

Push

19. Push Existing Branch

git push

Pushes commits to the remote.




---

20. Push Local Branch for First Time

git push -u origin <branch-name>

Creates the branch on GitHub/GitLab and links it to your local branch.

After this, you can simply use git push.




---

21. Force Push

git push --force


OR safer

git push --force-with-lease

Replaces remote history.

Use carefully, especially on shared branches.




---

Pull

22. Pull Latest Changes

git pull

Downloads and merges remote changes into your current branch.




---

23. Fetch Changes

git fetch

Downloads remote changes without merging them.




---

24. Pull with Rebase

git pull --rebase

Applies your commits on top of the latest remote changes.

Keeps history cleaner.




---

Merge

25. Merge Another Branch

git merge branch-name

Merges another branch into your current branch.




---

Rebase

26. Rebase

git rebase main

Replays your commits on top of another branch.

Produces a cleaner commit history.




---

27. Continue Rebase

git rebase --continue

Continues after resolving conflicts.




---

28. Abort Rebase

git rebase --abort

Cancels the rebase.




---

Merge Conflicts

29. See Conflicted Files

git status

Lists files with merge conflicts.




---

30. Continue Merge

git add .
git commit

Marks conflicts as resolved and finishes the merge.



---

Log & History

31. Commit History

git log

Shows all commits.




---

32. Short History

git log --oneline

Compact commit history.




---

33. Graph View

git log --oneline --graph --all

Displays branch structure visually.




---

Compare Changes

34. View Unstaged Changes

git diff

Shows changes not yet staged.




---

35. View Staged Changes

git diff --staged

Shows staged changes.




---

Undo

36. Undo Last Commit (Keep Changes)

git reset --soft HEAD~1

Removes the last commit while keeping your changes staged.




---

37. Undo Last Commit (Unstage Changes)

git reset HEAD~1

Removes the last commit and unstages the changes.




---

38. Remove Last Commit Completely

git reset --hard HEAD~1

Deletes the last commit and all associated changes permanently.




---

Stash

39. Save Temporary Work

git stash

Temporarily stores your uncommitted changes.




---

40. List Stashes

git stash list

Shows all saved stashes.




---

41. Restore Latest Stash

git stash pop

Applies the latest stash and removes it from the stash list.




---

42. Apply Stash Without Removing

git stash apply

Restores a stash but keeps it saved.




---

Tags

43. Create Tag

git tag v1.0

Creates a version tag.




---

44. Push Tags

git push origin --tags

Pushes all local tags to the remote.




---

Clean

45. Remove Untracked Files

git clean -fd

Deletes untracked files and directories.




---

Configuration

46. Check Username

git config user.name



---

47. Check Email

git config user.email



---

48. Set Username

git config --global user.name "Your Name"



---

49. Set Email

git config --global user.email "you@example.com"



---

Inspect

50. Show Current Commit

git show

Displays details of the latest commit.




---

51. See File Changes in a Commit

git show <commit-id>



---

Cherry Pick

52. Copy One Commit

git cherry-pick <commit-id>

Applies a specific commit from another branch to the current branch.




---

Restore Deleted File

53. Restore File

git checkout HEAD -- filename


OR

git restore filename



---

Remove File from Git

54. Remove Tracked File

git rm filename

Deletes a file and stages its removal.




---

Useful Workflow (Most Common at Work)

Create a New Feature Branch

git checkout main
git pull
git checkout -b feature/new-feature

Work and Commit

git status
git add .
git commit -m "Implement new feature"

Push for First Time

git push -u origin feature/new-feature

Keep Branch Updated

git checkout main
git pull
git checkout feature/new-feature
git rebase main

Push After Rebase

git push --force-with-lease

Merge Main into Feature (Alternative to Rebase)

git checkout feature/new-feature
git fetch origin
git merge origin/main

Daily Workflow

git status
git pull --rebase
git add .
git commit -m "Describe your changes"
git push

Pro Tips

Run git status frequently—it tells you exactly what's happening.

Use git fetch before inspecting remote changes without modifying your branch.

Prefer git pull --rebase for a cleaner history if your team uses rebasing.

Use git push --force-with-lease instead of --force after a rebase.

Write clear, meaningful commit messages (e.g., "Fix login validation" instead of "changes").


$$
	This cheat sheet covers 95% of the Git commands you'll use in day-to-day software development, including feature development, code reviews, bug fixes, and collaborating with teammates.

---

$$