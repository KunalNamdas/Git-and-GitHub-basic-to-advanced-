# **Comprehensive Guide to Git & GitHub: From Basics to Advanced**

---

## **Chapter 1: Introduction to Git**

### **What is Git?**
Git is a distributed version control system that tracks changes in files and allows multiple people to work on the same project simultaneously. It was created by Linus Torvalds in 2005.

### **Why Use Git?**
- **Version Control**: Easily track and revert changes.
- **Collaboration**: Multiple contributors can work simultaneously.
- **Branching and Merging**: Safely experiment with features without affecting the main codebase.
  
---

## **Chapter 2: Setting Up Git**

### **Installing Git**
1. **On Windows**:
   - Download from [Git’s website](https://git-scm.com).
   - Install using the setup wizard.

2. **On macOS**:
   ```bash
   brew install git
   ```

3. **On Linux**:
   ```bash
   sudo apt update
   sudo apt install git
   ```

### **Configuring Git**
After installation, set up your name and email:
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### **Checking Configuration**
```bash
git config --list
```

---

## **Chapter 3: Basic Git Concepts**

### **Repositories**
A Git repository (or “repo”) is a directory where Git stores project history. There are two types:
1. **Local Repository**: Located on your machine.
2. **Remote Repository**: Hosted on a server, such as GitHub.

### **Commits**
A commit is a snapshot of changes made to the files in a repository.

### **Branches**
Branches allow you to create independent lines of development. The default branch is usually called `main` or `master`.

---

## **Chapter 4: Working with Git**

### **Initializing a Repository**
```bash
git init
```

### **Staging and Committing Changes**
1. **Add files to the staging area**:
   ```bash
   git add filename
   ```
   or add all files:
   ```bash
   git add .
   ```

2. **Commit changes**:
   ```bash
   git commit -m "Describe your changes"
   ```

### **Viewing History**
```bash
git log
```

---

## **Chapter 5: Branching in Git**

### **Creating a New Branch**
```bash
git branch new-feature
```

### **Switching to a Branch**
```bash
git checkout new-feature
```

### **Creating and Switching to a Branch Simultaneously**
```bash
git checkout -b new-feature
```

### **Merging Branches**
1. Switch to the branch you want to merge into (usually `main`):
   ```bash
   git checkout main
   ```
2. Merge the other branch:
   ```bash
   git merge new-feature
   ```

### **Deleting a Branch**
```bash
git branch -d new-feature
```

---

## **Chapter 6: GitHub Basics**

### **What is GitHub?**
GitHub is a web-based platform that hosts Git repositories, enabling collaboration and sharing. It offers additional features like issue tracking, code reviews, and pull requests.

### **Creating a GitHub Account**
1. Go to [GitHub’s website](https://github.com) and sign up.

### **Creating a Repository on GitHub**
1. Click on the **New** button in the GitHub dashboard.
2. Name your repository and choose between **Public** or **Private** visibility.
3. Optionally, initialize with a **README** and a **.gitignore** file.

---

## **Chapter 7: Connecting Git and GitHub**

### **Adding a Remote Repository**
```bash
git remote add origin https://github.com/username/repository.git
```

### **Pushing Changes to GitHub**
```bash
git push -u origin main
```

### **Cloning a Repository from GitHub**
```bash
git clone https://github.com/username/repository.git
```

---

## **Chapter 8: Working with Pull Requests**

### **What is a Pull Request?**
A pull request is a request to merge changes from one branch (or fork) into another branch, often used in collaborative projects.

### **Creating a Pull Request**
1. Push your branch to GitHub.
2. Go to the repository on GitHub.
3. Select **Compare & pull request** and submit your request.

### **Reviewing and Merging Pull Requests**
- Reviewers can leave comments, approve, or request changes before merging.

---

## **Chapter 9: Collaboration on GitHub**

### **Forking a Repository**
1. Click on **Fork** on the repository page.
2. This creates a copy of the repository under your GitHub account.

### **Contributing to a Repository**
1. Fork the repo and clone it locally.
2. Make your changes, commit, and push to your forked repo.
3. Open a pull request from your fork to the original repo.

---

## **Chapter 10: Advanced Git Concepts**

### **Rebasing**
Rebasing rewrites commit history to make it linear and cleaner.

1. Start a rebase:
   ```bash
   git rebase branch-name
   ```

2. Resolve conflicts if any arise, then:
   ```bash
   git rebase --continue
   ```

### **Cherry-Picking**
Apply specific commits from one branch to another.
```bash
git cherry-pick commit-id
```

---

## **Chapter 11: Resolving Conflicts**

### **What are Conflicts?**
Conflicts occur when two branches have changes in the same file lines. Git can’t automatically merge these.

### **Resolving Conflicts**
1. Open the file and manually edit the conflicting sections.
2. Stage the resolved files:
   ```bash
   git add filename
   ```
3. Complete the merge:
   ```bash
   git commit
   ```

---

## **Chapter 12: Git Commands Reference**

### **Essential Commands**
- **git status**: Check the current status of your working directory.
- **git diff**: View changes in files.
- **git fetch**: Fetch changes from a remote repository.
- **git pull**: Fetch and merge changes from a remote repository.

### **Advanced Commands**
- **git reset**: Unstage or undo changes.
- **git stash**: Temporarily save changes.
- **git tag**: Mark specific commits as milestones (releases).

---

## **Chapter 13: Git Workflows**

### **Popular Workflows**
1. **Git Flow**: Divides work between feature, release, and hotfix branches.
2. **GitHub Flow**: Simple flow for short-lived branches.
3. **Forking Workflow**: Common in open-source projects, using forks and pull requests.

---

## **Chapter 14: GitHub Actions**

### **What are GitHub Actions?**
GitHub Actions is a CI/CD tool for automating workflows, such as running tests or deploying code.

### **Creating a GitHub Action**
1. Create a `.github/workflows` directory in your repository.
2. Add a YAML file with workflow definitions.
3. Example Workflow:
   ```yaml
   name: CI
   on: [push]
   jobs:
     build:
       runs-on: ubuntu-latest
       steps:
       - uses: actions/checkout@v2
       - name: Run a one-line script
         run: echo Hello, world!
   ```

---

## **Chapter 15: GitHub Pages**

### **What is GitHub Pages?**
GitHub Pages allows you to host static websites directly from a GitHub repository.

### **Creating a GitHub Pages Site**
1. Go to **Settings** > **Pages** in your repository.
2. Choose the branch and folder to deploy from.
3. Access your site at `https://username.github.io/repository`.

---

## **Chapter 16: Securing Your GitHub Repository**

### **Tips for Security**:
1. **Use SSH Keys**: Set up SSH keys for secure authentication.
2. **Enable Two-Factor Authentication (2FA)**.
3. **Use Secret Scanning**: GitHub alerts you if it detects sensitive information in your code.

---

## **Conclusion**

Git and GitHub are essential tools in modern software development, enabling powerful version control, collaboration, and automation capabilities.

**Authored by Kunal Namdas**
