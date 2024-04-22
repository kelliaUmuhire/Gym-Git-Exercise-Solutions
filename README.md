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
The GYM\git-exercises>git stash push -u -m "Home page"
Saved working directory and index state On dev: Home page

The GYM\git-exercises>git stash push -u -m "About page"
Saved working directory and index state On dev: About page

The GYM\git-exercises>git stash push -u -m "Team page"
Saved working directory and index state On dev: Team page

The GYM\git-exercises>git stash list
stash@{0}: On dev: Team page
stash@{1}: On dev: About page
stash@{2}: On dev: Home page

The GYM\git-exercises>git stash apply stash@{1}
Already up to date.
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)

The GYM\git-exercises>git stash list
stash@{0}: On dev: Team page
stash@{1}: On dev: About page
stash@{2}: On dev: Home page

The GYM\git-exercises>git stash apply stash@{2}
Already up to date.
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        home.html

nothing added to commit but untracked files present (use "git add" to track)

The GYM\git-exercises>git add .

The GYM\git-exercises>git commit -m "Home and about page"
[dev 55122da] Home and about page
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

The GYM\git-exercises>git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


The GYM\git-exercises>git push --set-upstream origin dev
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

The GYM\git-exercises>git stash clear

The GYM\git-exercises>git add .

The GYM\git-exercises>git commit -m "Reset for bundle 1 exercise 2"
[dev 92106d5] Reset for bundle 1 exercise 2
 2 files changed, 22 deletions(-)
 delete mode 100644 about.html
 delete mode 100644 home.html

The GYM\git-exercises>git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (1/1), done.
Writing objects: 100% (2/2), 249 bytes | 124.00 KiB/s, done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/kelliaUmuhire/git-exercises.git
   55122da..92106d5  dev -> dev

The GYM\git-exercises>git add home.html

The GYM\git-exercises>git stash
Saved working directory and index state WIP on dev: 92106d5 Reset for bundle 1 exercise 2

The GYM\git-exercises>git add about.html

The GYM\git-exercises>git stash
Saved working directory and index state WIP on dev: 92106d5 Reset for bundle 1 exercise 2

The GYM\git-exercises>git add team.html

The GYM\git-exercises>git stash
Saved working directory and index state WIP on dev: 92106d5 Reset for bundle 1 exercise 2

The GYM\git-exercises>git stash list
stash@{0}: WIP on dev: 92106d5 Reset for bundle 1 exercise 2
stash@{1}: WIP on dev: 92106d5 Reset for bundle 1 exercise 2
stash@{2}: WIP on dev: 92106d5 Reset for bundle 1 exercise 2

The GYM\git-exercises>git stash apply stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html


The GYM\git-exercises>git stash apply stash@{2}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html


The GYM\git-exercises>git commit -m "Home page & about page"
[dev e2707d0] Home page & about page
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

The GYM\git-exercises>git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 529 bytes | 176.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/kelliaUmuhire/git-exercises.git
   92106d5..e2707d0  dev -> dev

The GYM\git-exercises>git stash apply stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html


The GYM\git-exercises>git reset --hard
HEAD is now at e2707d0 Home page & about page
```

## Bundle 2

### Exercise 1

```bash
The GYM\git-exercises>git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

The GYM\git-exercises>git branch
  dev
* ft/bundle-2
  main

The GYM\git-exercises>git add services.html

The GYM\git-exercises>git commit -m "Added services page"
[ft/bundle-2 fe381f1] Added services page
 1 file changed, 11 insertions(+)
 create mode 100644 services.html

The GYM\git-exercises>git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


The GYM\git-exercises>git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 439 bytes | 439.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/kelliaUmuhire/git-exercises/pull/new/ft/bundle-2
remote:
To https://github.com/kelliaUmuhire/git-exercises.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
```

### Exercise 2

```bash
The GYM\git-exercises>git checkout main
Switched to branch 'main'

The GYM\git-exercises>git add .

The GYM\git-exercises>git commit -m "Added changes to services page"
[main e944465] Added changes to services page
 1 file changed, 1 insertion(+), 1 deletion(-)

The GYM\git-exercises>git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


