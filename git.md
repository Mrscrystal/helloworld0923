# Git命令

## 常用命令

### 合并

   fast-forward 分支上没有新的提交，git会默认用此方式  不会创建新的提交
  
    git merge dev

   no-fast-foward 分支上有提交，git会在当前分支傻瓜创建新的 merging commit

    git merge dev

### 合并冲突

   出现冲突，git会展现冲突位置，手动移除不想保留的修改，然后再次添加已修改的文件，提交

     git merge dev
     git add read.md
     git commit -m '修改文件'

### 变基

   会将当前分支的提交复制到指定的分支之上

    git rebase
   变基与合并的区别：Git不会尝试确定要保留或不保留那些文件。我们执行rebase的分支总是含有我们想要保留的最新近的修改！这样我们不会遇到热河合并冲突，而且可以保留一个漂亮的、线性的Git历史记录
  
### 交互式变基

 在我们正在 rebase 的提交上，我们可以执行以下 6 个动作：

* reword：修改提交信息；
* edit：修改此提交；
* squash：将提交融合到前一个提交中；
* fixup：将提交融合到前一个提交中，不保留该提交的日志消息；
* exec：在每个提交上运行我们想要 rebase 的命令；
* drop：移除该提交。

      git rebase -i HEAD~3
      drop 记录名   //移除一个提交
  
### 重置

#### 软重置

     git reset --soft HEAD~2
     git status

#### 硬重置

     git reset --hard HEAD~2
     git status

### 还原

    git revert 记录

### 拣选

   用于我们只需要某个分支的某一个提交时

    git cherry-pick 记录

### 取回

   获取远程的修改,fetch只是单传的下载新的数据

    git fetch origin master

### 拉取

   git pull实际上时连个命令和成了一个：git fetch和git merge

    git pull origin master

### Reflog

   git reflog可以展示已经执行过的素有动作的日志。基本包括你对分支的所有修改

    git reflog

### 拉取

   git pull实际上时连个命令和成了一个：git fetch和git merge

    git pull origin master
