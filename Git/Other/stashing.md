# Git Stashing

Stashing in Git is a way to temporarily save changes in your working directory that you’re not ready to commit yet. It’s useful when you need to switch branches or work on something else without committing your current changes.

## How Stashing Works

1. **Stash Your Changes:**
   `git stash`
    To save your current changes (both staged and unstaged) and revert your working directory to the last commit

2. **View Stashes:**
   `git stash list`
   To see a list of all stashed changes:
   Each stash is identified by a name like stash@{0}, stash@{1}, etc.

3. **Apply a Stash:**
   `git stash apply stash@{0}`
   If you have multiple stashes and want to apply a specific one, specify it.
   Note that apply keeps the stash in the list.

4. **Pop a Stash:**
   `git stash pop  stash@{0}`
   Reapply stash and stash and remove it from the stash list

5. **Drop a Stash:**
   `git stash drop stash@{0}`
   If you want to remove a specific stash without applying it

6. **Clear All Stashes:**
   `git stash clear`
   To remove all stashes

## Use Cases
**Context Switching:**
Save your progress and switch branches without committing unfinished work.

**Experimentation:**
Try out changes without risking your current work.

**Code Review**
Save changes to review or address issues without committing incomplete work.


