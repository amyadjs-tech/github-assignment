# github-assignment

# Question 1: Project Initialization & First Push

## Objective
Set up a new Git project and push it to a remote repository.

---

## Scenario
You are starting a new Python project. You need to track your work using Git and upload it to a remote repository.

---

# Steps

## 1. Create a New Project Folder

Create a new project folder where you want to save the Python project and then open that folder in VS Code.

---

## 2. Initialize a Git Repository

```bash
git init
```

---

## 3. Create `app.py` with Python Code

```bash
touch app.py
```

Open the file and add:

```python
print("Hello, This is Git-Github Assignment!")
```

---

## 4. Check Git Status

```bash
git status
```

You should see `app.py` as an untracked file.

## 5. Stage the File

```bash
git add app.py
```

---

## 6. Commit with a Meaningful Message

```bash
git commit -m "Initial commit: add app.py with basic Python code"
```

## 7. Create a Remote Repository

Go to GitHub (or GitLab/Bitbucket):

1. Click **New Repository**
2. Enter repository name: `my-python-project`
3. Do **NOT** initialize with README
4. Click **Create Repository**

---

## 8. Add Remote Repository (origin)

```bash
git remote add origin https://github.com/your-username/my-python-project.git
```
Below picture conatains all the above 8 steps.

<img width="1917" height="1027" alt="image" src="https://github.com/user-attachments/assets/7778f390-cd34-4f9f-99a9-bbbfb301f3e5" />

## 9. Verify Remote Configuration

```bash
git remote -v
```

Expected output:

```bash
origin  https://github.com/your-username/my-python-project.git (fetch)
origin  https://github.com/your-username/my-python-project.git (push)
```

---

## 10. Push Code to Remote Repository

```bash
git branch -M main
git push -u origin main
```

<img width="1917" height="1026" alt="image" src="https://github.com/user-attachments/assets/01598c85-d887-423d-9407-fe1aa7bee0b8" />

## Git Push Rejected Error Fix

The error occurred because the remote GitHub repository already contains some files (usually a `README.md`, `LICENSE`, or `.gitignore`) that are not present in your local repository.

Git prevents the push to avoid overwriting remote changes.

---

## Run the Following Command

```bash
git pull origin main --allow-unrelated-histories
```

<img width="1917" height="1026" alt="image" src="https://github.com/user-attachments/assets/c69c33b8-37df-4170-a520-9ce91c60ebb7" />

## If Git Opens an Editor for Merge Commit Message

1. Press `Esc`
2. Type:

```bash
:wq
```

3. Press `Enter`

---

## Push the Code Again

```bash
git push -u origin main
```

<img width="1917" height="1022" alt="image" src="https://github.com/user-attachments/assets/0a44a4b4-69ce-4740-9318-9d4bd487fd88" />

<img width="1917" height="962" alt="image" src="https://github.com/user-attachments/assets/ed98cecc-5fa6-49f6-b73c-92e60fe7ff9d" />

# Question 2: Working with Changes & History

## Objective
Track code changes and manage commit history properly.

---

## Scenario
You are enhancing your existing `app.py` application with new features.

---

# Steps

## 1. Modify `app.py` by Adding New Functionality

Update `app.py`:

```python
print("Hello, This is Git-Github Assignment!")
print("New Feature added")
```

---

## 2. Check What Changes Are Made Before Staging

```bash
git status
```

This command shows modified files before staging.

---

## 3. View Differences in the File

```bash
git diff
```
This displays the changes made inside `app.py`.

---
Above 3 steps in question number 2 are shown in below picture.

<img width="1917" height="1025" alt="image" src="https://github.com/user-attachments/assets/cdd0426d-7850-4520-8fd0-b9ccff729aa0" />

## 4. Stage Only Specific Changes (If Possible)

```bash
git add -p app.py
```

Git will ask which changes to stage.

Press:
- `y` → stage the change
- `n` → skip the change

