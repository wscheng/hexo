---
title: Hello hexo world! (001)
date: 2021-09-21 15:54:17
tags:
- testhexo
- hexo
---

[TOC]
測試看看TOC會不會支援大綱，看結果是不支援，有點可惜
(evernote知道這個功能的，真的很實用的功能，可以先一覽全文的大標)
可能要再看看外掛有沒有

* 我省略掉init的部分，可以自行參考官網，因為若有npm經驗應該不難理解
<https://hexo.io/zh-tw/docs/setup>

# hexo啟動
```bash
hexo server
```
預設是跑在localhost 4000 port
剛開始就會有一篇Hello world的範例文章存在

# hexo發文
```bash
hexo new [layout] "文章標題"
```
## layout type

### draft、post
產生檔案，預設post、draft

剛看到我不太清楚draft跟post有什麼差別，是說post也就還沒發佈出去
但其實hexo new post後，文章其實就是發出去了，也就是hexo server看得到
但draft實際上還在草稿夾裡

只能說這是在local未發佈出去的階段，是處於準備post出去的階段
而在hexo整體真正發佈出去的時候，就會被發佈出去，而draft則是被留在草稿夾不會被發佈

而draft要被轉為post，看來是使用hexo publish，可能是我目前沒有要寫很多文章，還覺
得draft不太會需要使用到。若同時撰寫兩篇以上文章的時候，可能就真的會需要draft功能。
畢竟不能把還沒寫好的文章也發佈出去！

```bash
hexo publish [layout] "文章標題"
```

### page

layout使用page
會直接在根目錄夾下面再建一個資料夾，目前還不知道實際有何用處
<http://localhost:4000/hexo-page/>

## 文章資訊
```markdown
---
title: Hello hexo world
date: 2021-09-21 15:54:17
tags:
- testhexo
- hexo
---
```

### tags

值得注意的只有tags，這部分記得要用 - (dash)去加標籤。一開始我以為是用空白去分別，
結果就得到一個含有空白的標籤啦。

# hexo TODO
- 網站基礎資訊更改、hexo發佈
改網站標題，產生靜態檔案跟發佈就留給下一篇囉！
- hexo改佈景
- hexo外掛