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
git checkout -b fix-greeting-bug
```

The `git checkout -b` command creates a new branch and automatically switches you to it. In this exercise, you are creating a branch called `fix-greeting-bug` where you will make your code changes.

## Checkpoint

Run:

```bash
git branch
```

You should see:

```text
* fix-greeting-bug
  main
```

The `*` shows which branch you are currently working on.

---
