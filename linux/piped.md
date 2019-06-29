# 管道符

## 管道符
> 管道命令符 | 的作用是将前一个目录的标准输出当做后一个命令的标准输入，格式为命令A | 命令B
	
	例：
		cat abc.txt|grep 'css'

## 输出重定向与输入重定向

- 标准输入：默认为键盘输入，为0时表示从其他文件或者目录的输出。
- 标准输出：默认输出到屏幕，为1时表示为文件
- 错误输出：默认输出到屏幕，为2时表示是文件

### 输出重定向
|符号|作用|
|:--:|:--:|
|命令 > 文件|将标准输出重定向到一个文件中(清空原有的文件数据)|
|命令 2> 文件|将错误输出重定向到一个文件中(清空原有的文件数据)|
|命令 >> 文件|将标准输出重定向到一个文件中(追加到原有文件内容的后面)|
|命令 2>> 文件|将错误输出重定向到一个文件中(追加到原有文件内容的后面)|
|命令 >> 文件 2>$1|将标准输出与错误输出共同写入到文件中（追加到原有内容的后面）|

### 输入重定向

|符号|作用|
|:--:|:--:|
|命令 < 文件|将文件作为命令的标准输入|
|命令 << 分解符|从标准输入中读入，知道遇到”分界符”才停止|
|命令 < 文件1 > 文件2|将文件1作为命令的标准输入并将标准输出到文件2|
