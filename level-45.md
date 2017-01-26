# 第45关 squash

> You have committed several times but would like all those changes to be one commit.
> 
> 你提交过几次，但是现在想把这些提交合并成一次提交。

承上关，如果要把多次合并合并成一次提交，可以用 ```git rebase -i``` 的 ```squash``` 命令。

先查一下提交日志：

```
$ git log --pretty=oneline
55d9ec9d216767dd1e080c32f5bcff1b3c62ab5b Updating README (squash this commit into Adding README)
749b65067db05a02515c580ad8e791306ff02305 Updating README (squash this commit into Adding README)
1ac3ed61a0ae302cf76dc6f3a37e56e2b5f750f9 Updating README (squash this commit into Adding README)
606be40cc9e5c684cab87c22c37a9d0225308761 Adding README
994f2b3a2df48ef4a406a5c62b4b6f6c8c1fac03 Initial Commit
```

从查询结果看出，添加了 README 之后来又对它做了3次修改。

找到 "Adding README" 下面一条日志的哈希值 "994f2b3a2df48ef4a4"，执行 ```reabse``` 命令：

```
$ git rebase -i 994f2b3a2df48ef4a4
```

系统自动打开文本编辑器，显示历史日志：

```
pick 606be40 Adding README
pick 1ac3ed6 Updating README (squash this commit into Adding README)
pick 749b650 Updating README (squash this commit into Adding README)
pick 55d9ec9 Updating README (squash this commit into Adding README)
```

把后3条日志前面的 "pick" 命令都改成 "squash"：

```
pick 606be40 Adding README
squash 1ac3ed6 Updating README (squash this commit into Adding README)
squash 749b650 Updating README (squash this commit into Adding README)
squash 55d9ec9 Updating README (squash this commit into Adding README)
```

保存退出，系统再次自动打开编辑器，内容是合并过的更新说明：

```
# This is a combination of 4 commits.
# The first commit's message is:
Adding README

# This is the 2nd commit message:

Updating README (squash this commit into Adding README)

# This is the 3rd commit message:

Updating README (squash this commit into Adding README)

# This is the 4th commit message:

Updating README (squash this commit into Adding README)
```

你可以在此编辑合并之后的更新说明，然后保存退出。再查日志，就会发现3次 "Updating README" 的提交都合并到 "Adding README" 中了。

```
$ git log --pretty=oneline
3e8c0e3a729a9d5f959214a2267c481ff0197722 Adding README
994f2b3a2df48ef4a406a5c62b4b6f6c8c1fac03 Initial Commit
```

第45关过关画面如下：

![第45关 squash](images/level-45-squash.png)