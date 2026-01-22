This is a simple Git cheat sheet covering the commands I use most often.

---

## Check status
See what’s going on before doing anything:
```bash
git status -sb
Add (stage changes)
Stage everything:

git add .
Stage interactively (recommended):

git add -p
Commit
Save changes locally:

git commit -m "Describe what you changed"
Useful:

git commit -am "msg" → add + commit tracked files

git commit --amend → fix last commit

Push
First push (sets upstream):

git push -u origin main
After that:

git push
Pull
Get latest changes:

git pull
Useful:

git pull --rebase → cleaner history

git pull --ff-only → avoids merge commits

Change origin URL
Check current remote:

git remote -v
Change origin:

git remote set-url origin git@github.com:ORG/REPO.git
Stash
Temporarily save work:

git stash
Apply stash:

git stash pop
Useful:

git stash -u → include untracked files

Revert vs Reset
Revert (safe, creates new commit):

git revert <commit_sha>
Reset (rewrites history, be careful):

git reset --soft HEAD~1
git reset --hard HEAD~1
Log
View commit history:

git log --oneline --graph --all
Diff
See changes:

git diff
git diff --staged
Show
Inspect one commit:

git show <commit_sha>
Common workflow
git status -sb
git add -p
git commit -m "Explain change"
git pull --rebase
git push
