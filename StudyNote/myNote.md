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