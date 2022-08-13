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

# vim

```
:set number # 显示行号

:syntax on/off # 高亮语法开关

```

光标移动
```
J: 向下一行
K: 向上一行
L: 向左移动
H: 向右移动

W: 左移一个单词
B: 往回移动一个单词

0：去行首(含行首空格)
^: 去行头部，第一个字符处
$：去行尾

gg:到文件第一行
G：到文件最后一行
line_num + gg: 跳转到指定行

```

INSERT MODE
```

u: 撤销刚才的编辑内容
ctrl+r: 撤销后再次恢复撤销的内容

i: 进入insert模式，从当前字符前开始
a: 进入insert模式，从当前字符后开始
o: 进入insert模式，在当前所在行下一行新建插入
O: 进入insert模式，在当前所在行上一行新建插入
shift+a: 进入insert模式，在当前行的尾部开始插入内容

```

Delete Cut and Paste

```
dw: 删除单词
dd: 删除行

number+dd: 一次删除number行，从当前所在行开始
 
dG: 从当前行开始，删错后面的所有行

db: 删除前一个单词，或者从此单词所在位置删除单词前面的字符，如，hello，my friend. 此时贯标如果在 i db删除的就是 fr, 此时贯标如果在 f ,删除的就是 my
d0: 从当前光标开始删除此行光标前所有
d$: 从当前光标开始删除此行光标后所有

# 粘贴
# dlete后的内容保存在缓存区，此时该内容可用来粘贴
p: 粘贴

```

Save
```
no info
```

Search and Replace
```

```



小插曲：vim注释的蓝色字体看不清楚如何解决
[见这里](https://blog.csdn.net/weixin_30256901/article/details/99657016)
> 
```
vi ~/.vimrc 加入如下内容
hi comment ctermfg =darkyellow
```


