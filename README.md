# Fast Forward Merge with Auto-Approval (GitHub Actions)

This project automates the **approval** and **fast-forward merging** of pull requests using GitHub Actions and a Personal Access Token (PAT).

---

## 📦 Features

- ✅ Automatically approves pull requests (PRs) using a GitHub token
- ✅ Fast-forwards the base branch to the PR head (no merge commits)
- ✅ Triggered on `pull_request` events
- ✅ Works with private or public repositories

---

## 🛠️ Local Setup

### 1. Clone the Repository

```bash
git clone https://github.com/jayendrapawar/fast-forward-merge.git
cd fast-forward-merge
```

---

### 2. Generate a GitHub Personal Access Token (Classic)

> This token will be used to approve and merge PRs through the GitHub API.

1. Go to [https://github.com/settings/tokens?type=classic](https://github.com/settings/tokens?type=classic)
2. Click **"Generate new token (classic)"**
3. Select the following scopes:
   - ✅ `repo` — Full control of private and public repositories
   - ✅ `workflow` — Access to GitHub Actions
4. Generate the token and **copy it immediately**

---

### 3. Add the PAT to GitHub Secrets

1. Go to your GitHub repo → **Settings** → **Secrets and variables** → **Actions**
2. Click **"New repository secret"**
3. Add:
   - **Name**: `PERSONAL_ACCESS_TOKEN`
   - **Value**: *Paste your token here*
4. Save it


## ✅ Example GitHub Actions Run

Check out a successful run for reference:  
🔗 [GitHub Actions #14281515297](https://github.com/jayendrapawar/fast-forward-merge/actions/runs/14281515297)

---

## ⚠️ Notes

- GitHub does **not allow a user to approve their own pull request**.
- Use a PAT from a different GitHub account (e.g. bot or reviewer) to enable approval.
- Only works if the PR can be fast-forwarded cleanly (no merge conflicts).

---

## 📄 License

MIT License © [Jayendra Pawar](https://github.com/jayendrapawar)
