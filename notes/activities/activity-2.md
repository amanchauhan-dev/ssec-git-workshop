# Activity 2 — Add New Page Using Branch (Push & Merge on GitHub)

## Objective

Learn how to:

- Create a feature branch
- Add a new page
- Push branch to GitHub
- Create a Pull Request
- Merge on GitHub

This follows **real industry workflow**.

---

# Starting Condition

Students must have:

- Completed Activity 1
- Repository exists on GitHub
- `main` branch pushed
- `index.html` already exists

---

# Step 1 — Create a New Branch

Create feature branch.

```bash
git switch -c feature-about
```

Check branch:

```bash
git branch
```

Expected:

```
main
* feature-about
```

---

# Step 2 — Create New Page

Create new file:

```bash
touch about.html
```

Add content inside `about.html`:

```html
<h1>About Page</h1>
<p>This page was created using a Git branch.</p>
```

Save file.

---

# Step 3 — Stage the File

```bash
git add about.html
```

Verify:

```bash
git status
```

Expected:

```
new file: about.html
```

---

# Step 4 — Commit the Changes

```bash
git commit -m "feat: add about page"
```

Check:

```bash
git log --oneline
```

---

# Step 5 — Push Branch to GitHub ⭐

Push new branch.

```bash
git push -u origin feature-about
```

Now go to **GitHub repository page**.

You will see:

**"Compare & Pull Request" button**

---

# Step 6 — Create Pull Request on GitHub ⭐

On GitHub:

1. Click **Compare & Pull Request**
2. Title:

```
feat: add about page
```

3. Description:

```
This pull request adds an about page to the project.
```

4. Click:

**Create Pull Request**

---

# Step 7 — Merge Pull Request on GitHub ⭐

On GitHub:

1. Click **Merge Pull Request**
2. Click **Confirm Merge**

Now the branch is merged into `main`.

This demonstrates **real GitHub workflow**.

---

# Step 8 — Pull Changes Locally

Update local repository.

```bash
git switch main

git pull origin main
```

Now check:

```bash
ls
```

Expected:

```
index.html
about.html
```

File is now available locally.

---

# Step 9 — Delete Feature Branch (Cleanup)

Delete local branch:

```bash
git branch -d feature-about
```

Delete remote branch (optional):

```bash
git push origin --delete feature-about
```

---

# Final Workflow Summary

Students complete:

```bash
git switch -c feature-about
touch about.html
git add about.html
git commit -m "feat: add about page"
git push -u origin feature-about

# Create Pull Request on GitHub
# Merge on GitHub

git switch main
git pull origin main
git branch -d feature-about
```

---

# What Students Learn in This Activity

This activity teaches:

- Feature branching
- `git push` new branch
- Pull Requests
- GitHub merging
- `git pull` updates
- Branch cleanup
