# 第47关 merge_squash

> Merge all commits from the long-feature-branch as a single commit.
> 
> 把名为 long-feature-branch 的分支合并到主干，把分支中的多次提交合并为主干上的一次提交。

在第38关我们曾学习过 ```merge``` 合并，它的语法是：

```
$ git merge branch-name
```

如果分支曾经提交过多次，那么用上面的语句合并之后，主干的日志也会出现多次提交记录。为了符合本关题意，把分支的多次提交合并为主干上的一次提交，要加一个 ```squash``` 参数，如下：

```
$ git merge branch-name --squash
```

如果不加 ```squash``` 参数，在合并之后系统会默默地做一个 ```commit``` 操作，而加了 ```squash``` 参数之后，不会自动 ```commit```，这时你还需要手动执行 ```commit``` 命令，并且写上提交说明。

第47关过关画面如下：

![第47关 merge_squash](images/level-47-merge-squash.png)