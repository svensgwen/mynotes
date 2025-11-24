# 🌀 Git Cheat Sheet — Fast, Clean & Modern
![GIT](../../Images/git.webp)
## 📦 Setup
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global core.editor "code --wait"
```

## 🌱 Start a Repo
```bash
git init           # start local repo
git clone URL      # clone remote repo
```

## 📥 Staging & Committing
```bash
git status
git add file.txt
git add .          # stage all
git commit -m "message"
git commit -am "add + commit tracked files"
```

## 🔄 Branching
```bash
git branch                 # list
git branch new-feature     # create
git switch new-feature     # move to branch
git switch -c hotfix       # create + switch
git merge new-feature      # merge branch into current
git branch -d branchname   # delete
```

## 🚀 Pushing & Pulling
```bash
git remote -v
git remote add origin URL

git push origin main
git push -u origin main     # set default upstream

git pull                    # pull latest
git fetch                   # fetch without merging
```

## 🔍 Viewing History
```bash
git log
git log --oneline
git log --graph --decorate --all
```

## 🎯 Undoing
```bash
git restore file.txt             # restore file
git restore --staged file.txt    # unstage

git reset HEAD~1                 # undo last commit, keep changes
git reset --hard HEAD~1          # undo commit + discard changes
```

## 🧩 Stashing
```bash
git stash
git stash list
git stash apply
git stash pop
```

## 🪢 Merging & Conflicts
```bash
git merge branchname
# if conflict:
#   fix file manually
git add .
git commit
```

## 🔧 Rebase
```bash
git rebase main
git rebase -i HEAD~3     # interactive rebase
```

## 🎯 Tags (Releases)
```bash
git tag v1.0
git tag -a v1.0 -m "release message"
git push origin --tags
```

## 🗑️ Remove Files
```bash
git rm file.txt
git rm -r folder/
```

## 🪄 Clone Shallow
```bash
git clone --depth=1 URL
```

## 🔐 GitHub SSH Setup
```bash
ssh-keygen -t ed25519 -C "you@example.com"
cat ~/.ssh/id_ed25519.pub
# add to GitHub → Settings → SSH Keys
```

## 🧹 Clean Up
```bash
git clean -n     # preview
git clean -f     # remove untracked files
```

## 🌍 Useful .gitignore template
```bash
*.log
node_modules/
dist/
.env
__pycache__/
```

## 🧠 TL;DR Flow
```bash
git add .
git commit -m "your message"
git push
```
