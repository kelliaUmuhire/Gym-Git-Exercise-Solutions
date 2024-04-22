## Bundle 1

### Exercise 1

Repo:

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
