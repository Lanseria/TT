## 交互式编辑器演练场
`VS Code` 这款编辑器的核心包含了许多功能。这个页面高亮了一些功能，并通过使用一些嵌入了的编辑器使你能狗尝试去使用它们。如果你需要更多这款 `VS Code` 编辑器的细节，甚至过去的更多可以参考我们的[文档](https://code.visualstudio.com/docs#vscode)

* [多光标编辑](#多光标编辑) - 块选择，出现所有选择，添加额外光标还有更多
* [智能感知](#智能感知) - 为你的代码和外部模块提供代码的助手性的语法提示和建议
* [行操作](#行操作) - 快速地移动你的行代码，使你的代码可以得到重新的排序
* [重命名重构](#重命名重构) - 在代码库中快速地重新命名符号
* [格式化](#格式化) - 使用内置地文件去选择格式，使你地代码看起来赏心悦目
* [代码折叠](#代码折叠) - 通过把无关地代码折叠使你更好地关注于你需要关注的代码
* [错误与警告](#错误与警告) - 按照你所制定的类型去显示代码中的错误与提示
* [Snippets](#Snippets) - 花费更少的敲代码时间有一套标准的代码块
* [Emmet](#Emmet) - 集成了Emmet的支持，将HTML和CSS编辑提升到一个新的水平

### 多光标编辑
使用多个光标允许您一次编辑文档的多个部分，大大提高了你的生产力。 请在下面的代码块中尝试以下操作：
1.框选择 - 按以下任何组合键 `Ctrl+Shift+Alt+DownArrow`, `Ctrl+Shift+Alt+RightArrow`, `Ctrl+Shift+Alt+UpArrow`, `Ctrl+Shift+Alt+LeftArrow` 去选择文本块, 你也可以按 `Shift+Alt` 并使用鼠标去选择相应的区块。
2.添加一个光标 - 按下 `Shift+Alt+UpArrow` 或者 `Shift+Alt+DownArrow` 去向上或向下添加一个新光标, 你也可以通过鼠标 `Alt+Click` 去添加编辑区中任何一个光标。
3.创建光标在所有出现过这个字符串的地方 - 选择一个你需要去替换的字符串，比如 `background-color` 然后按下 `Alt+F3`。现在你可以替换所有刚刚选择的字符串通过简单键入。

这只是多光标编辑的冰山一角，你可以看看 `selection menu` 和我们方便的 [键盘操作手册](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf) 去额外的练习。

```css
#p1 {background-color: #ff0000;}   /* red */
#p2 {background-color: #00ff00;}   /* green */
#p3 {background-color: #0000ff;}   /* blue */
```

> CSS 提示：你可能已经注意到在上面的CSS示例中，我们还提供了颜色色板内联，另外你如果将鼠标悬停在诸如#p1的元素上时，我们将显示它在HTML是如何显示的。关于一些特殊语言在编器辑功能上的一个简单的示例。