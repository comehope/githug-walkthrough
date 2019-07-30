# 第43关 cherry-pick

> Your new feature isn't worth the time and you're going to delete it. But it has one commit that fills in `README` file, and you want this commit to be on the master as well.
> 
> 你在新功能上的努力白废了，准备删除掉它，但是往 'README' 文件里填充内容的那次提交还有用，你要把这次提交合并到主线上。

如果你创建了一个分支，在其中进行了多次提交，而在合并时不想把分支上所有的提交都合并到主线，只想选取其中的1个提交合并到主线，那么你可以用下面的命令：

```
$ git cherry-pick hash-code
```

其中 hash-code 是某次提交生成的 HASH 值。cherry-pick 直译就是摘樱桃，把一个分支想象成一棵树，多次提交就让树上结满了果实，那么 cherry-pick 命令就是摘下其中的一个果实。

第43关过关画面如下：

![第43关 cherry-pick](images/level-43-cherry-pick.png)