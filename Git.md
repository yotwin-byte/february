# Git

---

# 1. What is Git?

Git is a distributed version control system used to track changes in source code and manage collaboration across teams. It maintains the complete history of a project, supports isolated feature development through branches, and enables stable CI/CD workflows.

It is used widely across platforms such as GitHub, GitLab, Bitbucket, and AWS CodeCommit. Git helps developers work independently, merge changes safely, and roll back to stable versions when needed.

> Gitは、ソースコードの変更を追跡し、チーム間の共同作業を管理するために使用される分散型バージョン管理システムです。プロジェクトの完全な履歴を維持し、ブランチによる独立した機能開発をサポートし、安定したCI/CDワークフローを実現します。
Gitは、GitHub、GitLab、Bitbucket、AWS CodeCommitなどのプラットフォームで広く利用されています。Gitは開発者が独立して作業し、変更を安全にマージし、必要に応じて安定したバージョンにロールバックすることを可能にします。
> 

---

# 2. Essential Git Terminology

| Term | Meaning | 概要 |
| --- | --- | --- |
| Repository | Contains the full project along with history and version tracking | プロジェクト全体と履歴およびバージョン管理を含みます |
| Commit | A snapshot of staged changes at a given point in time | 特定の時点における段階的変更のスナップショット |
| Branch | An isolated line of development for features or fixes | 機能や修正のための独立した開発ライン |
| Merge | Combines changes from one branch into another | あるブランチの変更を別のブランチに統合する |
| Clone | Downloads a remote repository to a local machine | リモートリポジトリをローカルマシンにダウンロードする |
| Pull | Downloads and integrates changes from remote | リモートからの変更をダウンロードし統合する |
| Push | Uploads local commits to remote | ローカルのコミットをリモートにアップロードする |
| HEAD | Pointer to the current branch or commit | 現在のブランチまたはコミットへのポインタ |

Repositories organize code, commits capture incremental work, and branches allow parallel development, which is core to DevOps and CI/CD workflows.

> リポジトリはコードを整理し、コミットは増分的な作業を記録し、ブランチは並行開発を可能にします。これらはDevOpsおよびCI/CDワークフローの中核をなすものです。
> 

---

# GIT COMMANDS

---

# 1. git init

**Description**

Initializes a new Git repository in the current directory. Creates the `.git` folder that stores version history.

**Command**

```
git init

```

---

# 2. git status

**Description**

Displays the working directory status, including modified, staged, and untracked files. Used frequently to review what has changed before committing.

**Command**

```
git status

```

---

# 3. git add

**Description**

Stages files for the next commit. Allows selective or complete staging of changes.

**Commands**

```
git add file.txt
git add .

```

---

# 4. git commit

**Description**

Saves staged changes as a new commit with a message describing the update.

**Command**

```
git commit -m "message"

```

---

# 5. git remote add

**Description**

Links a local repository to a remote repository such as GitHub.

**Command**

```
git remote add origin <repo-url>

```

---

# 6. git push

**Description**

Uploads local commits to the remote repository. The first push sets the upstream reference.

**Commands**

```
git push -u origin main
git push

```

---

# 7. git pull

**Description**

Fetches and automatically merges remote updates into the current branch.

**Command**

```
git pull

```

---

# 8. git fetch

**Description**

Retrieves remote changes without merging. Useful for reviewing updates before integrating them.

**Command**

```
git fetch

```

---

# 9. git merge

**Description**

Merges another branch’s changes into the current one.

**Command**

```
git merge feature/login

```

---

# 10. git branch

**Description**

Lists branches or creates a new one for isolated development.

**Commands**

```
git branch
git branch new-feature

```

---

# 11. git checkout / git switch

**Description**

Switches branches or creates a new branch and switches in one step. `git switch` is the modern method.

**Commands**

```
git checkout branch
git checkout -b new-branch
git switch branch

```

---

# 12. git restore

**Description**

Restores a file to its last committed version, discarding local modifications.

**Command**

```
git restore file.txt

```

---

# 13. git reset

**Description**

Moves the current branch pointer to a previous commit.

- `-hard` resets files and history
- `-soft` keeps changes in staging

**Commands**

```
git reset --hard <commit>
git reset --soft <commit>

```

---

# 14. git revert

**Description**

Creates a new commit that undoes a previous commit. Safe for shared branches because it preserves history.

**Command**

```
git revert <commit>

```

---

# 15. git stash

**Description**

Temporarily saves uncommitted changes so you can switch branches without losing work.

**Commands**

```
git stash
git stash apply
git stash list

```

---

# 16. git log

**Description**

Displays the commit history with timestamps, authors, and messages. Useful for debugging and audits.

**Commands**