---

## 5. Commit with a Clear Message

```bash
git commit -m "Added new feature message in app.py"
```

---

Steps 4 & 5 of question number 2 are shown in below picture.

<img width="1915" height="1022" alt="image" src="https://github.com/user-attachments/assets/7a3db125-67b6-43cf-9add-746f13585e45" />

## 6. Make Another Change in `app.py`

Add another line:

```python
print("Hello, This is Git-Github Assignment!")
print("New Feature added")
print("Second Feature added")
```

---

## 7. Stage All Changes

```bash
git add .
```

---

## 8. Commit Again

```bash
git commit -m "Added second feature message in app.py"
```
Steps 6, 7 & 8 of question number 2 are shown in below picture.

<img width="1917" height="1022" alt="image" src="https://github.com/user-attachments/assets/1f999400-e193-4a7a-8eee-96d8a2f861f5" />

## 9. View Full Commit History

```bash
git log
```

This shows:
- Commit ID
- Author
- Date
- Commit message

---
Steps 9 of question number 2 is shown in below picture.

<img width="1917" height="1030" alt="image" src="https://github.com/user-attachments/assets/08f6c126-38cf-43ba-a04b-a1bc914d238f" />

## 10. View Compact (One-Line) History

```bash
git log --oneline
```

Example output:

```bash
8deccab Added second feature message in app.py
c014093 Added new feature message in app.py
a1b2c3d Initial commit
```
Steps 10 of question number 2 is shown in below picture.

<img width="1917" height="1026" alt="image" src="https://github.com/user-attachments/assets/0668e3a8-22c9-4b51-9f5f-ba4784d8d5d3" />

# Result

You have successfully:

- Modified files in Git
- Viewed file differences
- Staged changes selectively
- Created multiple commits
- Viewed detailed and compact commit histor

# Question 3: Branching & Feature Development

## Objective
Work with branches and manage feature development.

---

## Scenario
You are developing a new feature separately to avoid affecting the main code.

---

# Steps

## 1. Create a New Branch (`feature-update`)

```bash
git branch feature-update
```

---

## 2. Switch to the New Branch

```bash
git checkout feature-update
```

Alternative command:

```bash
git switch feature-update
```

---

## 3. Modify `app.py` with New Feature Logic

Update `app.py`:

```python
print("Hello, This is Git-Github Assignment!")
print("New Feature added")
print("Second Feature added")
print("Feature Update Branch Logic Added")
```

---

## 4. Stage and Commit the Changes

### Stage Changes

```bash
git add app.py
```

### Commit Changes

```bash
git commit -m "Added feature update logic in app.py"
```

---

## 5. Switch Back to the `main` Branch

```bash
git checkout main
```

Alternative command:

```bash
git switch main
```

---

## 6. Merge the Feature Branch into `main`

```bash
git merge feature-update
```

---

Steps 1, 2, 3, 4, 5 & 6 of question number 3 are shown in below picture.

<img width="1917" height="1026" alt="image" src="https://github.com/user-attachments/assets/64ef532f-8c09-4dd4-ac50-83908c822815" />

## 7. Verify Changes are Merged

### Check `app.py`

```python
print("Hello, This is Git-Github Assignment!")
print("New Feature added")
print("Second Feature added")
print("Feature Update Branch Logic Added")
```

### Check Commit History

```bash
git log --oneline
```

---
Step 7 of question number 3 are shown in below picture.

<img width="1917" height="1022" alt="image" src="https://github.com/user-attachments/assets/6f523b43-9434-4e0a-b646-cdb60c70eb18" />

## 8. Delete the Branch Safely

```bash
git branch -d feature-update
```

This deletes the branch only if it has been merged successfully.

---

## 9. Try Force Deleting a Branch (Dummy Branch Example)

### Create Dummy Branch

```bash
git branch dummy-branch
```

### Force Delete Dummy Branch

