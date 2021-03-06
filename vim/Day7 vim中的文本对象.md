## vim07

### vim 中的文本对象

文本是结构化的，可以快速选择

### vim 文本对象用法

- 操作符（operator） + （内部`i` / 外部`a`） + 文本对象
- 可视化模式 + （内部`i` / 外部`a`）+ 文本对象

### vim 文本对象

- `w` 一个单词
- `(`或`)` 一对()
- `b` 一对()

* `[`或`]` 一对[]
* `{`或`}` 一对{}
* `B` 一对块{}
* `<`或`>` 一对<>
* `t` XML 标签
* `'` 一对'
* `"` 一对"
* ``` 一对`
* `s` 一个句子（以`.`，`!`或`?`结尾的语句）
* `p` 一个段落  

### vim 文本对象实践示例

- `v` + `i` + `b` 选中括号里面的内容
- `v` + `i` + `(` 选中括号里面的内容（包含括号）
- `d` + `i` + `b` 删除括号里面的内容
* `v` + `i` + `w` 选中当前单词

### vim-textobj-arguments
* `i` + `a` 不包含分隔符
* `a` + `a` 包含分隔符

#### 实践技巧

* `d` + `a` + `a` 删除一个参数
* `c` + `i` + `a` 修改一个参数

### vim-textobj-entire

* `d` + `a` + `e` 删除当前文本所有内容
* `d` + `i` + `e` 删除当前文本所有内容，但是不包含前面和后面的空格

