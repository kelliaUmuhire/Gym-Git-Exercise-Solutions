## Bundle 1

### Exercise 1

```bash
The GYM>mkdir git-exercises

The GYM>cd git-exercises

The GYM\git-exercises>git init
Initialized empty Git repository in C:/Users/Kellia/Documents/Projects/STUDIES/The GYM/git-exercises/.git/

The GYM\git-exercises>git branch -m main

The GYM\git-exercises>git add README.md

The GYM\git-exercises>git commit -m "Added README.md"
[main (root-commit) b4710cd] Added README.md
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

The GYM\git-exercises>git remote add origin https://github.com/kelliaUmuhire/git-exercises.git

The GYM\git-exercises>git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 241 bytes | 241.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/kelliaUmuhire/git-exercises.git
 * [new branch]      main -> main

The GYM\git-exercises>git checkout -b dev
Switched to a new branch 'dev'

The GYM\git-exercises>git checkout -b test
Switched to a new branch 'test'

The GYM\git-exercises>git checkout dev
Switched to branch 'dev'

The GYM\git-exercises>git branch -d test
Deleted branch test (was b4710cd).
```

### Exercise 2

```bash
C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash push -u -m "Home page"
Saved working directory and index state On dev: Home page

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash push -u -m "About page"
Saved working directory and index state On dev: About page

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash push -u -m "Team page"
Saved working directory and index state On dev: Team page

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash list
stash@{0}: On dev: Team page
stash@{1}: On dev: About page
stash@{2}: On dev: Home page

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash apply stash@{1}
Already up to date.
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash list
stash@{0}: On dev: Team page
stash@{1}: On dev: About page
stash@{2}: On dev: Home page

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash apply stash@{2}
Already up to date.
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        home.html

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git add .

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git commit -m "Home and about page"
[dev 55122da] Home and about page
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git push --set-upstream origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 500 bytes | 125.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/kelliaUmuhire/git-exercises/pull/new/dev
remote:
To https://github.com/kelliaUmuhire/git-exercises.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash clear

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git add .

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git commit -m "Reset for bundle 1 exercise 2"
[dev 92106d5] Reset for bundle 1 exercise 2
 2 files changed, 22 deletions(-)
 delete mode 100644 about.html
 delete mode 100644 home.html

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (1/1), done.
Writing objects: 100% (2/2), 249 bytes | 124.00 KiB/s, done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/kelliaUmuhire/git-exercises.git
   55122da..92106d5  dev -> dev

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git add home.html

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash
Saved working directory and index state WIP on dev: 92106d5 Reset for bundle 1 exercise 2

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git add about.html

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash
Saved working directory and index state WIP on dev: 92106d5 Reset for bundle 1 exercise 2

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git add team.html

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash
Saved working directory and index state WIP on dev: 92106d5 Reset for bundle 1 exercise 2

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash list
stash@{0}: WIP on dev: 92106d5 Reset for bundle 1 exercise 2
stash@{1}: WIP on dev: 92106d5 Reset for bundle 1 exercise 2
stash@{2}: WIP on dev: 92106d5 Reset for bundle 1 exercise 2

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash apply stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html


C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash apply stash@{2}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html


C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git commit -m "Home page & about page"
[dev e2707d0] Home page & about page
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 529 bytes | 176.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/kelliaUmuhire/git-exercises.git
   92106d5..e2707d0  dev -> dev

C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git stash apply stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html


C:\Users\Kellia\Documents\Projects\STUDIES\The GYM\git-exercises>git reset --hard
HEAD is now at e2707d0 Home page & about page
```
