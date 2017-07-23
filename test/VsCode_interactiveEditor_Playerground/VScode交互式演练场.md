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

### 智能感知

Visual Studio Code 的强大的智能感知来自由 `JavaScript` 与 `TypeScript` 的预安装。将文本光标放在错误下划线的前面，在点号(.)的右边按下 `keyboard` 也同样会触发智能感知系统。注意这些建议是如何从 `Request API` 出来的。

```js
var express = require('express');
var app = express();

app.get('/', function (req, res) {
    res.send(`Hello ${req.}`);
});

app.listen(3000);
```

>**提示:** 同时我们也拥有除了 `JavaScript` 和 `TypeScript` 支持之外，其他语言的支持，你可以通过扩展来更新你的智能感知系统。

### 行操作
你想在一行操作整个文本是一件很常见的事。我们同样提供了一组十分有用的快捷键来帮助你来完成这些。
1.通过操作键盘 `Ctrl+Shift+D` 拷贝光标指向的这一行并把它插入在这行下面。
2.分别通过操作键盘 `Ctrl+Shift+UpArrow` 和 `Ctrl+Shift+DownArrow` 可以进行对你选中的行上下调整操作。
3.通过操作键盘 `Ctrl+Shift+K` 可以选择删除整行。
```js
{
    "name": "John",
    "age": 31,
    "city": "New York"
}
```
>**提示:** ；另一个非常常用的任务是可以注释整段代码块，通过触发键盘 ` Ctrl+Shift+/` 。

### 重命名重构
去重新命名一个类似函数名或者变量名在这里是十分简单的。敲击 `F2` 当你需要替换掉所有有关 `Book` 的符号 - 它将会遍历在这个项目中的所有文件。你也可以在鼠标右击的下拉菜单中看到重构的选项。
```js
// Reference the function
new Book("War of the Worlds", "H G Wells");
new Book("The Martian", "Andy Weir");

/**
 * Represents a book.
 */
function Book(title, author) {
    this.title = title;
    this.author = author;
}
```
>**JSDOC 提示:** 上面的例子还展示了使用 `JSDoc` 注释获得 `IntelliSense` 提示的另一种方法。 您可以通过调用 `Book` 函数并在 `IntelliSense Experience` 中查看增强的上下文以了解函数以及参数。

### 格式化

没有一个优秀的 `formatter` 使你的代码看起来整齐美观是一件非常不容易的事。幸运的是，你可以非常容易的通过敲击 `Shift+Alt+F` 来使你的文档变得非常好看，同时，你也可以使用组合键 `Ctrl+K Ctrl+F` 使你的选中的代码块格式化。以上这两个选项都可以通过右击的下拉菜单也可以得到。
```js
var cars = ["Saab", "Volvo", "BMW"];

for (var i=0; i < cars.length; i++) {
// Drive the car
console.log(`This is the manufacturer [${cars[i]}])`);
    }
```
>**提示** 扩展程序库中提供了其他格式化程序。格式化支持也可以通过设置进行配置。 启用 `editor.formatOnSave` 。
### 代码折叠
在大文件中，通常可以将代码段折叠起来以提高可读性。 为此，您可以按 `Ctrl + Shift + [折叠代码 - 按Ctrl + Shift +]` 展开。 也可以使用左侧沟槽中的 `+/-` 图标进行折叠。 折叠所有部分 `Ctrl + K Ctrl + 0` 或展开所有 `Ctrl + K Ctrl + 0` 。
```html
<div>
    <header>
        <ul>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
        </ul>
    </header>
    <footer>
        <p></p>
    </footer>
</div>
```
>**提示** 折叠是基于缩进，因此可以应用于所有语言。 只需缩小代码以创建可折叠部分，您可以使用 `Ctrl + K Ctrl + 1` 到 `Ctrl + K Ctrl + 5` 之类的快捷方式折叠一定数量的级别。
### 错误与警告
当您编辑代码时，会出现错误和警告。 在下面的示例中，您可以看到一些语法错误。 按 `Ctrl + K N` ，您可以依次浏览它们，并查看详细的错误消息。 当您更正它们时，波形和滚动条指示器将更新。
```js
// This code has a few syntax errors
Console.log(add(1, 1.5));


function Add(a : Number, b : Number) : Int {
    return a + b;
}
```
### 块
您可以通过使用片段大大加快编辑速度。 只需从建议列表中键入 `try` 并选择 `trycatch` ，然后按 `Tab` 键创建一个 `try-> catch` 块。 您的光标将被放置在文本错误上，便于编辑。 如果存在多个参数，请按 `Tab` 键跳转到该参数。
>**提示** 扩展库包括几乎所有框架和语言可想象的扩展的片段。 您还可以创建自己的用户定义的片段。
### Emmet
`Emmet` 将片段的想法提升到一个全新的层次：您可以键入可以动态解析的类似 `CSS` 的表达式，并根据您在缩写中输入的内容生成输出。 要使用`Emmet`，只需在 `Emmet` 语法的有效段之后按 `Tab` 键即可进行扩展。 尝试通过在 `ul> li.item $ * 5` 后按 `Tab` 键查看 `Emmet` 的动作。
>**提示**：`Emmet` 作弊表是Emmet语法建议的重要来源。`Emmet`还可以通过`emmet.syntaxProfiles`设置为其他语言启用。