## 清空 git 的历史

好像不管用……

```plain
Administrator@lennovo-PC MINGW64 /d/tzx/git
$ git clone $(cat url)
Cloning into 'github-pure-hosting'...
remote: Counting objects: 3, done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
Checking connectivity... done.

Administrator@lennovo-PC MINGW64 /d/tzx/git
$ cd github-pure-hosting/

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ ls
README.md

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ rm -f .git/index

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ git clean -df
Removing README.md

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ ls

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ l .git
bash: l: command not found

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ ls .git
config  description  HEAD  hooks/  info/  logs/  objects/  packed-refs  refs/

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ echo > README.md <<EOF
> 完全清空 Git 的历史。
> EOF

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ git add README.md
warning: LF will be replaced by CRLF in README.md.
The file will have its original line endings in your working directory.

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ git commit -m "will this work?"
[master warning: LF will be replaced by CRLF in README.md.
The file will have its original line endings in your working directory.
d53735d] will this work?
warning: LF will be replaced by CRLF in README.md.
The file will have its original line endings in your working directory.
 1 file changed, 1 insertion(+), 2 deletions(-)

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ git push
Counting objects: 3, done.
Writing objects: 100% (3/3), 254 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To git@github.com:district10/github-pure-hosting.git
   e7e88dc..d53735d  master -> master

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ git diff

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ rm -f .git/index

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ git clean -df
Removing README.md

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        deleted:    README.md


Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$ git diff

Administrator@lennovo-PC MINGW64 /d/tzx/git/github-pure-hosting (master)
$
```
