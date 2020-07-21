# Introduction

-------------------

这是gitbook首页。

gitbook默认主题，自带三种样式 `White/Sepia/Night`

在外部，加入了`styles/website.css`，目的是更改gitbook默认的主题中`Night`样式的配色。

使用Solarized配色方案，覆盖了`Night`样式，和默认主题`style.css`中的一些颜色配置。

在book.json中加入使用外部css的配置。

```json
"styles": {
  "website": "styles/website.css"
},
```

具体修改的内容，可以直接查看`website.css`中的代码。

为了配合`Solarized`配色，加入了代码高亮的插件 `prism` 。

```json
"plugins":[
  "prism"
]

```

以及`prism`的配置，同样使用了`Solarized`

```json
"pluginsConfig": {
      "prism": {
          "css": [
              "prismjs/themes/prism-solarizedlight.css"
          ]
      }
}

```

**book.json中内容说明**

```json
{
  "title":"Discovery Unlimited",
  "author": "Jarod Sun",
  "links": {
        "sidebar": {
            "Website": "http://jarodsun.com"
        }
  },
  "plugins":[
    "hide-element",//隐藏gitbook的链接
    "fontsettings",//默认主题中，调整样式的插件
    "search",//默认搜索
    "prism",//添加的代码高亮插件，为了可以使用Solarized配色
    "-highlight",//要使用上面的高亮插件，要屏蔽默认的高亮插件
    "theme-default"//默认主题
  ],
  "styles": {
    "website": "styles/website.css"//引入自建的css样式
  },
  "pluginsConfig": {
        "hide-element": {
            "elements": [".gitbook-link"]//隐藏掉那个链接，看着清爽一些
        },
        "theme-default": {
              "showLevel": false//其实这行可有可无
        },
        "prism": {
            "css": [
                "prismjs/themes/prism-solarizedlight.css"//引入Solarized的高亮配色
            ]
        }
  }
}

```
