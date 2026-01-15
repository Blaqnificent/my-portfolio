# DevOps Git and GitHub Lab Report


## Project Title
My DevOps Portfolio Git and GitHub Workflow Lab

## Objective
The objective of this lab is to demonstrate practical understanding of Git version control, branching, merge conflict resolution, and remote collaboration using GitHub.

---

## 1. Setting Up the Local Repository

### Description
A local Git repository was created and initialized. A README file was added and committed to establish the initial structure of the project.

### Commands Used
```bash
mkdir my-portfolio && cd my-portfolio
git init
echo "# My DevOps Portfolio" > README.md
git add README.md
git commit -m "Initial commit Add README"
git status
git log --oneline
```

### Checkpoint
- Repository contains at least one commit
- Git status shows a clean working tree

### Screenshot Placeholder
- ![Screenshot showing `git log --oneline` with the initial commit](checkpoint-1)

---

## 2. Working with Branches for Feature Development

### Feature Branch Creation
A feature branch was created to add personal information without affecting the main branch.

### Commands Used
```bash
git switch -c feature/about-me
echo "Skills Linux Bash Scripting" > about.md
git add about.md
git commit -m "Add about me section"
```

### Updating README With Link
The README file was updated to include a link to the about page.

```bash
git add README.md
git commit -m "Update README with link to about section"
```

### Merging the Feature Branch
```bash
git checkout main
git merge feature/about-me
git log --graph --oneline
```

### Checkpoint
- Feature branch successfully merged into main
- No merge conflicts occurred

### Screenshot Placeholder
- ![Screenshot of `git log --graph --oneline` showing the merge](checkpoint-2)

---

## 3. Simulating and Resolving Merge Conflicts

### Creating a New Feature Branch
```bash
git checkout -b feature/projects
```

### Editing README on Feature Branch
```md
## Projects DevOps Lab 1
```

```bash
git add README.md
git commit -m "Add projects section"
```

### Creating a Conflict on Main Branch
```bash
git checkout main
```

```md
## Projects Git Basics
```

```bash
git add README.md
git commit -m "Add projects on main"
```

### Triggering the Merge Conflict
```bash
git merge feature/projects
```

### Resolving the Conflict
The conflict markers were removed and both project sections were combined.

```bash
git add README.md
git commit -m "Resolve merge conflict in README"
git status
```

### Checkpoint
- Merge conflict detected and resolved successfully
- Repository returned to a clean state

### Screenshot Placeholders
- ![Screenshot of README.md showing resolved conflict](checkpoint-3.1)
- ![Screenshot of commit message resolving the merge conflict](checkpoint-3.2)


---

## 4. Remote Collaboration With GitHub

### Creating and Connecting to GitHub Repository
```bash
git remote add origin https://github.com/Blaqnificent/my-portfolio.git
git push -u origin main
```

### Simulating Collaboration Using Pull Requests
```bash
git checkout -b feature/enhancement
echo "DevOps Skills Git Docker" > skills.md
git add skills.md
git commit -m "Add skills file"
git push origin feature/enhancement
```

### Pull Request Process
- Pull request created on GitHub
- Pull request reviewed and merged into main

### Syncing Local Repository
```bash
git checkout main
git pull
```

### Checkpoint
- Feature branch pushed to GitHub
- Pull request created and merged successfully
- Local repository synchronized with remote

### Screenshot Placeholders
- ![Screenshot of GitHub pull request creation page](checkpoint-4.1)
- ![Screenshot of merged pull request on GitHub](checkpoint-4.2)

---

## Conclusion
This lab demonstrated Git repository setup, branching, merge conflict resolution, and GitHub collaboration using pull requests. These workflows are essential for effective DevOps and software development practices.

