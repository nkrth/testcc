# testcc

[![Build Status](https://travis-ci.org/NickKartha/testcc.svg?branch=master)](https://travis-ci.org/NickKartha/testcc)

Using cookie_cutter to build a test module for PyPI

Travis CI: https://travis-ci.org/NickKartha/testcc

Base repo: https://github.com/audreyr/cookiecutter-pypackage/

According to https://help.github.com/en/articles/adding-an-existing-project-to-github-using-the-command-line
I may have started erroneosly because I put in a `README.md` before pushing the project.
I am now facing issues pushing the project.

Steps ommiting few:

1. [x] Open Git Bash.

2. [x] `$git init` : Initializes the repository
```
    C:\Users\CCF\Desktop\GROUP 17\testcc>git init
    Reinitialized existing Git repository in C:/Users/CCF/Desktop/GROUP 17/testcc/.git/
```
3. [x] `$ git add .` : Adds the files in the local repository and stages them for commit. 
To unstage a file, use `git reset HEAD YOUR-FILE`.
```
C:\Users\CCF\Desktop\GROUP 17\testcc>git reset .
C:\Users\CCF\Desktop\GROUP 17\testcc>git add .
```

4. [x] Commit the files that you've staged in your local repository.
`$ git commit -m "First commit"`: Commits the tracked changes and prepares them to be pushed to a remote repository. 
To remove this commit and modify the file, use `git reset --soft HEAD~1` and commit and add the file again.
```
C:\Users\CCF\Desktop\GROUP 17\testcc>git commit -m "First commit"
[master (root-commit) 33c826d] First commit
 29 files changed, 913 insertions(+)
 create mode 100644 .editorconfig
 create mode 100644 .github/ISSUE_TEMPLATE.md
 create mode 100644 .gitignore
 create mode 100644 .travis.yml
 create mode 100644 AUTHORS.rst
 create mode 100644 CONTRIBUTING.rst
 create mode 100644 HISTORY.rst
 create mode 100644 MANIFEST.in
 create mode 100644 Makefile
 create mode 100644 README.rst
 create mode 100644 docs/Makefile
 create mode 100644 docs/authors.rst
 create mode 100644 docs/conf.py
 create mode 100644 docs/contributing.rst
 create mode 100644 docs/history.rst
 create mode 100644 docs/index.rst
 create mode 100644 docs/installation.rst
 create mode 100644 docs/make.bat
 create mode 100644 docs/readme.rst
 create mode 100644 docs/usage.rst
 create mode 100644 requirements_dev.txt
 create mode 100644 setup.cfg
 create mode 100644 setup.py
 create mode 100644 testcc/__init__.py
 create mode 100644 testcc/cli.py
 create mode 100644 testcc/testcc.py
 create mode 100644 tests/__init__.py
 create mode 100644 tests/test_testcc.py
 create mode 100644 tox.ini
```

5. [x] At the top of your GitHub repository's Quick Setup page, click  to copy the remote repository URL.
> `https://github.com/NickKartha/testcc.git`

6. [x] In the Command prompt, add the URL for the remote repository where your local repository will be pushed.
[resource: https://help.github.com/en/articles/adding-a-remote]
```
$ git remote add origin remote repository URL
# Sets the new remote
$ git remote -v
# Verifies the new remote URL
```
```
C:\Users\CCF\Desktop\GROUP 17\testcc>git remote add origin "https://github.com/NickKartha/testcc.git"

C:\Users\CCF\Desktop\GROUP 17\testcc>git remote -v
origin  https://github.com/NickKartha/testcc.git (fetch)
origin  https://github.com/NickKartha/testcc.git (push)
testcc  https://github.com/NickKartha/testcc (fetch)
testcc  https://github.com/NickKartha/testcc (push)
upstream        https://github.com/NickKartha/testcc.git (fetch)
upstream        https://github.com/NickKartha/testcc.git (push)

C:\Users\CCF\Desktop\GROUP 17\testcc>
```

7. [ ] Push the changes in your local repository to GitHub.
```
$ git push origin master
# Pushes the changes in your local repository up to the remote repository you specified as the origin
```
```
C:\Users\CCF\Desktop\GROUP 17\testcc>git push origin master
To https://github.com/NickKartha/testcc.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/NickKartha/testcc.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

C:\Users\CCF\Desktop\GROUP 17\testcc>git pull ...
fatal: '...' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

C:\Users\CCF\Desktop\GROUP 17\testcc>git pull  .
From .
 * branch            HEAD       -> FETCH_HEAD
Already up to date.

C:\Users\CCF\Desktop\GROUP 17\testcc> git push origin master
To https://github.com/NickKartha/testcc.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/NickKartha/testcc.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

C:\Users\CCF\Desktop\GROUP 17\testcc>git add .
warning: LF will be replaced by CRLF in README.md.
The file will have its original line endings in your working directory

C:\Users\CCF\Desktop\GROUP 17\testcc>git push origin msater
error: src refspec msater does not match any.
error: failed to push some refs to 'https://github.com/NickKartha/testcc.git'
```

Stuck here. Feel free to submit issue.

Ok, continuing. I took the existing `README.md` from the latest zip and manually put it into the local repo folder.

Samson tried to help. His attmpt follows:
```
C:\Users\CCF\Desktop\GROUP 17\testcc>git init
Reinitialized existing Git repository in C:/Users/CCF/Desktop/GROUP 17/testcc/.git/

C:\Users\CCF\Desktop\GROUP 17\testcc>git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   README.md


C:\Users\CCF\Desktop\GROUP 17\testcc>git add --all

C:\Users\CCF\Desktop\GROUP 17\testcc>git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   README.md


C:\Users\CCF\Desktop\GROUP 17\testcc>git commit -m "Initial commit"
[master 58bbdd5] Initial commit
 1 file changed, 2 insertions(+)
 create mode 100644 README.md

```
We encountered the same error when we tried `git push remote master`

I googled the symptom and got back this useful guide: https://blog.plover.com/prog/git-ff-error.html

It explains to do the following:

+ [ ] 1. Fetch the remote master branch and check it out.

+ [ ] 2. Do some work and commit it on the local master.

+ [ ] 3. Push the new work back to the remote.

+ [ ] 4. Refresh the tracking branch.

+ [ ] 5. Rewrite the local changes.

+ [ ] 6. Try the push again.

--> I'll try to this out soon ;;