The GYM\git-exercises>git push --set-upstream origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 330 bytes | 330.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/kelliaUmuhire/git-exercises.git
   fdc23b2..e944465  main -> main
branch 'main' set up to track 'origin/main'.

The GYM\git-exercises>git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

The GYM\git-exercises>git diff

The GYM\git-exercises>git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

The GYM\git-exercises>git diff
diff --cc services.html
index c6025a7,f470287..0000000
--- a/services.html
+++ b/services.html
@@@ -6,9 -6,6 +6,13 @@@
      <title>Services Page</title>
    </head>
    <body>
++<<<<<<< HEAD
 +    <h1>Services</h1>
 +    <p>
 +      The main purpose of the services page is to show the services we provide
 +    </p>
++=======
+     <h1>Services Main Page</h1>
++>>>>>>> main
    </body>
  </html>

The GYM\git-exercises>git merge main
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

The GYM\git-exercises>git add .

The GYM\git-exercises>git commit -m "Resolved conflicts"
[ft/service-redesign d8618e3] Resolved conflicts

The GYM\git-exercises>git merge main
Already up to date.

The GYM\git-exercises>git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


The GYM\git-exercises>git push --set-upstream origin ft/service-redesign
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 222 bytes | 222.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/kelliaUmuhire/git-exercises.git
   51a94c9..d8618e3  ft/service-redesign -> ft/service-redesign
```

## Bundle 3

### Exercise 1

```bash
The GYM\git-exercises>git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

The GYM\git-exercises>git add team.html

The GYM\git-exercises>git commit -m "Added team page"
[ft/team-page 789e0c0] Added team page
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

The GYM\git-exercises>git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 430 bytes | 430.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/kelliaUmuhire/git-exercises/pull/new/ft/team-page
remote:
To https://github.com/kelliaUmuhire/git-exercises.git
 * [new branch]      ft/team-page -> ft/team-page

The GYM\git-exercises>git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

The GYM\git-exercises>git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

The GYM\git-exercises>git checkout ft/team-page
Switched to branch 'ft/team-page'

The GYM\git-exercises>git log --oneline
789e0c0 (HEAD -> ft/team-page, origin/ft/team-page) Added team page
e944465 (origin/main, main, ft/contact-page) Added changes to services page
fdc23b2 Merge pull request #2 from kelliaUmuhire/ft/bundle-2
fe381f1 (origin/ft/bundle-2, ft/bundle-2) Added services page
e2707d0 (origin/dev, dev) Home page & about page
92106d5 Reset for bundle 1 exercise 2
55122da Home and about page
b4710cd Added README.md

The GYM\git-exercises>git checkout ft/contact-page
Switched to branch 'ft/contact-page'

The GYM\git-exercises>git cherry-pick 789e0c0
[ft/contact-page 36e0779] Added team page
 Date: Mon Apr 22 16:58:51 2024 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

The GYM\git-exercises>git add contact.html

The GYM\git-exercises>git commit -m "Added contact page"
[ft/contact-page 6e6fcb5] Added contact page
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html

The GYM\git-exercises>git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 701 bytes | 701.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/kelliaUmuhire/git-exercises/pull/new/ft/contact-page
remote:
To https://github.com/kelliaUmuhire/git-exercises.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

The GYM\git-exercises>git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

The GYM\git-exercises>git add faq.html

The GYM\git-exercises>git commit -m "Added faq page"
[ft/faq-page cef4dd8] Added faq page
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

The GYM\git-exercises>git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


The GYM\git-exercises>git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 428 bytes | 428.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/kelliaUmuhire/git-exercises/pull/new/ft/faq-page
remote:
To https://github.com/kelliaUmuhire/git-exercises.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

The GYM\git-exercises>git revert 789e0c0
[ft/faq-page c96f4e0] Revert "Added team page"
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html

The GYM\git-exercises>git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 271 bytes | 271.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/kelliaUmuhire/git-exercises.git
   cef4dd8..c96f4e0  ft/faq-page -> ft/faq-page
```

### Exercise 2

```bash
The GYM\git-exercises>git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

The GYM\git-exercises>git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

The GYM\git-exercises>git add .

