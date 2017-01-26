# 第49关 stage_lines

> You've made changes within a single file that belong to two different features, but neither of the changes are yet staged. Stage only the changes belonging to the first feature.
> 
> 你修改了一个文件的多处代码，这些代码分属于2个不同的功能，代码还没有提交到暂存区。仅提交第1个功能相关的代码到暂存区。

用 `git add` 命令可以把文件添加到暂存区，但如果你不想把文件中的全部修改都提交到暂存区，或者说你只想把文件中的部分修改提交到缓存区，那么你需要加上 `edit` 参数：

```
$ git add your-file --edit
```

这时 Git 会自动打开文本编辑器，编辑的内容就是 `git diff` 命令的结果，这时你就可以编辑2个文件之间的差异，只保留要提交到暂存区的差异，而删除不需要提交到暂存区的差异，然后保存退出，Git 就会按你编辑过的差异把相应的内容提交到暂存区。

比如本关，文件的差异为：

```
$ git diff feature.rb
diff --git a/feature.rb b/feature.rb
index 1a271e9..4a80dda 100644
--- a/feature.rb
+++ b/feature.rb
@@ -1 +1,3 @@
 this is the class of my feature
+This change belongs to the first feature
+This change belongs to the second feature
```

从最后2行可以看出，新增的代码分别对应2个不同的功能，如果我们只想提交第1个功能的代码，删除掉最后一行即可。

第49关过关画面如下：

![第49关 stage_lines](images/level-49-stage-lines.png)