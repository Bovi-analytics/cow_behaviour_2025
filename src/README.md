# Project Template

## Overview

This repository serves as a template for organizing machine learning projects throughout the organization. It provides a standardized directory structure to ensure consistency, modularity, and efficient collaboration across teams. The template includes placeholders for:

- **Python Scripts (.py):** Core functionalities and modules.
- **Jupyter Notebooks (.ipynb):** Pipelines and experimentation.
- **Organized Directories:** For data, models, utilities, and more.

Teams are encouraged to use this template as a starting point for their projects and customize it according to their specific needs. The same tree structure should be used in Blob Storage for consistent data organization.

## Directory Structure

![Dir tree](misc/readme_data/dir_tree.png?raw=true "Dir tree")

## Usage Instructions

### 1. Forking the Template Repository

To work with this template and have a workflow that allows for later updates and pull requests on shared code (for example, enhancements to utility functions), you should **fork the repository from the organization rather than creating a repository from a template**. Forking retains the full commit history and establishes a connection to the main template so you can pull in updates later.

**Steps to fork and clone:**

1. **Fork the Repository:**
In GitHub, navigate to the organization’s template repository and click **Fork**. This creates an independent copy of the repository under your own GitHub account.
2. **Clone Your Fork Locally:**
Replace `<your-fork-url>` with your fork’s URL and `<new-project-name>` with your desired project directory name:

```bash
git clone <your-fork-url> <new-project-name>
cd <new-project-name>
```

3. **Set Up the Upstream Remote:**
This connects your fork back to the original template repository, making it easy to pull in any updates:

```bash
git remote add upstream https://github.com/<org-name>/project_template.git
```


### 2. Customizing the Template

Once you’ve cloned your fork, customize your project as needed:

- **Add Your Models:**
Place your specific models under `src/pyfiles/models/`.
- **Implement Utility Functions:**
Add or update shared utilities in `src/pyfiles/utils/`.
- **Develop Pipelines:**
Use the `notebooks/pipelines/` directory for experimentation or pipeline development.
- **Organize Your Data:**
Organize your data under `data/models/`, following the same structure used in the template.


### 3. Keeping Shared Files Updated

To ensure that shared files (e.g., utility functions, abstract classes like `initialize.py` and `inference.py`) remain up to date with the improvements in the main template, follow these steps:

1. **Fetch Updates from Upstream:**

```bash
git fetch upstream
```

2. **Merge Changes from the Upstream Main Branch:**

```bash
git pull upstream main
```

Resolve any conflicts that might arise and commit the merge. This will keep your fork synchronized with shared updates from the original template.

### 4. Contributing Back to the Template

If you make improvements to shared files that could benefit all teams, consider contributing back to the original template repository:

1. **Commit Your Changes:**
Commit your changes in your fork with a clear message.
2. **Push Changes to Your Fork:**
Push your commits to your GitHub fork.
3. **Open a Pull Request:**
On GitHub, navigate to your fork, click **New pull request**, and ensure that the base repository is the original template repository. Provide a detailed description of your changes so that reviewers have context.

## Forking vs. Repository Templates

### Forking:

- **Retains Full History and Connection:**
Your fork includes the entire commit history and maintains an explicit link (via the upstream remote) with the original template.
- **Facilitates Updates and Collaboration:**
You can easily fetch updates from the main template and contribute enhancements back via pull requests.


### Repository Templates:

- **Creates an Independent Copy:**
When you create a new repository from a template, you get the standardized directory structure, but without history, making it difficult to merge updates later.
- **Suitable for One-Time Setup:**
This approach is useful for quickly starting projects when ongoing contributions or updates to the template are not required.

For ongoing collaboration and shared improvements, **forking** is the recommended workflow.
