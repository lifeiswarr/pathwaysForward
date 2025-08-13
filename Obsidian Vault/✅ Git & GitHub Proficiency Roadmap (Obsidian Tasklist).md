

---
# .[[VANITY]].[[topics to cover]].

## 📦 1. Basics of Version Control
- [ ] Understand what version control is
- [ ] Know the difference between Git and GitHub
- [ ] Install Git and configure (`git config`, username, email)
- [ ] Initialize a Git repository (`git init`)
- [ ] Check repo status (`git status`)
- [ ] Stage files (`git add`)
- [ ] Commit changes (`git commit -m ""`)
- [ ] View commit history (`git log`)
- [ ] Understand .gitignore and how to use it

## 🌳 2. Branching & Merging
- [ ] Create branches (`git branch <branchname>`)
- [ ] Switch between branches (`git checkout`, `git switch`)
- [ ] Merge branches (`git merge`)
- [ ] Understand merge conflicts and resolve them
- [ ] Visualize branches (`git log --oneline --graph`)
- [ ] Delete branches locally (`git branch -d`)

## 🔁 3. Remote Repositories
- [ ] Create a GitHub repo and link it to local Git (`git remote add origin`)
- [ ] Push code to GitHub (`git push`)
- [ ] Pull updates (`git pull`)
- [ ] Clone repos (`git clone`)
- [ ] Understand HTTPS vs SSH authentication
- [ ] Set up SSH key for GitHub access

## 🧪 4. Collaboration & Workflow
- [ ] Fork a repository
- [ ] Make a Pull Request (PR)
- [ ] Review PRs and request changes
- [ ] Use Issues and Discussions for collaboration
- [ ] Sync fork with upstream repository
- [ ] Rebase vs Merge: when and why
- [ ] Squash commits before merging
- [ ] Use GitHub CLI for easier workflows (`gh`)

## 🧹 5. Undo & Fix Mistakes
- [ ] Undo last commit (`git reset --soft`, `--mixed`, `--hard`)
- [ ] Revert a specific commit (`git revert`)
- [ ] Remove files from staging (`git reset HEAD <file>`)
- [ ] Amend a commit (`git commit --amend`)
- [ ] Stash changes (`git stash`, `git stash pop`)
- [ ] Recover deleted branches and commits (`git reflog`)

## 🛠️ 6. Git Internals & Advanced Use
- [ ] Understand the 3-stage architecture (Working Dir → Staging → Repo)
- [ ] Learn how `.git` directory works
- [ ] Cherry-pick commits (`git cherry-pick`)
- [ ] Tagging releases (`git tag`)
- [ ] Use submodules (`git submodule`)
- [ ] Work with Git Hooks (pre-commit, post-commit)
- [ ] Use bisect to find faulty commits (`git bisect`)
- [ ] Understand object model (commits, trees, blobs)

## 📊 7. GitHub Power Features
- [ ] Create and use GitHub Actions for CI/CD
- [ ] Write and use GitHub workflows in `.github/workflows/`
- [ ] Enable branch protection rules
- [ ] Use CODEOWNERS for auto review assignment
- [ ] Create GitHub Pages from repos
- [ ] Use GitHub Projects & Boards (Kanban-style)
- [ ] Create GitHub Packages and Releases
- [ ] Generate changelogs from commits

## 🔐 8. Security & Best Practices
- [ ] Store credentials securely (`git-credential-store`, `manager-core`)
- [ ] Rotate or revoke SSH tokens and PATs (personal access tokens)
- [ ] Use `.gitattributes` for cross-platform consistency
- [ ] Avoid committing secrets (learn `git-secrets`, `truffleHog`)
- [ ] Sign commits with GPG (`git commit -S`)
- [ ] Setup `.npmrc`, `.dockerignore`, `.env` securely with GitHub

## 🧠 9. Real-World Workflows
- [ ] Git Flow (feature, develop, hotfix, release branches)
- [ ] GitHub Flow (trunk-based)
- [ ] Rebase-based feature branching
- [ ] Monorepo vs Polyrepo strategies
- [ ] Use Git for notebooks/data science with DVC

## 🎯 10. Practice & Projects
- [ ] Contribute to an open-source repo
- [ ] Use GitHub with Jupyter notebooks
- [ ] Setup a project board in GitHub
- [ ] Create a release cycle with tags and changelogs
- [ ] Automate testing with GitHub Actions on PR

---

## 🔁 Review Checklist
- [ ] Can you work with multiple branches?
- [ ] Can you resolve conflicts?
- [ ] Can you recover lost code using `reflog` or `stash`?
- [ ] Are you comfortable using both `merge` and `rebase`?
- [ ] Can you collaborate through PRs effectively?
- [ ] Do you understand CI/CD basics via GitHub Actions?

