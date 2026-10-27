# Campus Connect — Git & GitHub Assignment

Practical assignment for **Version Control System**, B.Tech, 3rd Semester, Section F (Session 2026–2027).

| | |
|---|---|
| **Student** | Yash Khatana |
| **URN** | 2581442 |
| **Faculty** | Dr. Sangeeta |
| **School** | School of Computer Science and Engineering |

## Assigned problems

| ID | Problem statement |
|---|---|
| GIT-02 | Check Git Configuration |
| GIT-29 | Create Multiple Feature Branches |

## GIT-02 — Check Git Configuration

```bash
git --version                         # confirm Git is installed
git config --global --list            # before: no ~/.gitconfig exists
git config --global user.name "Yash Khatana"
git config --global user.email "itsyash2008@gmail.com"
git config --global core.editor "nano"
git config --global color.ui auto
git config --list --show-scope        # which level each setting comes from
git config --show-origin user.email   # which file a value lives in
```

## GIT-29 — Create Multiple Feature Branches

Each feature of the site is developed on its own branch, isolated from `main`:

| Branch | Feature | Created with |
|---|---|---|
| `feature/login` | Student login page | `git branch` |
| `feature/dashboard` | Attendance and marks dashboard | `git checkout -b` |
| `feature/dark-mode` | Dark colour theme | `git switch -c` |

```bash
git branch feature/login              # create only
git checkout -b feature/dashboard     # create and switch (classic)
git switch -c feature/dark-mode       # create and switch (modern)
git branch -v                         # list branches with their last commit
git log --oneline --graph --all       # see the branches diverge from main
git push -u origin --all              # publish every branch to GitHub
git branch -a                         # local and remote-tracking branches
```
