Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git pull origin master
From https://gitee.com/jiaxisky/learngit
 * branch            master     -> FETCH_HEAD
Already up to date.

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ ^C

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git fetch --all

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git reset --hard origin/master
HEAD is now at ef3d196 提交关系图

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git pull origin master
From https://gitee.com/jiaxisky/learngit
 * branch            master     -> FETCH_HEAD
Already up to date.

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> master


Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git init
Initialized empty Git repository in D:/Obsidian/document site/Excalidraw/xuexi/.git/

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=<remote>/<branch> master


Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ origin master
bash: origin: command not found

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git pull origin master
fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$  git remote -v

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git remote add origin https://gitee.com/jiaxisky/learngit

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git pull --rebase origin master
remote: Enumerating objects: 19, done.
remote: Counting objects: 100% (19/19), done.
remote: Compressing objects: 100% (15/15), done.
remote: Total 19 (delta 3), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (19/19), 3.20 KiB | 3.00 KiB/s, done.
From https://gitee.com/jiaxisky/learngit
 * branch            master     -> FETCH_HEAD
 * [new branch]      master     -> origin/master

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git add sss.txt

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git commit -m "提交sss"
[master 27e3de3] 提交sss
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 sss.txt

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git push origin master
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 6 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 267 bytes | 267.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Powered by GITEE.COM [GNK-6.4]
To https://gitee.com/jiaxisky/learngit
   ef3d196..27e3de3  master -> master

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git remote add origin https://github.com/jiaxisky/learngit
error: remote origin already exists.

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git add sss.txt

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$  git commit -m "提交sss"
On branch master
nothing to commit, working tree clean

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$  git push origin master
Everything up-to-date

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git remote add origin git@github.com:jiaxisky/learngit
error: remote origin already exists.

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git remote rm origin

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git remote add origin git@github.com:jiaxisky/learngit

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git add sss.txt

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git commit -m "提交sss"
[master 7a9cf43] 提交sss
 1 file changed, 1 insertion(+)

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git push origin master
To github.com:jiaxisky/learngit
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'github.com:jiaxisky/learngit'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$ git pull --rebase origin master
remote: Enumerating objects: 10, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 9 (delta 2), reused 8 (delta 1), pack-reused 0
Unpacking objects: 100% (9/9), 588.19 KiB | 512.00 KiB/s, done.
From github.com:jiaxisky/learngit
 * branch            master     -> FETCH_HEAD
 * [new branch]      master     -> origin/master
Successfully rebased and updated refs/heads/master.

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)
$  git push origin master
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 6 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (9/9), 2.36 KiB | 2.36 MiB/s, done.
Total 9 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
To github.com:jiaxisky/learngit
   1aebf2b..53246c6  master -> master

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site/Excalidraw/xuexi (master)

# 常用语句

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git add .
warning: in the working copy of '.obsidian/plugins/obsidian-weread-plugin/data.json', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of '.obsidian/workspace.json', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'Obsidian Document/微信读书/精品小说/小巷人家-大米.md', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'Obsidian Document/笔记本/git教程.md', LF will be replaced by CRLF the next time Git touches it

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git remote -v
origin  git@github.com:jiaxisky//obsidian_workspace (fetch)
origin  git@github.com:jiaxisky//obsidian_workspace (push)

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git remote add origin git@github.com:jiaxisky/obsidianworkspace
error: remote origin already exists.

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git remote rm origin

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$  git remote -v

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git remote add origin git@github.com:jiaxisky/obsidianworkspace.git

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git remote -v
origin  git@github.com:jiaxisky/obsidianworkspace.git (fetch)
origin  git@github.com:jiaxisky/obsidianworkspace.git (push)

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git add .
warning: in the working copy of 'Obsidian Document/笔记本/git教程.md', LF will be replaced by CRLF the next time Git touches it

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git config --global core.autocrlf true

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git commit -a -m"上传所有文件"
[master aa5d4a0] 上传所有文件
 4 files changed, 27 insertions(+), 11 deletions(-)

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git push -u origin master
ERROR: We're doing an SSH key audit.
Reason: unverified automatically (private key found in a public repository)
Please visit https://github.com/settings/keys/89672649 to approve this key so we know it's safe.

Fingerprint:
SHA256:FTvsPTsU08e0eZg2su93J+uTMZanHiuiL7RyG7XJFwo

fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git pull --rebase origin master
error: cannot pull with rebase: You have unstaged changes.
error: Please commit or stash them.

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git remote -v
origin  git@github.com:jiaxisky/obsidianworkspace.git (fetch)
origin  git@github.com:jiaxisky/obsidianworkspace.git (push)

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git remote rm origin

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git remote add origin git@github.com:jiaxisky/learngit.git

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git add .
warning: in the working copy of '.obsidian/workspace.json', LF will be replaced by CRLF the next time Git touches it

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git push -u origin master
ERROR: We're doing an SSH key audit.
Reason: unverified automatically (private key found in a public repository)
Please visit https://github.com/settings/keys/89672649 to approve this key so we know it's safe.

Fingerprint:
SHA256:FTvsPTsU08e0eZg2su93J+uTMZanHiuiL7RyG7XJFwo

fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git remote rm origin

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$ git remote add origin git@github.com:jiaxisky/learngit.git

Administrator@SKY-2020092105 MINGW64 /d/Obsidian/document site (master)
$
