## Day11

### 数字

- 数字 + `operator` + 动作（范围）
- `operator` + 数字 + 动作（范围）

* 好处：保持了连贯的撤销历史记录
* 坏处：需要先思考

示例：
`d` + 3 + `w` 删除三个单词

### 点

#### 重复上一次的修改

- 刚才进行的更新（增删改）
- 离开 insert 模式之前的全部按键操作记录

#### 删除一个单词的命令如何选择（光标在单词尾部）

- `b` + `d` + `e`
- `d` + `b` + `x`
- `d` + `i` + `w`
  > 优先选择可以使用`.`进行重复操作的命令，如`d`+`i`+`w`

#### 一键移动 一键操作

- 快速在尾部加`;`
  - `j` + `L` + `a` + `;`
  - `j` + `A` + `;` 然后就可以使用`j` + `.` + `j` 来一直自动跳转到下一行的尾部并进入 insert 模式

#### 查找手动替换

1. `/` + 要查找的词
2. `cw` + 要替换的词
3. `n` 切换到下一个位置
4. `.` 替换

#### 能够重复就不要使用次数（数字）=> 执行（`d`+`i`+`w`） 重复（`.`） 回退（`u`）
