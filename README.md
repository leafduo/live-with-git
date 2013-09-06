# Live with Git

## What's Git

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

NO.

Git is a distributed file system which is often used as DVCS.

## TL; DR

1. Commit early, commit often
2. Don't change published history

第一条出事了不慌，第二条避免挨骂。

## 3 Sections

![3 sections in git project](assets/3 sections.png)

1. working directory 就是每天修改的那些文件
2. staging area 是 add 过后还没 commit 的那部分，也叫 index，有些命令用 --cached 表示 staging area
3. repository 已经提交过的代码

## Moving status

- git add
- git commit
- git reset
- git checkout


## Don't Panic when Code is Missing

- Git doesn't lose code you already committed
- Except that `.git` has been deleted :-(
- Use `git reflog` and `git fsck`

### git-reflog

- shows what have been done recently
- alias for `git log -g --abbrev-commit --pretty=oneline`
- customizable

### git-fsck

- find dangling objects
- dangling blob, commit…
- git grep <regex> `git fsck | grep "dangling commit" | cut -d " " -f 3-`

## Don't Panic when Regression is Found

- Use `git bisect`
- Binary search which commit introduces the bug

## Find who is responsible

- `git blame`
- Ask how the code works
- Xcode integration

![git-blame-xcode-integration](assets/git-blame-xcode-integration.png)

## Rewriting history

- git rebase
- git rebase -i
- git commit --amend
- git revert
- git cherry-pick

## I have an upstream project!

### Submodule

- perfect for project you won't touch
- git submodule add
- git submodule init
- git submodule update
- git submodule update --init --recursive
- git submodule foreach git pull

### Subtree

## PM is Coming!

- git stash

## Configuration

- .gitignore
- .gitattributes
- .gitconfig
- git config

## Alias

### git-alias

- git co

### shell alias

- alias g=git
- alias gs=git status
- alias gl=git log

## Working with Gerrit

- git-review

## Internal

- blob
- commit
- tree
- tag
- branch
- remote

## Reference

Pro git

http://sethrobertson.github.io/GitBestPractices/

RTFM



git reset --hard --soft --mixed

git reflog

git alias

git rebase -i

alias g=git

zsh brach tag completion

git submodule

git lg

git review

commit often

Revision number

HEAD HEAD~1 HEAD..1

git cherry-pick

Stash

Attributes

3 areas

导入代码的时候保留历史

http://adit.io/posts/2013-08-16-five-useful-git-tips.html

git checkout --orphan YourBranchName

git remote

git subtree

git revert

git commit --amend

git submodule add

git blame

git submodule foreach