```
git log
git log --oneline --graph

```

---

# 17. git show

**Description**

Displays details about a specific commit, including changes made.

**Command**

```
git show <commit>

```

---

# 18. git diff

**Description**

Shows differences between files before committing. Helps verify changes line-by-line.

**Commands**

```
git diff
git diff --staged

```

---

# 19. git tag

**Description**

Creates tags to mark release versions or specific commit references.

**Commands**

```
git tag v1.0
git push origin --tags

```

---

# 20. git rebase

**Description**

Rewrites commit history to create a clean, linear sequence of commits.

**Command**

```
git rebase main

```

---

# 21. git cherry-pick

**Description**

Applies a specific commit onto the current branch. Useful for migrating isolated fixes.

**Command**

```
git cherry-pick <commit>

```

---

# 22. git bisect

**Description**

Finds the commit that introduced a bug through binary search.

**Commands**

```
git bisect start
git bisect bad
git bisect good <commit>

```

---

# 23. git rm

**Description**

Removes a file from the working directory and the Git index.

**Command**

```
git rm file.txt

```

---

# 24. git mv

**Description**

Renames a file while preserving version history.

**Command**

```
git mv old.txt new.txt

```

---

# 25. git clean

**Description**

Deletes untracked files or directories.

**Command**

```
git clean -fd

```

---

# 26. git submodule

**Description**

Adds a separate Git repository inside your project.

**Command**

```
git submodule add <repo-url>

```

---

# 27. git clone

**Description**

Clones a remote repository to a local system.

**Command**

```
git clone <repo-url>

```

---

# 28. git remote -v

**Description**

Displays remote URLs connected to the repository.

**Command**

```
git remote -v

```

---

# 29. git blame

**Description**

Shows who last modified each line in a file. Helpful for root-cause analysis.

**Command**

```
git blame file.txt

```

---

# 30. git archive

**Description**

Creates an archive (ZIP/TAR) of project files excluding the Git history.

**Command**

```
git archive --format=zip HEAD > project.zip

```

---

# Git Installation & Setup

Git must be installed on developer machines and CI agents so everyone works consistently.

**Linux Installation**

```
sudo apt install git

```

**Global Setup**

```
git config --global user.name "Your Name"
git config --global user.email "you@mail.com"
git config --global init.defaultBranch main

```

---

# Git Project Basics

Core commands to initialize and manage a repository:

```
git init
git status
git add file.txt
git add .
git commit -m "message"
git remote add origin <url>
git push -u origin main

```

---

# Branching (Important for DevOps)

Branches allow independent work without affecting the main codebase.

```
git branch feature/login
git checkout feature/login
git checkout -b feature/login
git branch

```

---

# Merging Branches

```
git checkout main
git merge feature/login
git branch -d feature/login

```

---

# Pull, Fetch, Push

```
git pull
git fetch
git merge origin/main
git push

```

---

# Handling Merge Conflicts

Conflict markers:

```
<<<<<<< HEAD
your changes
=======
their changes
>>>>>>> branch

```

Fix manually, stage, and commit.

---

# Reset vs Revert vs Restore

- Reset → rewrite history
- Revert → safe rollback
- Restore → undo file changes locally

```
git reset --hard <commit>
git revert <commit>
git restore file.txt

```

---

# Pull Requests (Code Review)

PRs typically include:

- Summary of the change
- Associated issue or ticket
- Reviewer assignments
- CI/CD checks
- Security checks
- Final merge rules

---

# Git in CI/CD

Git events trigger:

- Build
- Test
- Static analysis
- Security scanning
- Deployment pipelines

Used across GitHub Actions, Jenkins, GitLab CI, and Azure DevOps.

---

# Git + SSH Keys

Generate secure key pair:

```
ssh-keygen -t ed25519 -C "you@mail.com"

```

Clone via SSH:

```
git clone git@github.com:user/repo.git

```

---

# Git Submodules (Advanced)

Useful for:

- Shared libraries
- Microservice dependencies
- Vendor code

---

# Git Best Practices

- Commit small and often
- Use meaningful commit messages
- Avoid committing secrets
- Protect the main branch
- Always use feature branches
- Use `.gitignore` properly
- Use tags for releases
- Rebase before merging to keep history clean
- Ensure code review happens through PRs

---

# Git Interview Questions

**Beginner**

- What is Git?
- What is a commit?
- Difference between clone and pull?
- What is a branch?

**Intermediate**

- How do merge conflicts occur?
- Merge vs rebase?
- What is HEAD?
- Reset vs revert vs restore?

**Advanced**

- What is GitFlow?
- What is detached HEAD?
- How does cherry-pick work?
- What is Git bisect?
- How do you secure secrets in Git?