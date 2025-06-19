🔧 GitHub Authentication and Repository Setup

This repository demonstrates how to set up GitHub authentication using a **Personal Access Token (PAT)** and perform basic Git operations from a local development environment.

📌 Steps Followed

✅ 1. Generated a Personal Access Token (PAT)
- Go to [GitHub Token Settings](https://github.com/settings/tokens)
- Created a **Classic Token**
- Selected scopes:
  - `repo` (Full control of private and public repositories)
- Set expiration as needed
- Copied and saved the token securely

✅ 2. Configured Git to Store Credentials
Ran this command to store the token permanently:
```bash
git config --global credential.helper store
````

🔒 This stores the token in plaintext inside `~/.git-credentials`

✅ 3. Used the Token for Git Authentication

When prompted by Git:

* **Username**: Abhishek7439
* **Password**: \[Paste the GitHub token instead of GitHub password]

Git then saved these credentials automatically and authenticated all future commands without asking again.

✅ 4. Pushed Code to GitHub

Used the following commands:

```bash
git add .
git commit -m "Initial commit"
git push origin master
```

✅ 5. Managed Branches

* Local branch was named `master`
* GitHub default branch was `main`
* To sync:

```bash
git branch -m master main
git push -u origin main
git push origin --delete master  # (optional)
```

---

📂 Final Notes

* Token authentication is now the default and required for HTTPS Git operations.
* You should avoid using GitHub passwords directly — **use tokens or SSH keys**.
* To improve security, consider using `git-credential-manager` or SSH authentication.

```

