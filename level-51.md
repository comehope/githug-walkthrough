# 第51关 find\_old\_branch

> You have been working on a branch but got distracted by a major issue and forgot the name of it. Switch back to that branch.
> 
> 你在一个分支上工作时，被分派处理一个重要的问题，可是处理完这个问题之后，你忘了刚才是在哪个分支上工作了。切换回那个分支。

这种情况确实经常发生，笨办法就是逐个进入各个分支查看日志，再回忆一下刚才的工作情景。而 Git 提供了一个工具，可以用来查看你在 Git 上的历史操作：

```
$ git reflog
894a16d HEAD@{0}: commit: commit another todo
6876e5b HEAD@{1}: checkout: moving from solve_world_hunger to kill_the_batman
324336a HEAD@{2}: commit: commit todo
6876e5b HEAD@{3}: checkout: moving from blowup_sun_for_ransom to solve_world_hunger
6876e5b HEAD@{4}: checkout: moving from kill_the_batman to blowup_sun_for_ransom
6876e5b HEAD@{5}: checkout: moving from cure_common_cold to kill_the_batman
6876e5b HEAD@{6}: commit (initial): initial commit
```

你看，不仅与文件相关的 `git commit` 操作被记录了，连你 `git checkout` 操作也都记下来了，现在，你就知道此前是怎么在各个分支之间跳转的了。

第51关过关画面如下：

![第51关 find_old_branch](images/level-51-find-old-branch.png)