# git is useful
**Happy New Year!**
笑死
- 笑不出来了
  - 第一次修改
#总结一下上午学的一些东西
- 场景一，搞乱了工作区的一些东西，想要直接丢弃工作区的修改时。用命令`git checkout -- file`
- 场景二，当你修改了工作区的内容而且add到了暂存区，用命令`git reset HEAD file`
- 场景三，如果已经提交到了版本库当中，想要撤销本次提交。参考版本回退
  - 使用`git log`查看版本控制系统的历史记录。后面可以添加`--pretty=oneline`参数
  - 使用`git reset --hard HEAD^`表示会退到上一个版本
  - git中，`HEAD`表示当前版本，HEAD^ 表示上一个版本，HEAD^^表示上上个版本，而HEAD~100表示上100个版本
  - 使用`git reset --hard <commit id>`可以回到对应版本。
  - 使用`git reflog`查看我的每一次命令（找版本号）♪（ｖ＾＿＾）ｖ
- 添加远程库
  1. 添加远程库`git remote add origin git@server-name:path/repo-name.git` 其中`origin`是默认的习惯名
  2. 使用`git push` 命令把当前分支master推送到远程，加参数`-u`可以 把本地的master和远程master关联起来，不过似乎要把`master`改成`main`才可以。
  `git remote add origin git@github.com:michaelliao/learngit.git`
   `git push -u origin master`
  3. 之后如果本地做了提交可以使用`git push  origin master(main)`，把本地`master`分支的最新修改推送至GitHub