# Assignment 1.5 — GitHub Essentials II

## 1. Objective

The objective of this assignment is to upload a local project to GitHub, connect a local Git repository to a remote repository, push files to GitHub, and verify the commit history.

## 2. Introduction

GitHub is an online platform used to store, manage, and share code. It works with Git, a version control system that tracks changes in project files. A local repository stores project files and commit history on a computer, while a remote repository stores the project online. The `git push` command uploads local commits to the remote repository.

## 3. Creating a GitHub Account

1. Open [GitHub](https://github.com/).
2. Create a new account or sign in to an existing account.
3. Verify your email address if required.

## 4. Creating a New Public Repository

1. Sign in to GitHub.
2. Click the **+** icon and select **New repository**.
3. Enter the repository name: `web-development-practice`.
4. Select **Public**.
5. Leave the options for adding a README, `.gitignore`, or license unchecked because the local project already exists.
6. Click **Create repository**.

A public repository allows other people to view your project.

## 5. Connecting the Local Repository to GitHub

Open the terminal inside your existing `web-development-practice` project folder.

Check the repository status:

```bash
git status
```

Set the branch name to `main`:

```bash
git branch -M main
```

Connect the local repository to your GitHub repository:

```bash
git remote add origin https://github.com/YOUR-USERNAME/web-development-practice.git
```

Replace `YOUR-USERNAME` with your actual GitHub username.

Verify the remote connection:

```bash
git remote -v
```

The output should display your GitHub repository URL for fetching and pushing.

**Note:** If the `origin` remote already exists, use `git remote set-url origin https://github.com/YOUR-USERNAME/web-development-practice.git` instead of adding it again.

## 6. Uploading the Local Project to GitHub

Upload the existing commits and project files:

```bash
git push -u origin main
```

This command pushes the local commits to GitHub and sets `origin/main` as the upstream branch.

If GitHub asks you to authenticate, complete the sign-in or authorization process.

After the command succeeds, refresh your GitHub repository page. Your project files should appear online.

## 7. Creating a New File for the Second Push

Create a new file named `github-upload-demo.html` in the project folder.

On Windows PowerShell, run:

```powershell
New-Item -ItemType File -Path github-upload-demo.html
```

Open the file:

```powershell
notepad github-upload-demo.html
```

Add the following HTML code and save the file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub Upload Demo</title>
</head>
<body>
    <h1>My GitHub Project</h1>
    <p>This file demonstrates my second push to GitHub.</p>
</body>
</html>
```

## 8. Creating the Second Commit and Pushing It

Check the status of the repository:

```bash
git status
```

Stage the new file:

```bash
git add github-upload-demo.html
```

Create the second commit:

```bash
git commit -m "Add GitHub upload demo page"
```

Push the new commit to GitHub:

```bash
git push
```

The new file and its commit should now be available in your remote repository.

## 9. Verifying the Commit History

To view the local commit history, run:

```bash
git log --oneline
```

To verify the commits on GitHub:

1. Open your public repository.
2. Click the commit history link, usually displayed as **Commits**.
3. Confirm that the earlier project commits and the new commit named `Add GitHub upload demo page` are visible.
4. Open the repository's **Code** tab and verify that `github-upload-demo.html` is present.

The commit history should include the earlier commits from Assignment 1.4 and the new commit created in this assignment.

## 10. Expected Project Structure

```text
web-development-practice/
│
├── index.html
├── style.css
├── README.md
├── github-upload-demo.html
│
├── week-1/
│   └── index.html
│
├── week-2/
│   └── index.html
│
└── week-3/
    └── index.html
```

The `.git` directory also exists locally, although it is hidden by default and is not uploaded as a normal project folder.

## 11. Submission — Public GitHub Repository Link

After successfully uploading your project, copy your public repository URL.

**Repository URL format:**

`https://github.com/YOUR-USERNAME/web-development-practice`

Replace `YOUR-USERNAME` with your actual GitHub username and submit your real repository link.

## 12. Conclusion

In this assignment, I learned how to create a public GitHub repository, connect it to a local Git repository, upload project files using `git push`, create and push a second commit, and verify the commit history on GitHub. These skills are essential for collaborating with other developers and managing projects online.
