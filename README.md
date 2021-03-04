# learn-git

***

## Config

```
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```

## Add

`git add readme.md`

---

## Commit

`git commit -m "What you want write."`

## Diff

**查看修改内容**

`git diff readme.md`

**查看工作区和版本库里面最新版本的区别**

`git diff HEAD -- readme.md`

---



## Reset&Log

**查看历史记录**

`git log`

> `git log`命令显示从最近到最远的提交日志,如果嫌输出信息太多，看得眼花缭乱的，
>
> 可以试试加上`--pretty=oneline`参数

**带参数查看日志**

`git log --graph --pretty=oneline --abbrev-commit`

> pretty:漂亮的
>
> abbrev：缩写（abbreviation）

**查看历史版本**

`git reflog`

---



**退回**

`git reset --hard HEAD^`

*在cmd命令中，`^`是转义字符，所以要用`HEAD^^`或者`HEAD~1`*

*`--hard` 后也可以接版本ID号（只需要输入前几位数）*

---



## branch

### Create a new branch

*Create a new branch 'dev'.*

`git checkout -b dev `

**创建并进入名为dev的分支，等价于：**	

`git branch dev `

`git checkout dev`

### Look all branch

`git branch`

### Return to master

`git checkout master`

### Merge

**假设当前有分支，将其合并到master**

`git merge dev`

### Delete a branch

*删除前请回到master分支*

`git branch -d dev`

### Switch

*最新版本可用*	`git switch`	*命令切换分支*

**切换到新的dev**

`git switch -c dev`

**切换到已有的master**

`git switch master`

---

**撤销修改可用**	`git checkout -- <file>`





