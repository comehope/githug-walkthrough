# 第16关 log

> You will be asked for the hash of most recent commit.  You will need to investigate the logs of the repository for this.
> 
> 你将被询问最近一次提交的 hash 值，可以通过仓库日志找到它。

本关考察的是对日志查询结果的阅读能力。

每执行一次 `git commit` 命令都会在仓库里留下一个更新日志，可以通过 `git log` 命令查看历史日志，查询结果按提交时间倒序列出所有更新，每条日志包含一个40位的 hash 值、作者名字、电子邮件地址和提交日期及说明，示例如下：

```
$ git log
commit 30fef820b410142d3ded8c0908cd1dcb4c0cade0
Author: comehope <comehope@163.com>
Date:   Tue Nov 22 17:30:24 2016 +0800

    THIS IS THE COMMIT YOU ARE LOOKING FOR!
    
$ git log --pretty=oneline
411bf644d492f6106acda662612dbc627f951769 THIS IS THE COMMIT YOU ARE LOOKING FOR!
```

第2条语句增加了 ```---pretty=oneline``` 参数，表示把日志以紧凑的格式显示，每行显示一次提交，只列出提交的 hash 值和说明，便于快速查看多条日志。

第16关过关画面如下：

![第16关 log](images/level-16-log.png)