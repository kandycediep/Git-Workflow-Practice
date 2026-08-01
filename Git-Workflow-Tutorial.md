# Your First Git Workflow!!

In this exercise, you'll complete the same Git workflow you'll use on a real team:

**clone → branch → edit → stage → commit → push → pull request**

Follow each step in order. If a checkpoint doesn't match what you see, go back and double-check the previous step before continuing.

# Before You Start
- Git installed
- GitHub account
- Repository access

# Step 1: Clone the Repository

## Goal

Download a copy of this repository to your machine so you can work on it locally. This will give you access to the starter code you'll modify during this exercise.

## Command

First, open a terminal on your machine and navigate to the location where you want to save this repository.

1. Go to this repository on GitHub.
2. Click the green **Code** button.
3. Select **HTTPS** and copy the URL.
4. Paste it where you see `<repository-url>` below.

```bash
git clone <repository-url>
cd git-workflow-practice
```

The `git clone` command downloads a copy of the repository to your machine. The `cd` command moves you into the project folder so you can start working.

<img width="1176" height="765" alt="Recording 2026-08-01 at 19 08 56" src="https://github.com/user-attachments/assets/49dccc63-6dd0-4331-82b5-5b54b9150ffd" />

## Checkpoint

Run:

```bash
git status
```

You should see:

```text
On branch main
nothing to commit, working tree clean
```

---

# Step 2: Create a Branch

## Goal

Create a new branch for your changes. A branch keeps your work separate from `main` until it is ready to be reviewed and merged.

## Command

Before making any changes, create and switch to your own branch.

Run:

```bash
git checkout -b fixing-greeting-bug
```

The `git checkout -b` command creates a new branch and automatically switches you to it. In this exercise, you are creating a branch called `fixing-greeting-bug` where you will make your code changes.

## Checkpoint

Run:

```bash
git branch
```

You should see:

```text
* fixing-greeting-bug
  main
```

The `*` shows which branch you are currently working on.

---

# Step 3: Make a Change

## Goal

Fix a small bug in the starter code. This will be the change you commit and submit in your Pull Request.

## Command

Open:

```text
greeting.py
```

The `welcome_message()` function contains a typo in the welcome message. Update the function so it returns:

```text
Welcome to the team!
```

instead of:

```text
Welcom to the team!
```

Save the file after making your change.

## Checkpoint

Run:

```bash
python greeting.py
```

You should see:

```text
Welcome to the team!
```

This confirms that your change was successful.

---

# Step 4: Review Your Changes

## Goal

Check which files you changed and review the exact updates before saving them in a commit.

## Command

Run:

```bash
git status
```

This shows which files Git noticed have changed.

Next, run:

```bash
git diff
```

This shows the exact lines that were added, removed, or modified.

## Checkpoint

After editing `greeting.py`, you should see it listed when you run:

```bash
git status
```

Example:

```text
Changes not staged for commit:
  modified:   greeting.py
```

Running:

```bash
git diff
```

should show your typo fix:

```diff
- return "Welcom to the team!"
+ return "Welcome to the team!"
```

---

# Step 5: Stage Your Change

## Goal

Tell Git which changes you want to include in your next commit.

## Command

Run:

```bash
git add greeting.py
```

The `git add` command moves your changes into the staging area. This tells Git that you are ready to include this file in your next commit.

## Checkpoint

Run:

```bash
git status
```

You should see:

```text
Changes to be committed:
  modified:   greeting.py
```

The file should appear under **"Changes to be committed"**, which means it is ready to be saved in your next commit.

---

# Step 7: Push Your Branch to GitHub

## Goal

Upload your branch and its commit to GitHub so your changes are available for review.

## Command

Run:

```bash
git push origin fixing-greeting-bug
```

The `git push` command uploads your local branch and its commits to GitHub. The `origin` refers to the remote repository where your project is stored.

## Checkpoint

Go to this repository on GitHub and refresh the page.

You should see a banner suggesting you open a Pull Request for:

```text
fixing-greeting-bug
```

This confirms that your branch was successfully pushed to GitHub.

---

# Step 8: Open a Pull Request

## Goal

Create a Pull Request (PR) to propose merging your branch into `main`. A PR allows teammates to review your changes before they are added to the main codebase.

## Command

On GitHub:

1. Click **"Compare & pull request"** after pushing your branch.
2. Make sure the PR is comparing:

```text
fixing-greeting-bug → main
```

3. Add a short title, for example:

```text
Fix welcome message typo
```

4. In the description, briefly explain:
   - What you changed
   - Why you made the change

5. Click **Create pull request**.

<img width="1176" height="765" alt="Recording 2026-08-01 at 19 43 39" src="https://github.com/user-attachments/assets/2e92d3d6-61ae-4356-b1f5-8656ec35b2a4" />


## Checkpoint

You should now have an open Pull Request on GitHub.

On a real team, this is where a teammate would review your changes, leave feedback, and approve the update before it is merged.

---

# 🎉 You Completed Your First Git Workflow

clone → branch → edit → stage → commit → push → PR

Nice work! You just completed the core Git workflow that you'll use for most changes on a development team. The code you change will vary, but the Git process stays the same.

## What's Next?

This tutorial covered the basics. Future versions will include:

- Handling merge conflicts
- Responding to code review comments
- Keeping your branch updated with `git pull`
