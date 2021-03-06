## vim02

### vim 移动

- 移动到行首：
  - 数字键`0`
  - `^` 移动到本行第一个不是 blank 字符的位置
    > blank 字符：空格、tab、换行、回车
- 移动到行尾：
  - `$`
  - `g`+`_` 移动到本行最后一个不是 blank 字符的位置
- 默认移动快捷键不好用，这里我们修改一下
  - 在 VS Code 中按下`command` + `shift` + `p`，选择 setting.json 文件
    - 添加以下配置
    ```json
     "vim.normalModeKeyBindings":[
        {"before": ["H"], "after": ["^"]},
        {"before": ["L"], "after": ["g","_"]},
    ]
    ```
    > 注意：这里`"g"`和`"_"`的顺序不能变，把`"g"`放后面会导致映射失败

### vim 插入

- `I` 在行首插入
- `A` 在行尾插入
- `O` 在行前插入（另起一行）
- `o` 在行后插入（另起一行）

### vim 快捷操作

* `yy` 复制当前行
* `p` 粘贴
* `dd` 删除当前行

> 这里的复制粘贴与默认的`command` + `c` 或 `command` + `v`不冲突

### 在vim中修改上下左右按键

* 需要先下载一个软件：https://karabiner-elements.pqrs.org/
* 把上下左右映射为 `control` + `k`/`j`/`h`/`l`

![image](../images/Day2.png)