---
title: Hello hexo world! (002)
date: 2021-09-21 17:04:38
tags:
- hexo
- todo
---


# 修改網站資訊
## _config.yml

目前有改的，功能其實一目瞭然

```yml
title: 升字手札
subtitle: '每天進步1%，一年後變成37個自己！？'
author: wscheng
language:
- zh-tw
- en
# URL
## Set your site url here. For example, if you use GitHub Page, set url as 'https://username.github.io/project'
url: http://wscheng.github.io/hexo
```
#### TODO
之後再把這篇
1. 補上圖片，可能較好了解會呈現在網站何處
2. 目前沒看到email的欄位，之後再找找

### language
可以多個lanuage，然後調整順位，繁體中文(台灣)是zh-tw
```yml
language:
- zh-tw
- en
```

# hexo部署

官網原本第三步為
```
新增 Travis CI 到 GitHub 帳戶中。
```
是使用Travis CI，但我查了一下，發現現在Travis CI是要付費的。而Github有自己的CI了Github Actions.

* 待補完