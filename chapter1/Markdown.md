# Markdown简介

------

# Markdown

## 什么是 Markdown

Markdown 是一种方便记忆、书写的纯文本标记语言，用户可以使用这些标记符号以最小的输入代价生成极富表现力的文档：譬如您正在阅读的这份文档。
它使用简单的符号标记不同的标题，分割不同的段落，**粗体** 或者 *斜体* 某些文字，更棒的是，它还支持`高亮一段代码`、`绘制表格`等等一些高阶功能。

## Markdown 编辑器

Markdown 编辑器非常多，根据使用场景不同，大致可以分为3类：

- 平台集成：博客系统，如简书、CSDN等
- 专业软件：Mou(Mac)、MarkdownPad(Win)、Typora(多平台)、Dillinger(网页版)等
- 插件集成：有些软件本身不支持 Markdown，但可以通过插件完美兼容 Markdown 语法，如 Sublime Text、VS code等

选择顺手的、适合自己的编辑器，能大大提高码字效率。

## Markdown 简明语法手册

### 1. 斜体和粗体

使用 `*`或者`_` 和 `**`或者`__` 表示斜体和粗体。

示例：

```
这是 *斜体*
这是 _斜体_
这是 **粗体**
这是 __粗体__
_斜体**中间**加粗_
```

这是 *斜体*

这是 _斜体_

这是 **粗体**

这是 __粗体__

_斜体**中间**加粗_

### 2. 分级标题

在行首加井号表示不同级别的标题 (H1-H6)，例如：# H1, ## H2, ### H3，#### H4。

```
# 这是1个#号的标题
## 这是2个#号的标题
### 这是3个#号的标题
#### 这是4个#号的标题
##### 这是5个#号的标题
###### 这是6个#号的标题
```

示例：


# 这是1个#号的标题
## 这是2个#号的标题
### 这是3个#号的标题
#### 这是4个#号的标题
##### 这是5个#号的标题
###### 这是6个#号的标题




### 3. 外链接

使用 \[描述](链接地址) 为文字增加外链接。

示例：

`这是去往 [我的Blog](http://jarodsun.com) 的链接。`

这是去往 [我的Blog](http://jarodsun.com) 的链接。

### 4. 无序列表

使用 *，+，- 表示无序列表。

示例：

```shell
- 无序列表项 一
- 无序列表项 二
- 无序列表项 三
```

- 无序列表项 一
- 无序列表项 二
- 无序列表项 三

### 5. 有序列表

使用数字和点表示有序列表。

示例：

```shell
1. 有序列表项 一
2. 有序列表项 二
3. 有序列表项 三
```

1. 有序列表项 一
2. 有序列表项 二
3. 有序列表项 三

### 6. 文字引用

使用 > 表示文字引用。

示例：

`> 野火烧不尽，春风吹又生。`

> 野火烧不尽，春风吹又生。

### 7. 行内代码块

使用 \`代码` 表示行内代码块。

示例：

让我们聊聊 \`html`。

让我们聊聊 `html`。

### 8.  代码块

使用 `四个缩进空格`或者`tab` 表示代码块。

示例：

    public class HelloWorld {
        public static void main(String[] args) {
            System.out.println("Hello World");
        }
    }

### 9.  插入图像

使用 \!\[描述](图片链接地址) 插入图像。

示例：
`![Github](https://github.githubassets.com/images/modules/logos_page/Octocat.png)`

![Github](https://github.githubassets.com/images/modules/logos_page/Octocat.png)

### 10. 删除线

使用 ~~ 表示删除线。

~~这是一段错误的文本。~~

### 11. 加强的代码块

代码示例：Java

```java
    public class HelloWorld {
        public static void main(String[] args) {
            System.out.println("Hello World");
        }
    }
```

代码示例：Ruby

```ruby
class ArticlesController < ApplicationController

  def index
    @articles = Article.all
  end

  def show
    @article = Article.find(params[:id])
  end

  def new
    @article = Article.new
  end

  def edit
    @article = Article.find(params[:id])
  end

  def create
    @article = Article.new(article_params)

    if @article.save
      redirect_to @article
    else
      render 'new'
    end
  end

  def update
    @article = Article.find(params[:id])

    if @article.update(article_params)
      redirect_to @article
    else
      render 'edit'
    end
  end

  def destroy
    @article = Article.find(params[:id])
    @article.destroy

    redirect_to articles_path
  end

  private
    def article_params
      params.require(:article).permit(:title, :text)
    end
end

```

### 12. 表格支持

```
| 项目        | 价格   |  数量  |
| --------   | -----:  | :----:  |
| Java     | \$160 |   5     |
| PHP        |   \$120   |   12   |
| Javascript        |    \$210    |  23  |

```

| 项目        | 价格   |  数量  |
| --------   | -----:  | :----:  |
| 计算机     | \$1600 |   5     |
| 手机        |   \$12   |   12   |
| 管线        |    \$1    |  234  |

### 13.分隔线
使用三个或多个星号、中划线、下划线创建分隔线：

示例：
```
三个或更多...
--- ---
中划线
***
星号
___
下划线
```
三个或更多...

--- ---

中划线

***

星号

___

下划线

### X. Html 标签

如果上面的语法还不能满足你，甚至可以在 Markdown 语法中嵌套 Html 标签。
HTML中的Markdown语法不会**解析**。
譬如，你可以用 Html 写一个纵跨两行的表格：

    <table>
        <tr>
            <th rowspan="2">值班人员</th>
            <th>星期一</th>
            <th>星期二</th>
            <th>星期三</th>
        </tr>
        <tr>
            <td>李强</td>
            <td>张**</td>
            <td>王*</td>
        </tr>
    </table>


<table>
    <tr>
        <th rowspan="2">值班人员</th>
        <th>星期一</th>
        <th>星期二</th>
        <th>星期三</th>
    </tr>
    <tr>
        <td>李强</td>
        <td>张明</td>
        <td>王平</td>
    </tr>
</table>

### I. 忽略Markdown格式

如果需要忽略Markdown格式，也就是转义Markdown的关键字，只需要在Markdown关键字前使用反斜杠 \ 即可。

示例：

`我不想让\*\*星号被解析\*\*，下划线 \_和下划线\_ 中的文字也不需要处理。`

我不想让\*\*星号被解析\*\*，下划线 \_和下划线\_ 中的文字也不需要处理。
