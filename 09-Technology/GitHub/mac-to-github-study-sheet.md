# Mac → Git → GitHub Study Sheet

## The Big Idea
A file is not on GitHub merely because it exists on the Mac. Git must see it, stage it, commit it, and then push the commit to GitHub.

**Mac file → Git status → Git add → Git commit → Git push → GitHub**

## Safe Everyday Routine
1. Open the knowledge-base repository.
2. Run `git status`.
3. Create or edit the file.
4. Run `git status` again.
5. Stage the intended file with `git add <file>`.
6. Run `git status` and verify what is staged.
7. Commit with a short descriptive message: `git commit -m "Describe what you changed"`.
8. Push with `git push`.
9. Run `git status` again.
10. Optionally run `git log --oneline -3` and verify the result on GitHub.

## Useful Commands
- `git status` — shows what Git sees without changing anything.
- `git pull` — brings newer GitHub changes down to the local repository.
- `git add <file>` — stages a chosen file for the next commit.
- `git commit -m "message"` — records the staged change locally.
- `git push` — sends local commits to GitHub.
- `git log --oneline -3` — shows the three most recent commits.

## Safety Rule
Before doing anything destructive or when uncertain, run `git status` first. It reports the current state without modifying files.

## Porch Thought
**Status before action, commit before push.**
