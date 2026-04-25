# Base template repository

> [!NOTE]
> This template repository is for now experimental.

## Import changes from template repository

Forked repositories can be synchronized via GitHub, but template repositories
don't have this option as it will become a standalone project and has no
permanent link to its parent.

To bring in updates from the template later, you have to manually link them
using git as described below.

### Step 1: Add the template repository as a remote

```bash
git remote add template https://github.com/hspaans/template.git
```

### Step 2: Fetch the template changes

```bash
git fetch template
```

### Step 3: Merge with unrelated histories

```bash
git merge template/master --allow-unrelated-histories
```

### Step 4: Resolve conflicts

1. Open your code editor
2. Look for the `<<<<<<< HEAD` and `>>>>>>> template/master` markers.
3. Choose which changes to keep.
4. Stage and commit:

```bash
git add .
git commit -m "Merged latest updates from template"
git push origin master
```
