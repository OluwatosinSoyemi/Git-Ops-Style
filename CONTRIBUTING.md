# Contributing Guidelines

Thank you for contributing to this project. This guide explains the development workflow, rules, and standards to follow when working on the project.

---

## Full Development Workflow

This project follows a GitOps-style workflow that integrates Trello, GitHub, and GitHub Actions.

1. Select a task from the Trello board (e.g., TRELLO-001)
2. Create a feature branch for the task
3. Begin development on the feature branch
4. Commit changes using the Trello ID
5. Push the feature branch to GitHub
6. When code is pushed, the Trello card reflects **In Progress**
7. Open a pull request (PR) targeting the `main` branch
8. When a PR is opened, the Trello card reflects **Review/QA**
9. GitHub Actions automatically runs CI checks (linting and testing)
10. Fix any issues if tests or linting fail
11. Merge the PR only after all checks pass
12. When the PR is merged, the Trello card reflects **Done**

The workflow stages are:

**Backlog → In Progress → Review/QA → Done**

Card movement reflects development progress and is aligned with GitHub actions such as pushes, pull requests, and merges.

---

## Branching Rules

* The `main` branch is protected and must always remain stable
* No direct pushes to `main` are allowed
* All development must be done in feature branches

Branch naming format:

feature/TRELLO-###-description

Example:

feature/TRELLO-003 API Docs

---

## Commit Format

All commits must reference a Trello ID.

Format:

[TRELLO-003] Add documentattion and screenshots


This ensures traceability between tasks and code changes.

---

## Pull Request (PR) Process

1. Push your feature branch to GitHub
2. Open a pull request targeting the `main` branch
3. Ensure the PR title includes the Trello ID
4. Wait for CI checks to complete
5. Fix any issues if checks fail
6. Merge only when all checks pass

---

## CI/CD Pipeline Explanation

The project uses GitHub Actions for Continuous Integration.

The pipeline runs automatically on:

* Push to feature branches
* Pull requests to the `main` branch

Pipeline steps:

1. Install dependencies
2. Run lint checks using flake8
3. Run tests using pytest

If any step fails:

* The build is marked as failed
* The pull request is blocked from merging

---

## Coding Standards

* Follow Python style guidelines
* Ensure all tests pass before committing
* Write clean, readable, and maintainable code
* Use meaningful and descriptive commit messages
* Avoid unused code or debug statements

---

## Failure Handling

If the CI pipeline fails:

1. Check GitHub Actions logs
2. Identify the cause of failure
3. Fix the issue locally
4. Re-run tests and lint checks
5. Commit and push the fix

The CI pipeline will automatically run again.

Pull requests cannot be merged until all checks pass.

---

## Summary

This workflow ensures:

* High code quality
* Automated validation through CI/CD
* Clear traceability between tasks and code
* Consistent and structured collaboration

Following these guidelines helps maintain a reliable and scalable development process.
