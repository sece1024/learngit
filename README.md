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

[git创建新分支 - 明明一颗大白菜 - 博客园 (cnblogs.com)](https://www.cnblogs.com/mmykdbc/p/9076063.html)

### Create a new branch

*Create a new branch 'dev'.*

`git checkout -b dev `

**创建并进入名为dev的分支，等价于：**	

`git branch dev `

`git checkout dev`

### Look all branch

`git branch`

查看所有分支

`git branch -a`

### Return to master

`git checkout master`

### Merge

**假设当前有分支，将其合并到master**

`git merge dev`

### Delete a branch

*删除前请回到master分支*

删除本地已合并分支：

`git branch -d dev`

使用参数`-D`删除本地未合并分支



**删除服务器远端的分支：**

`git push origin -delete dev`

### Switch

*最新版本可用*	`git switch`	*命令切换分支*

**切换到新的dev**

`git switch -c dev`

**切换到已有的master**

`git switch master`

---

**撤销修改可用**	`git checkout -- <file>`

### push/pull to/from origin

`git push origin dev` | dev是分支名

`git pull origin dev`



## Origin



**查看远程库**

`git remote`

**查看远程库详细信息**

`git remote -v`

---



### Push & Pull

`git pull`



`git push` -d 





## Clone

* clone包含子模块的代码仓库

` git clone --recurse-submodules https://github.com/xxxxx.git`

git clone --recurse-submodules https://github.com.cnpmjs.org/Ewenwan/ShiYanLou.git

# server

[云服务器git（详解在阿里云上搭建自己的git服务器） - 开心学习 (studyofnet.com)](http://studyofnet.com/news/2867.html)