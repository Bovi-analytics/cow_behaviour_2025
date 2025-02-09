Project Template
Overview
This repository serves as a template for organizing machine learning projects across the company. It provides a standardized directory structure to ensure consistency, modularity, and collaboration across teams.
The template includes placeholders for:
Python scripts (.py) for core functionalities.
Jupyter notebooks (.ipynb) for pipelines and experimentation.
Organized directories for data, models, and utilities.
Teams can use this template as a starting point for their projects and customize it according to their specific needs.

Directory Structure

![Dir tree](misc/readme_data/dir_tree.png?raw=true "Dir tree")

Usage Instructions
1. Cloning the Template Repository
To start a new project using this template:

bash
git clone <template-repo-url> <new-project-name>
cd <new-project-name>

2. Customizing the Template
Add your specific models under src/pyfiles/models/.
Implement utility functions in src/pyfiles/utils/.
Use notebooks/pipelines/ for experimentation or pipeline development.
Organize your data in data/models/.

3. Keeping Utils and Abstract Classes Updated
To ensure shared files like utils and abstract classes (initialize.py, inference.py, etc.) stay updated:
Pull updates from the template repository:

bash
git pull upstream main

Resolve conflicts if necessary and merge changes into your project.

Contributing Back to the Template
If you make improvements to shared files that could benefit all teams, submit a pull request to the template repository with a description of your changes.