```bash
git branch -D dummy-branch
```

`-D` force deletes the branch even if it is not merged.

---

Steps 8 & 9 of question number 3 are shown in below picture.

<img width="1917" height="1026" alt="image" src="https://github.com/user-attachments/assets/afaf201f-7bd9-4508-9a16-604c157e4737" />

# Result

You have successfully:

- Created and switched branches
- Developed features separately
- Merged changes into `main`
- Verified merged updates
- Deleted branches safely and forcefully

  # Question 4: Handling Errors (Stash, Reset, Revert)

## Objective
Learn how to manage mistakes and unfinished work.

---

## Scenario
You are in the middle of development but need to handle urgent changes and fix mistakes.

---

# Steps

## 1. Make Changes to `app.py` but Do NOT Commit

Update `app.py`:

```python
print("Hello, This is Git-Github Assignment!")
print("Temporary Development Changes")
```

Create an untracked file:

```bash
touch notes.txt
```

---

## 2. Stash the Changes (Including Untracked Files)

```bash
git stash -u
```

Explanation:
- `-u` includes untracked files in the stash.

---

## 3. Check the Stash List

```bash
git stash list
```

Example output:

```bash
stash@{0}: WIP on main: abc1234 Temporary changes
```

---

## 4. Apply the Stashed Changes Back

```bash
git stash apply
```

This restores the stashed changes without deleting the stash entry.

---

Steps 1, 2, 3 & 4 of question number 4 are shown in below picture.

<img width="1917" height="1031" alt="image" src="https://github.com/user-attachments/assets/6851239c-5a6c-4ab6-842c-18f9c0a6b19b" />

## 5. Commit the Changes

### Stage Changes

```bash
git add .
```

### Commit Changes

```bash
git commit -m "Added temporary development changes"
```

---

## 6. Make Another Commit with Incorrect Code

Update `app.py`:

```python
print("Incorrect Buggy Code")
```

### Stage and Commit

```bash
git add app.py
git commit -m "Added incorrect buggy code"
```

---

## 7. Undo the Last Commit Using Reset

### Keep Changes but Remove Commit

```bash
git reset --soft HEAD~1
```

Explanation:
- Removes the last commit
- Keeps changes staged

Alternative:

```bash
git reset --hard HEAD~1
```

⚠️ `--hard` removes both commit and changes permanently.

---

## 8. Make Another Commit

Correct `app.py`:

```python
print("Corrected Application Code")
```

### Stage and Commit

```bash
git add app.py
git commit -m "Fixed incorrect code issue"
```

---

## 9. Undo a Commit Using Revert

```bash
git revert HEAD
```

Explanation:
- Creates a new commit that reverses the previous commit
- Safer for shared repositories

If editor opens:
1. Press `Esc`
2. Type:

```bash
:wq
```

3. Press `Enter`

---

Steps 5, 6, 7, 8 & 9 of question number 4 are shown in below picture.

<img width="1917" height="1025" alt="image" src="https://github.com/user-attachments/assets/22658e0f-09f5-4ea6-9254-b711b51f07db" />

## 10. Verify the Commit History

### Full History

```bash
git log
```

### Compact History

```bash
git log --oneline
```

Example output:

```bash
f7h8i9j Revert "Fixed incorrect code issue"
e4f5g6h Fixed incorrect code issue
a1b2c3d Added temporary development changes
```
Step 10 of question number 4 are shown in below picture.
<img width="1917" height="1022" alt="image" src="https://github.com/user-attachments/assets/faad5dde-f06c-49b6-b37a-bc62942a5166" />
<img width="1917" height="1026" alt="image" src="https://github.com/user-attachments/assets/a4bf2e1c-9861-4eda-b040-c80f2bddf744" />

# Result

You have successfully learned how to:

- Stash unfinished work
- Restore stashed changes
- Undo commits using reset
- Reverse commits safely using revert
- Verify commit history



























