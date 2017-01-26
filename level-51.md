# 第51关 revert
> You have committed several times but want to undo the middle commit. All commits have been pushed, so you can't change existing history.
> 
> 你提交了多次，但想取消中间的某次提交。所有提交的内容都已经推送到服务端了，所以你不能改变已有的历史。

我们曾用过修改提交历史的 `git rebase -i` 命令，用此方法可以取消多次提交中的某次提交，不过，这只是针对还没有推送到服务端的情况，如果已经提交到服务端，你就不能改变已有的历史了，只能想别的办法解决了。

Git 提供了 `revert` 工具来解决这种问题，它相当于是对某次提交的逆操作，比如你提交时新建了一个文件，那么 Git 就会创建一个删除此文件的提交。语法如下：

```
$ git revert hash-code
$ git revert hash-code --no-edit
```

其中的 hash-code 就是你要取消的提交的哈希值。第2条命令中的 `no-edit` 参数表示由系统自动生成一句提交说明，如果没有这个参数，Git 会自动调用文本编辑器请你编写提交说明。

第51关过关画面如下：

![第51关 revert](images/level-51-revert.png)