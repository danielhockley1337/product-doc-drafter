Commit all local changes and push to GitHub.

1. Run `git rev-parse --is-inside-work-tree` to check if the current directory is inside a git repo. If it's not, report "Not a git repository" and stop.

2. Run `git add -A` to stage all changes (tracked, untracked, and new files).

3. Run `git diff --cached --stat` to see what's staged. If nothing is staged, report "Nothing to commit - working tree clean" and stop.

4. Run `git diff --cached` to read the full staged diff. Use it to write a short, descriptive commit message that summarizes what actually changed. One sentence, plain language, no padding.

5. Commit with that message:
```
git commit -m "<generated message>"
```

6. Run `git push origin HEAD` to push to the current branch.

7. Report back:
- The commit message
- The diff summary (files changed, insertions, deletions)
- Confirmation that the push succeeded
