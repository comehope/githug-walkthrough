# 第53关 conflict

> You need to merge mybranch into the current branch (master). But there may be some incorrect changes in mybranch which may cause conflicts. Solve any merge-conflicts you come across and finish the merge.
> 
> 你要把名为 mybranch 的分支合并到当前分支 master 中，但是可能有些地方的修改会引起冲突。请解决冲突，完成合并。

在第38关我们学习过 `git merge` 命令，但在工作中难免会发生合并冲突。发生冲突的原因是合并分支与被合并分支都修改了同一个文件的同一行代码，此时 Git 系统要求你介入，决定是保留你的代码还是别人的代码，或者都保留下来。

当发生冲突时，Git 会给出以下提示：

```
$ git merge mybranch
Auto-merging poem.txt
CONFLICT (content): Merge conflict in poem.txt
Automatic merge failed; fix conflicts and then commit the result.
```

以上信息告诉你自动合并失败，需要你手动解决冲突并提交修改后的结果。在本关中，是一个名为 poem.txt 的文件的第2行代码发生了冲突。

这时你可以编辑有冲突的文件，文件内容如下：

```
Humpty dumpty
<<<<<<< HEAD
Categorized shoes by color
=======
Sat on a wall
>>>>>>> mybranch
Humpty dumpty
Had a great fall
```

其中7个左尖括号 `<<<<<<<` 和7个右尖括号 `>>>>>>>` 之间的区域是冲突的部分，而中间的7个等号 `=======` 则把有冲突的代码分开，上部分是你的代码（通常是主线代码），下部分是别人的代码（通常是开发分支的代码）。编辑这部分内容，保留你想要的，删除你不要的，保存退出，再单独提交这个文件即可。

第53关过关画面如下：

![第53关 conflict](images/level-53-conflict.png)