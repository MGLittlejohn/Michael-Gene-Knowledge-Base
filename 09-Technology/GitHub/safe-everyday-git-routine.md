# Safe Everyday Git Routine

## Routine
1. Open the local knowledge-base folder.
2. Run `git status`.
3. If the repository may have newer remote changes, run `git pull` before starting fresh local edits.
4. Create or edit the intended file.
5. Run `git status` again.
6. Stage only the intended file(s) with `git add <file>`.
7. Check `git status` again.
8. Commit with a short descriptive message.
9. Push to GitHub.
10. Run `git status` and optionally `git log --oneline -3` to verify.

## Big Idea
**Local file → status → add → commit → push → GitHub.**

Creating a file on the Mac does not put it on GitHub by itself. Git must stage it, commit it, and push it.

## Safety Rule
Before doing anything destructive, run `git status`. It reports what Git sees without changing files.

## Porch Rule
**Status before action. Commit before push.**
