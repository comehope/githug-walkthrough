# 附录B Linux 常用命令

在命令行环境下使用 Git 时，除了执行 Git 命令，还要操作文件和目录，以下是常用的 Linux 命令：

### 查看文件

> ls

### 查看隐藏文件

> ls -a

### 建目录

> mkdir name

### 删除目录

> rmdir name

不能删除非空目录

### 删除非空目录

> rm -rf dir-name

### 移动文件/目录，也可用于文件/目录改名

> mv source target

### 复制文件或目录

> cp source target

### 查看文本文件内容

> cat your-file-name.txt

### 从文本文件中搜索文本

> grep 'TODO' \*
>
> grep 'TODO' app.rb