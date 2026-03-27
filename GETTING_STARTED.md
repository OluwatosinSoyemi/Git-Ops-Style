# Getting Started

This guide helps a new contributor set up the project and start contributing in under one hour.

---

## Environment Setup

### 1. Clone the Repository

git clone https://github.com/OluwatosinSoyemi/Git-Ops-Style
cd Git-Ops-Style


---

### 2. Install Dependencies

Ensure Python is installed (Python 3.10 or higher).

Then install required packages:

pip install -r requirements.txt


---

### 3. Verify Installation

Run the tests to confirm everything is working:

pytest -v

You should see all tests passing.

---

## Running Tests

Tests are written using pytest.

To run tests:

pytest -v


To check code quality using linting:

flake8 app.py test_app.py

All tests must pass and no linting errors should exist before pushing code.

---

## Branch Workflow

This project uses a feature-branch workflow.

### 1. Switch to main branch

git checkout main
git pull

---

### 2. Create a new feature branch

git checkout -b feature/TRELLO-XXX-description

Example:

git checkout -b feature/TRELLO-004 CONTRIBUTING guide


---

### 3. Make changes and commit

git add .
git commit -m "[TRELLO-XXX] Short description" 

Example:

git commit -m "[TRELLO-004] Add contributory guides"


---

### 4. Workflow Tracking

Trello cards reflect development progress based on Git actions:

- Push → In Progress
- Pull Request → Review/QA
- Merge → Done 

---

## Pull Request (PR) Creation

### 1. Push your branch

git push origin feature/TRELLO-XXX-description


---

### 2. Open Pull Request on GitHub

* Go to your repository on GitHub
* Click "Compare & pull request"
* Ensure base branch is `main`
* Add a title including Trello ID

Example:

[TRELLO-004] CONTRIBUTING guide


---

### 3. Wait for CI Checks

GitHub Actions will automatically:

* Install dependencies
* Run lint checks
* Run tests

---

### 4. Merge the Pull Request

* Only merge if all checks pass (green)
* If checks fail, fix the issues and push again

---

## Troubleshooting

### Tests Failing

* Run tests locally:

  pytest -v

* Fix any failing test cases

---

### Lint Errors

* Run:

  flake8 app.py test_app.py

* Fix formatting or syntax issues

---

### Merge Blocked

* Ensure CI checks are passing
* Check GitHub Actions logs for errors

---

### Dependency Issues

* Reinstall dependencies:

  pip install -r requirements.txt

---






