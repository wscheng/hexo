---
title: Hello hexo world! (002)
date: 2021-09-21 17:04:38
tags:
  - hexo
  - todo
---

# 修改網站資訊

## \_config.yml

目前有改的，功能其實一目瞭然

```yml
title: 升字手札
subtitle: "每天進步1%，一年後變成37個自己！？"
author: wscheng
language:
  - zh-tw
  - en
# URL
## Set your site url here. For example, if you use GitHub Page, set url as 'https://username.github.io/project'
url: http://wscheng.github.io/hexo
```

- title, subtitle 的部分(在 header)
  {% asset_img header.png %}

- author 的部分(在 footer)
  {% asset_img footer.png %}

#### TODO

之後再把這篇

1. [x] 補上圖片，可能較好了解會呈現在網站何處
2. 目前沒看到 email 的欄位，之後再找找

### language

可以多個 lanuage，然後調整順位，繁體中文(台灣)是 zh-tw

```yml
language:
  - zh-tw
  - en
```

# hexo 部署

直接使用官網的[一鍵部署](https://hexo.io/zh-tw/docs/github-pages#%E7%A7%81%E4%BA%BA%E5%84%B2%E5%AD%98%E5%BA%AB)

1. github 開一個 public 的 repository
2. \_config.yml 加入

```
deploy:
  type: git
  repo: https://github.com/wscheng/hexo
  branch: gh-pages
```

3. 執行 hexo clean && hexo deploy

```
hexo clean && hexo deploy
```
