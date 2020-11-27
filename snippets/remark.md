Place your global snippets here. Each snippet is defined under a snippet name and has a scope, prefix, body and 
description. Add comma separated ids of the languages where the snippet is applicable in the scope field. If scope 
is left empty or omitted, the snippet gets applied to all languages. The prefix is what is 
used to trigger the snippet and the body will be expanded and inserted. Possible variables `are` : 
$1, $2 for tab stops, $0 for the final cursor position, and ${`1` :label}, ${`2` :another} for placeholders. 
Placeholders with the same ids are connected.
`Example` :
```
"Print to console": {
	"scope": "javascript,typescript",
	"prefix": "log",
	"body": [
		"console.log('$1');",
		"$2"
	],
	"description": "Log output to console"
}
```
`TM_SELECTED_TEXT` :当前选定的文本或空字符串；
注 :选定后通过在命令窗口点选「插入代码片段」插入。

`TM_CURRENT_LINE` :当前行的内容；

`TM_CURRENT_WORD` :光标所处单词或空字符串
`注` :所谓光标一般为文本输入处那条闪来闪去的竖线，该项可定制。单词使用 VSCode 选词（Word Wrap）器选择。你最好只用它选择英文单词，因为这个选择器明显
没有针对宽字符优化过，它甚至无法识别宽字符的标点符号。

`TM_LINE_INDEX` :行号（从零开始）；

`TM_LINE_NUMBER` :行号（从一开始）；

`TM_FILENAME` :当前文档的文件名；

`TM_FILENAME_BASE` :当前文档的文件名（不含后缀名）；

`TM_DIRECTORY` :当前文档所在目录；

`TM_FILEPATH` :当前文档的完整文件路径；

`CLIPBOARD` :当前剪贴板中内容。

> 此外，还有一些用于插入当前时间的变量，这里单独列出

`CURRENT_YEAR` : 当前年份；

`CURRENT_YEAR_SHORT` : 当前年份的后两位；

`CURRENT_MONTH` : 格式化为两位数字的当前月份，如 02；

`CURRENT_MONTH_NAME` : 当前月份的全称，如 July；

`CURRENT_MONTH_NAME_SHORT` : 当前月份的简称，如 Jul；

`CURRENT_DATE` : 当天月份第几天；

`CURRENT_DAY_NAME` : 当天周几，如 Monday；

`CURRENT_DAY_NAME_SHORT` : 当天周几的简称，如 Mon；

`CURRENT_HOUR` : 当前小时（24 小时制）；

`CURRENT_MINUTE` : 当前分钟；

`CURRENT_SECOND` : 当前秒数。

> 此外，还有一些用于插入行/块注释的变量，其将根据当前文件的语言模式
自动调整

`BLOCK_COMMENT_START` : 块注释上半段，

输出示例:

*PHP* : /*

*HTML* : <!--

`BLOCK_COMMENT_END` 块注释下半段，
输出示例:

*PHP* : */

*HTML* : -->

`LINE_COMMENT` 行注释，

输出示例:

*PHP* : //

*HTML* : \<!-- -->