# Install Z SH

[这里查看如何安装](https://www.geeksforgeeks.org/how-to-install-z-shellzsh-on-linux/)

```
# 打印当前使用的shell
echo $SHELL

```

# Oh My ZSH

[这里查看如何安装](https://zhuanlan.zhihu.com/p/35283688)


# mkdir & 目录

创建多层目录
```
# -p 实现多层创建
mkdir -p [path]
```

# Tree Commond

用来查看目录结构
```
# 查询结果像是这样
➜  Desktop tree ~
/home/trent
├── Desktop
│   ├── example-3
│   └── hello
│       └── my
│           └── world
├── demo.sh
├── trent_proj
│   ├── abc.py
│   └── hello.py
└── trent_temp

```

# Less Head & tail

```
# less 分页查看


# 只想看前十行
head query.sql


# 只想看最后十行
tail query.sql
```

# cp (copy)


# find

```
# 查找指定名称的文件/目录
## . 目录地址
## -type 搜索的类型,f:文件，d:目录...
## -iname 文件名搜索关键字,加i代表忽略大小写
find ./ -type f -iname "query*.sql"

# 查找空目录
find ~ -type d -empty

# 查找空文件
find ~ -type f -empty

# 查找空目录&空文件
find ~ -empty
```

# grep

```
# 在指定目录查询包含指定字符（支持正则表达）的文件

grep -r "END" ~/Desktop # 在Desktop目录下查询含有“END”字符串的文件


grep -rni "Customer" . # 在当前目录下查询含有“Customer”字符串的文件，-rni，r：查询目录需要，n:显示所在文件的行号，i:忽略大小写


grep -rni -A 1 -B 2 "customer980" ./Desktop # 在Desktop目录下查询含有customer980字符串的文件，输出此行且输出该行的前两行和后一行

grep "customer980" # 查找含有customer980的文件
```

# 其他有用命令

history
```
history # 打印最近执行命令

!100 # 根据打印的命令输入序号，将历史命令复制到命令输入区
```


