# Task 2 – Git and GitHub Workflow

## Branch Structure
- main: stable production branch
- dev: integration branch for features
- feature1: adds new gameplay behavior
- feature2: extends game logic
- feature3: implements hint system
- hotfix: urgent production fix
- documentation: repository documentation and learning summary

## Purpose
This repository demonstrates advanced Git workflows including merging,
rebasing, squashing commits, and cherry-picking hotfixes.

## Learning Summary

### Merge vs Rebase
- **Merge** preserves full branch history and shows where changes came from.
  I used merge when integrating feature branches into `dev` and syncing `main` back into `dev`.
- **Rebase** rewrites history to create a linear commit sequence.
  I rebased `feature2` onto `dev` to keep the history clean before merging.

### Squash
- Squashing combines multiple commits into one.
- This is useful to clean up messy development history before merging into shared branches.
- Squashing reduces noise in the `dev` branch.

### Cherry-Pick
- Cherry-pick applies a single commit from one branch to another.
- I used cherry-pick to apply a hotfix directly to `main` without merging all `dev` changes.
- This is ideal for urgent production fixes.

### Branch History Observations
- `feature1` used a merge-based workflow and shows merge commits.
- `feature2` was rebased, resulting in a clean, linear history.
- `feature3` (if inspected) demonstrates how squashing simplifies history.

### When to Use Each Strategy
- Use **merge** when preserving full collaboration history is important.
- Use **rebase** when working alone on a feature and wanting a clean history.
- Use **squash** before merging features to reduce commit clutter.
- Use **cherry-pick** for selective fixes across branches.