The GYM\git-exercises>git commit -m "Update home page"
[main c0ab80d] Update home page
 1 file changed, 1 insertion(+), 1 deletion(-)

The GYM\git-exercises>git push
To https://github.com/kelliaUmuhire/git-exercises.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/kelliaUmuhire/git-exercises.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

The GYM\git-exercises>git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 924 bytes | 11.00 KiB/s, done.
From https://github.com/kelliaUmuhire/git-exercises
   e944465..115c92e  main       -> origin/main
Merge made by the 'ort' strategy.
 services.html | 5 ++++-
 1 file changed, 4 insertions(+), 1 deletion(-)

The GYM\git-exercises>git push
Enumerating objects: 9, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 589 bytes | 589.00 KiB/s, done.
Total 5 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
To https://github.com/kelliaUmuhire/git-exercises.git
   115c92e..6d5faa1  main -> main

The GYM\git-exercises>git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

The GYM\git-exercises>git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

The GYM\git-exercises>git add .

The GYM\git-exercises>git commit -m "Updated home page"
[ft/home-page-redesign e5a20e9] Updated home page
 1 file changed, 1 insertion(+)

The GYM\git-exercises>git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 8 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.52 KiB | 1.52 MiB/s, done.
Total 14 (delta 7), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (7/7), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/kelliaUmuhire/git-exercises/pull/new/ft/home-page-redesign
remote:
To https://github.com/kelliaUmuhire/git-exercises.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.
```

## Bundle 4

### Exercise 1

```bash
The GYM\git-exercises>git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

The GYM\git-exercises>git remote add git-copy https://github.com/kelliaUmuhire/git-exercises-copy.git

The GYM\git-exercises>git add .

The GYM\git-exercises>git commit -m "Updated home page"
[main a3b6746] Updated home page
 1 file changed, 1 insertion(+)

The GYM\git-exercises>git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 330 bytes | 330.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/kelliaUmuhire/git-exercises.git
   6d5faa1..a3b6746  main -> main

The GYM\git-exercises>git push git-copy main
Enumerating objects: 32, done.
Counting objects: 100% (32/32), done.
Delta compression using up to 8 threads
Compressing objects: 100% (30/30), done.
Writing objects: 100% (32/32), 4.56 KiB | 2.28 MiB/s, done.
Total 32 (delta 17), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (17/17), done.
To https://github.com/kelliaUmuhire/git-exercises-copy.git
 * [new branch]      main -> main
```

### Exercise 2

```bash
The GYM\git-exercises>git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'

The GYM\git-exercises>git merge --squash ft/footer
Updating a3b6746..3edefba
Fast-forward
Squash commit -- not updating HEAD
 home.html | 5 +++++
 1 file changed, 5 insertions(+)

The GYM\git-exercises>git commit -m "Footer changes squashing"
[ft/squashing 590c5e6] Footer changes squashing
 1 file changed, 5 insertions(+)

The GYM\git-exercises>git push origin ft/squashing
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 372 bytes | 372.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/kelliaUmuhire/git-exercises/pull/new/ft/squashing
remote:
To https://github.com/kelliaUmuhire/git-exercises.git
 * [new branch]      ft/squashing -> ft/squashing
```

## Bundle 5

### Exercise 5

```bash
The GYM>git clone https://github.com/kelliaUmuhire/git-cafe-exercise.git
Cloning into 'git-cafe-exercise'...
remote: Enumerating objects: 107, done.
remote: Counting objects: 100% (14/14), done.
remote: Compressing objects: 100% (10/10), done.
Receiving objects:  99% (106/107), 1.92 MiB | 1.43 MiB/sused 93
Receiving objects: 100% (107/107), 1.95 MiB | 1.06 MiB/s, done.
Resolving deltas: 100% (5/5), done.

The GYM>cd git-cafe-exercise

The GYM\git-cafe-exercise>git add .

The GYM\git-cafe-exercise>git commit -m "Edited index.html"
[main c80145c] Edited index.html
 1 file changed, 399 insertions(+), 239 deletions(-)

The GYM\git-cafe-exercise>git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.55 KiB | 1.55 MiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/kelliaUmuhire/git-cafe-exercise.git
   d1d3f9c..c80145c  main -> main
```
