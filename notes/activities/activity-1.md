# Activity 1 — Create, Stage, Commit, Rename Branch, Push

## Objective

Learn the complete beginner workflow:

**Create Repo → Stage → Commit → Rename Branch → Push**

You will:

- Create a Git repository
- Add and commit a file
- Rename branch to `main`
- Push project to GitHub

---

# Step 1 — Create Project Folder

```bash
mkdir my-first-repo
cd my-first-repo
```

---

# Step 2 — Initialize Git Repository

```bash
git init
```

Check status:

```bash
git status
```

---

# Step 3 — Create a File

```bash
touch index.html
```

Add content inside `index.html`:

```html
<h1>Hello Git!</h1>
<p>This is my first Git project.</p>
```

---

# Step 4 — Stage the File

```bash
git add index.html
```

Verify:

```bash
git status
```

---

# Step 5 — Commit the File

```bash
git commit -m "feat: add index.html homepage"
```

Check history:

```bash
git log --oneline
```

---

# Step 6 — Rename Default Branch to main

This step ensures standard naming.

```bash
git branch -M main
```

Now check:

```bash
git branch
```

Expected:

```bash
* main
```

---

# Step 7 — Create Repository on GitHub

Go to:

[https://github.com](https://github.com)

Then:

1. Click **New Repository**
2. Name:

```
my-first-repo
```

3. Do NOT add README
4. Click **Create Repository**

---

# Step 8 — Connect Local Repo to GitHub

```bash
git remote add origin https://github.com/USERNAME/my-first-repo.git
```

Verify:

```bash
git remote -v
```

---

# Step 9 — Push Code to GitHub

```bash
git push -u origin main
```

This uploads your project.

Refresh GitHub page — you should see:

```
index.html
```

---

# Final Workflow Summary

Students complete:

```bash
git init
git add index.html
git commit -m "feat: add index.html homepage"
git branch -M main
git remote add origin <repo-url>
git push -u origin main
```
