# Project Template

## Overview

This repository serves as a template for organizing machine learning projects throughout the organization. It provides a standardized directory structure to ensure consistency, modularity, and efficient collaboration across teams. The template includes placeholders for:

- **Python Scripts (.py):** Core functionalities and modules.
- **Jupyter Notebooks (.ipynb):** Pipelines and experimentation.
- **Organized Directories:** For data, models, utilities, and more.

Teams are encouraged to use this template as a starting point for their projects and customize it according to their specific needs. The same tree structure should be used in Blob Storage for consistent data organization.

---

## Directory Structure

![Dir tree](src/misc/readme_data/dir_tree.png?raw=true "Dir tree")

---

## Usage Instructions

### 1. Forking the Template Repository

To work with this template while keeping the original clean, you should **fork the repository from the organization**. Forking creates an independent copy of the repository under your account while maintaining a connection to the original (parent) repository. This allows you to:

- Work privately on your fork without affecting the original.
- Pull updates from the original template when needed.
- Contribute improvements back to the original by creating pull requests.


#### **Steps to Fork and Clone:**

1. **Fork the Repository:**
    - Go to the organization’s template repository on GitHub.
    - Click **Fork** in the top-right corner. This creates a copy of the repository under your GitHub account.
2. **Clone Your Fork Locally:**
    - Open GitHub Desktop or use Git on the command line.
    - Clone your forked repository by replacing `<your-fork-url>` with your fork's URL:

```bash
git clone <your-fork-url> <new-project-name>
cd <new-project-name>
```

3. **Set Up Upstream Remote:**
    - Connect your fork back to the original template repository so you can pull updates later:

```bash
git remote add upstream https://github.com/<org-name>/project_template.git
```

4. **Working in Databricks:**
    - In Databricks, go to **Repos** in the sidebar.
    - Click **Add Repo**, paste your fork's URL, and click **Create**.
    - This will create a Git-backed folder in your Databricks workspace where you can edit notebooks and scripts directly.

---

### 2. Customizing Your Fork

Once you’ve cloned your fork locally or added it as a repo in Databricks, customize it as follows:

- **Add Your Models:**
Place specific models under `src/pyfiles/models/`.
- **Implement Utility Functions:**
Add or update shared utilities in `src/pyfiles/utils/`.
- **Develop Pipelines:**
Use `notebooks/pipelines/` for experimentation or pipeline development.
- **Organize Your Data:**
Keep your data organized under `data/models/`, following the same structure used in the template.

---

### 3. Keeping Your Fork Updated with Template Changes

To ensure that your fork stays up-to-date with changes made in the original template repository:

1. **Fetch Updates from Upstream:**

```bash
git fetch upstream
```

2. **Merge Changes from Upstream into Your Local Branch:**

```bash
git pull upstream main
```

Resolve any conflicts if they arise and commit the merge.
3. **Push Updates to Your Fork:**

```bash
git push origin main
```


This ensures that you always have access to improvements or bug fixes made in the main template repository.

---

### 4. Contributing Back to the Template Repository

If you make improvements (e.g., new utility functions) that could benefit all teams, contribute them back by creating a pull request:

1. **Create a New Branch for Your Changes:**

```bash
git checkout -b update-utils
```

2. **Commit Your Changes:**

```bash
git add .
git commit -m "Add new utility function for X"
```

3. **Push Your Branch to Your Fork:**

```bash
git push origin update-utils
```

4. **Open a Pull Request:**
    - Go to your fork on GitHub.
    - Click **New Pull Request**, ensuring that:
        - The base repository is the organization’s template (e.g., `Bovi-analytics/project_template_with_fork_function`).
        - The compare branch is your branch (`update-utils`).
    - Provide a clear description of your changes and submit the pull request.

---

### 5. Choosing How You Use Your Fork

When cloning or managing your fork, tools like GitHub Desktop may ask how you plan to use it:

- If most of your work is private but you occasionally contribute back to shared utilities, select **"For my own purposes"**.
- You can still create pull requests targeting the parent project when needed without changing this setting.

---

### Summary of Workflow

1. Fork this repository into your own GitHub account.
2. Clone your fork locally or add it as a repo in Databricks.
3. Work on your project privately in your fork.
4. Keep your fork updated by pulling changes from upstream.
5. Contribute shared improvements back via pull requests.

---

## Why Use Forking?

Forking is preferred over creating independent repositories because:

- It retains a connection to the original template, allowing you to pull updates easily.
- It enables collaboration by allowing contributions (pull requests) back to the main template.
- It ensures consistency across projects while allowing customization for individual needs.
