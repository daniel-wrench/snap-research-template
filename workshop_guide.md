# Introduction to Reproducible Research
### SNAP workshop, February 20th 2025

Have cloned GitHub that has much of this.
Could get students to clone this too, and then go through steps of adding a simple script, committing, tracking changes, undoing.
Setting up and installing virtual environment: see here for improvement on pip freeze https://calmcode.io/course/pip-tools/compile 

See here for general principles: https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510 

## TO-DO
-   Create git repo with this file, called `snap-research-template`. Confirm can view this file on GitHub
-   As with quick version I made, have the appropriate folders (maybe re-fork?)
-   Referring to notebook, lay out our plan of attack. Some things will be already provided (requirements.txt, initialised git repo), but we will also describe how these are created if you are **starting from scratch**.
-   Refer to Git carpentry to confirm that content
-   Let Alexa know about workshop

## Introduction

### What is reproducible research?

-   A.K.A. open science, sustainable software
-   Ensures collaboration, longevity, and transparency.
-   Key pillars: version control, environments, structure.
-   Demo: A messy vs. well-structured research project.
-   What won't we be covering?
    -   Containers
    -   Object-oriented programming
    -   Testing, `__init__.py` files, and other aspects of creating a piece of "software" (i.e. R/Python library/package)
-   Instead, we are focusing on creating a reproducible **data pipeline**, as one would encounter in a scientific analysis and would typically (but not necessarily) be limited to step-by-step, functional-style programming. 

## Prerequisites

Participants should have installed:

-   VS Code (with Python and Git extensions)

-   Git (configured: check with `git config --list` )

    -   `git config --global user.name "Your Name"`

    -   `git config --global user.email "you@example.com"`

-   Python (latest stable version, e.g., 3.10+)

-   An active GitHub account

## Version Control with Git and GitHub

### Why Use Git?

-   Tracks changes, enables collaboration.
-   Local vs. remote repositories.

### Hands-on: Initializing a Git Repository

``` bash
git init
git status
git add .
git commit -m "First commit"
.gitignore (e.g., ignore __pycache__/, .venv/, data/)
```

### Pushing to GitHub

``` bash
git remote add origin <repo-url>
git push -u origin main
```

### Branching and Collaboration

``` bash
git checkout -b new-feature
git merge new-feature
git pull origin main
```

## Virtual Environments and Dependency Management

### Why Use Virtual Environments?

-   Prevents dependency conflicts.
-   Important part of research reproducibility.
-   May have heard of Docker or Singularity: "containers" for greater independence of software from your machine. Here we will stick with the basic but very common implementation: virtual environments and the requirements.txt file.
-   *If people already know about these, they can look into*

### Setting Up a Virtual Environment

``` bash
python -m venv .venv
source .venv/bin/activate   # macOS/Linux
.venv\Scripts\activate     # Windows
pip install pandas numpy matplotlib
pip freeze > requirements.txt

pip install -r requirements.txt
```

## Structuring a Research Repository

### Recommended folder structure:

```         
project-name
├── data/          # Raw & processed data (ignored in Git)
├── scripts/       # Python or R scripts
├── notebooks/     # Jupyter notebooks
├── results/       # Figures, tables, outputs
├── doc/           # Documents, manuscript, reports
├── README.md      # Project overview
├── requirements.txt  # Dependencies
├── .gitignore     # Ignoring unnecessary files
├── LICENSE        # Licensing (MIT, GPL, etc.)
├── environment.yml  # Conda environment file (if used)
```

## GitHub Co-Pilot

-   Free version available with limited number of requests (2000 code completions/month, 50 queries): github.com

-   Pro version available if you sign up (for free) for student package: <https://github.com/education/students>

## Wrap-Up and Q&A

-   Recap key takeaways.
-   Provide resources (Software Carpentry, The Turing Way).
-   Open Q&A and troubleshooting.
-   **Provide template for working reproducible research repo on GitHub? With some instructions in README, e.g. for installing virtual environment, what else should be in README**