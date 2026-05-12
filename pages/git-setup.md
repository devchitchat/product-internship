---
title: Git Setup for Interns
---

# Git Setup for Interns

Follow these steps to get access to the repo so you can submit your feedback and update documents.

## 1. Create a GitHub Account

If you don't already have one, sign up at [github.com](https://github.com).

## 2. Get Access to the Repo

Send your GitHub username to your manager so you can be added as a collaborator on [devchitchat/product-internship](https://github.com/devchitchat/product-internship).

## 3. Install Git

Check if you already have it:

```sh
git --version
```

If not, install it via Homebrew on Mac (recommended) or from [git-scm.com](https://git-scm.com).

**Installing Homebrew**

[Homebrew](https://brew.sh) is a package manager for Mac that makes it easy to install developer tools. To install it, open Terminal and run:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## 4. Install VS Code

[Visual Studio Code](https://code.visualstudio.com) is a free code editor that works great for editing markdown files and code. Download and install it from the VS Code website.

Once installed, you can open any file from the terminal with:

```sh
code pages/index.md
```

## 5. Configure Git with Your Identity

```sh
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

## 6. Clone the Repo

In a terminal, create a folder to store repos.

```sh
mkdir ~/src
```

Then `cd src`

```sh
git clone https://github.com/devchitchat/product-internship.git
cd product-internship
```

## 7. Make Your Changes

Edit files using any text editor. For example, to update your notes in the internship playbook:

```sh
# open the file in your editor, e.g.:
code pages/index.md
```

## 8. Commit and Push Your Changes

```sh
git add pages/index.md
git commit -m "Add feedback: week 1 notes"
git push origin main
```

## 9. Use a Branch for Your Updates (Recommended)

Rather than pushing directly to `main`, create a branch and open a pull request so your manager can review changes before they go live:

```sh
git checkout -b intern/your-name-feedback
# ... make your edits ...
git add pages/index.md
git commit -m "Week 1 feedback and notes"
git push origin intern/your-name-feedback
```

Then open a pull request on GitHub from your branch to `main`. Your manager will review and merge it.

---

The typical loop once you're set up: **edit a file → `git add` → `git commit` → `git push` → open a pull request**.
