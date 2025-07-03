# Git Cheat Sheet

Git is the free and open source distributed version control system that's responsible for everything GitHub related that happens locally on our computer. This cheat sheet features the most important and commonly used Git commands for easy reference.

## SETUP
*Configuring user information used across all local repositories*

Set a name that is identifiable for credit when reviewing version history:
```bash
git config --global user.name "[firstname lastname]"
```

Set an email address that will be associated with each history marker:
```bash
git config --global user.email "[valid-email]"
```

Set automatic command line coloring for Git for easy reviewing:
```bash
git config --global color.ui auto
```

## SETUP & INIT
*Configuring user information, initializing and cloning repositories*

Initialize an existing directory as a Git repository:
```bash
git init
```

Retrieve an entire repository from a hosted location via URL:
```bash
git clone [url]
```

## STAGE & SNAPSHOT
*Working with snapshots and the Git staging area*

Show modified files in working directory, staged for your next commit:
```bash
git status
```

Add a file as it looks now to your next commit (stage):
```bash
git add [file]
```

Unstage a file while retaining the changes in working directory:
```bash
git reset [file]
```

Diff of what is changed but not staged:
```bash
git diff
```

Diff of what is staged but not yet committed:
```bash
git diff --staged
```

Commit your staged content as a new commit snapshot:
```bash
git commit -m "[descriptive message]"
```

## BRANCH & MERGE
*Isolating work in branches, changing context, and integrating changes*

List your branches. A * will appear next to the currently active branch:
```bash
git branch
```

Create a new branch at the current commit:
```bash
git branch [branch-name]
```

Switch to another branch and check it out into your working directory:
```bash
git checkout [branch-name]
```

Merge the specified branch's history into the current one:
```bash
git merge [branch]
```

Show all commits in the current branch's history:
```bash
git log
```

## INSPECT & COMPARE
*Examining logs, diffs and object information*

Show the commit history for the currently active branch:
```bash
git log
```

Show the commits on branchA that are not on branchB:
```bash
git log branchB..branchA
```

Show the commits that changed file, even across renames:
```bash
git log --follow [file]
```

Show the diff of what is in branchA that is not in branchB:
```bash
git diff branchB...branchA
```

Show any object in Git in human-readable format:
```bash
git show [SHA]
```

## TRACKING PATH CHANGES
*Versioning file removes and path changes*

Delete the file from project and stage the removal for commit:
```bash
git rm [file]
```

Change an existing file path and stage the move:
```bash
git mv [existing-path] [new-path]
```

Show all commit logs with indication of any paths that moved:
```bash
git log --stat -M
```

## SHARE & UPDATE
*Retrieving updates from another repository and updating local repos*

Add a git URL as an alias:
```bash
git remote add [alias] [url]
```

Fetch down all the branches from that Git remote:
```bash
git fetch [alias]
```

Merge a remote branch into your current branch to bring it up to date:
```bash
git merge [alias]/[branch]
```

Transmit local branch commits to the remote repository branch:
```bash
git push [alias] [branch]
```

Fetch and merge any commits from the tracking remote branch:
```bash
git pull
```

## REWRITE HISTORY
*Rewriting branches, updating commits and clearing history*

Apply any commits of current branch ahead of specified one:
```bash
git rebase [branch]
```

Clear staging area, rewrite working tree from specified commit:
```bash
git reset --hard [commit]
```

## TEMPORARY COMMITS
*Temporarily store modified, tracked files in order to change branches*

Save modified and staged changes:
```bash
git stash
```

List stack-order of stashed file changes:
```bash
git stash list
```

Write working from top of stash stack:
```bash
git stash pop
```

Discard the changes from top of stash stack:
```bash
git stash drop
```

## IGNORING PATTERNS
*Preventing unintentional staging or committing of files*

System wide ignore pattern for all local repositories:
```bash
git config --global core.excludesfile [file]
```

Save a file with desired patterns as `.gitignore` with either direct string matches or wildcard globs:
```gitignore
logs/
*.notes
pattern*/
```

## INSTALLATION & GUIS

With platform specific installers for Git, GitHub also provides the ease of staying up-to-date with the latest releases of the command line tool while providing a graphical user interface for day-to-day interaction, review, and repository synchronization.

- **GitHub for Windows**: https://windows.github.com
- **GitHub for Mac**: https://mac.github.com
- **Git for All Platforms**: http://git-scm.com

For Linux and Solaris platforms, the latest release is available on the official Git web site.

---

*education@github.com | education.github.com*


## 📬 Connect with Me

<p align="center">
  <a href="https://github.com/Akib-Osmani" target="_blank" rel="noopener">
    <img alt="GitHub" src="https://img.shields.io/badge/-GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
  <a href="https://www.linkedin.com/in/akib-osmani02" target="_blank" rel="noopener">
    <img alt="LinkedIn" src="https://img.shields.io/badge/-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="mailto:akibaiub.edu@gmail.com" target="_blank" rel="noopener">
    <img alt="Email" src="https://img.shields.io/badge/-Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
</p>


## 📄 License

This project is open-source and available under the [Apache 2.0 License](LICENSE).