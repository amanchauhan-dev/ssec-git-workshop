# Contribution Guide

This activity is designed to practice the full GitHub workflow including fork, branch, merge, and pull request.

---

# Final Activity — Add Your Introduction

Each participant must create their own Markdown file and write a short introduction.

## File Location

Create your file inside:

```
/participants/your-name.md
```

Example:

```
/participants/amanchauhan-dev.md
```

Use lowercase letters and hyphens instead of spaces.

Examples:

Rahul Patel → rahul-patel.md
Neha Sharma → neha-sharma.md

---

# What to Write in Your File

Write a short introduction using Markdown.

Example:

```
# Your Name

## Introduction

- Name: Your Full Name
- Branch: Your Department
- Year: Your Year
- Interests: Coding, Web Development, AI
- GitHub Username: your-username

## About Me

Write 2–4 lines about yourself and your interests.
```

---

# Contribution Workflow

Follow these steps carefully.

---

# Step 1 — Fork the Repository

Click the **Fork** button on GitHub.

This creates your own copy of the repository.

---

# Step 2 — Clone Your Fork

Copy your fork URL and run:

```
git clone https://github.com/your-username/repository-name.git
cd repository-name
```

---

# Step 3 — Create a Branch Using Your Name

Create a new branch:

```
git checkout -b your-name
```

Example:

```
git checkout -b amanchauhan-dev
```

---

# Step 4 — Create Your File

Create:

/participants/your-name.md

Write your introduction inside it.

---

# Step 5 — Stage and Commit

```
git add participants/your-name.md
git commit -m "Add participant: your-name"
```

---

# Step 6 — Push Your Branch to Your Fork

```
git push origin your-name
```

Your branch is now available in your fork.

---

# Step 7 — Merge Your Branch into Main (in Your Fork)

Go to your fork on GitHub.

Create a Pull Request from:

your-name → main (inside your fork)

Then **merge the Pull Request in your fork**.

After merging, your changes will be in:

your-fork/main

---

# Step 8 — Create Pull Request to Upstream Repository

Now create a Pull Request from:

your-fork/main → upstream/main

This sends your contribution to the original repository for review.

---

# Important Rules

- Create only ONE file
- Do NOT edit other participant files
- Use your own name for branch and file
- Follow the correct folder path
- Keep content appropriate

---

# After Submission

Once your Pull Request to the upstream repository is reviewed and merged, your contribution becomes part of the main project.

This completes the GitHub contribution activity.
