# 第54关 submodule

> You want to include the files from the following repo: `https://github.com/jackmaney/githug-include-me` into a the folder `./githug-include-me`. Do this without cloning the repo or copying the files from the repo into this repo.
> 
> 你想把 `https://github.com/jackmaney/githug-include-me` 这个仓库的代码引入到自己项目的 `./githug-include-me` 目录，这个方法不需要克隆第三方仓库，也不需要把第三方仓库的文件复制到你的项目中。

如果你想把别人的仓库代码作为自己项目一个库来使用，可以采用模块化的思路，把这个库作为模块进行管理。Git 专门提供了相应的工具，用如下命令把第三方仓库作为模块引入：

```
$ git submodule add module-url
```

其中的 module-url 就是第三方仓库的地址。

第54关过关画面如下：

![第54关 submodule](images/level-54-submodule.png)