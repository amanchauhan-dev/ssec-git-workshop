# Activity 3 — Merge Conflict Simulation (Using Pull Request)

## Objective

Learn how to:

- Create a merge conflict intentionally
- Understand why conflicts happen
- Resolve conflicts using GitHub
- Update local repository after conflict resolution

This simulates **real team conflicts**.

# Starting Condition

You should already have:

- Repository from Activity 1
- `index.html` file
- `about.html` file (from Activity 2)
- Repository pushed to GitHub
- Working `main` branch

---

# Step 1 — Create First Feature Branch

Create a branch:

```bash
git switch -c feature-header
```

Open:

```text
index.html
```

Modify file:

```html
<h1>Welcome to My Website</h1>
<p>This is the header section.</p>
```

Save file.

---

# Step 2 — Stage and Commit Changes

```bash
git add index.html

git commit -m "feat: update header text"
```

Push branch:

```bash
git push -u origin feature-header
```

Now go to GitHub.

Create Pull Request:

**feature-header → main**

But **DO NOT MERGE YET**.

Leave it open.

---

# Step 3 — Create Second Branch From main

Switch to main:

```bash
git switch main

git pull origin main
```

Create another branch:

```bash
git switch -c feature-footer
```

Open:

```text
index.html
```

Modify the **same line differently**:

```html
<h1>My Portfolio Website</h1>
<p>This is the footer section.</p>
```

Save file.

---

# Step 4 — Stage and Commit Second Change

```bash
git add index.html

git commit -m "feat: update footer text"
```

Push second branch:

```bash
git push -u origin feature-footer
```

---

# Step 5 — Merge First Pull Request

Go to GitHub.

Open PR:

```text
feature-header → main
```

Click:

**Merge Pull Request**

Now `main` contains header changes.

---

# Step 6 — Create Conflict (Second PR)

Now open PR:

```text
feature-footer → main
```

GitHub will show:

```text
This branch has conflicts that must be resolved
```

Conflict created successfully.

---

# Step 7 — Resolve Conflict on GitHub ⭐

Click:

**Resolve conflicts**

You will see something like:

```text
<<<<<<< HEAD
<h1>Welcome to My Website</h1>
=======
<h1>My Portfolio Website</h1>
>>>>>>> feature-footer
```

Fix manually:

Example:

```html
<h1>My Portfolio Website</h1>
<p>Header and Footer Updated</p>
```

Remove:

```text
<<<<<<<
=======
>>>>>>>
```

Click:

**Mark as resolved**

Then:

**Commit merge**

---

# Step 8 — Merge Second Pull Request

After resolving conflict:

Click:

**Merge Pull Request**

Now both changes are merged.

---

# Step 9 — Pull Updated Code Locally

Update your local repository:

```bash
git switch main

git pull origin main
```

Check file:

```bash
cat index.html
```

You should see final merged content.

---

# Final Workflow Summary

Students perform:

```bash
git switch -c feature-header
# edit index.html
git add index.html
git commit -m "feat: update header"
git push -u origin feature-header

# Create PR but don't merge

git switch main
git pull origin main

git switch -c feature-footer
# edit same lines
git add index.html
git commit -m "feat: update footer"
git push -u origin feature-footer

# Merge first PR
# Resolve conflict in second PR
# Merge second PR

git switch main
git pull origin main
```

---

# What Students Learn in This Activity

This teaches:

- Why merge conflicts happen
- How to identify conflicts
- GitHub conflict UI
- Conflict resolution
- Pull request conflict handling
- Updating local repository after merge

This is a **core professional Git skill**.
