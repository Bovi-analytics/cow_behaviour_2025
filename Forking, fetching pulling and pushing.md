### **Key Points About Forks and Upstream**

1. **Your Forked Repository (Private Work)**:
    - The forked repo (`cow_behaviour_2025`) is where you will do most of your work.
    - You can treat this as your private project repository, where you add models, experiments, and other project-specific code.
2. **The Template Repository (Shared Utilities)**:
    - The original template repository (`project_template_with_fork_function`) is owned by the organization and serves as a clean, centralized template for all teams.
    - If you improve shared utilities (e.g., `initialize.py`, `inference.py`), you should contribute those changes back to the template by creating a **pull request**.
3. **Upstream Relationship**:
    - Your forked repo maintains a connection to the template repository via the `upstream` remote.
    - This allows you to:
        - Pull updates from the template into your fork.
        - Push changes from your fork to the template via pull requests.

---

### **How to Work with Both Repositories**

Here’s how to manage your workflow:

#### **1. Set Up Remotes**

After cloning your fork locally, ensure you have two remotes configured:

- `origin`: Points to your fork (`cow_behaviour_2025`). This is where you push most of your changes.
- `upstream`: Points to the original template repository (`project_template_with_fork_function`). This is used for pulling updates or contributing back.

Run these commands to verify or set up remotes:

```bash
# Check remotes
git remote -v

# Add upstream if not already set
git remote add upstream https://github.com/Bovi-analytics/project_template_with_fork_function.git
```

---

#### **2. Workflow for Private Work**

For most of your work:

1. Make changes in your fork (`cow_behaviour_2025`).
2. Commit and push changes to `origin` (your fork):

```bash
git add .
git commit -m "Your commit message"
git push origin main
```

3. These changes will stay in your fork and will not affect the template repository.

---

#### **3. Workflow for Contributing Back to the Template**

When you make improvements to utility functions or shared code that should be added to the template:

1. Create a new branch in your fork for these changes:

```bash
git checkout -b update-utils
```

2. Make your changes and commit them.
3. Push the branch to your fork:

```bash
git push origin update-utils
```

4. Open a pull request from this branch in your fork (`cow_behaviour_2025`) to the `main` branch of the template repository (`project_template_with_fork_function`).

GitHub will automatically detect that this is a pull request targeting the upstream repository.

---

#### **4. Keeping Your Fork Updated**

When updates are made in the template repository, you’ll want to pull them into your fork:

1. Fetch updates from `upstream`:

```bash
git fetch upstream
```

2. Merge updates into your local branch (e.g., `main`):

```bash
git merge upstream/main
```

3. Push merged changes back to your fork:

```bash
git push origin main
```


This ensures that your fork stays up-to-date with improvements made in the template repository.
