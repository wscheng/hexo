---
title: Hello hexo world! (001)
date: 2021-09-21 15:54:17
tags:
  - testhexo
  - hexo
  - todo
---

[TOC]
測試看看 TOC 會不會支援大綱，看結果是不支援，有點可惜
(evernote 知道這個功能的，真的很實用的功能，可以先一覽全文的大標)
可能要再看看外掛有沒有

- 我省略掉 init 的部分，可以自行參考官網，因為若有 npm 經驗應該不難理解
  <https://hexo.io/zh-tw/docs/setup>

# hexo 啟動

```bash
hexo server
```

預設是跑在 localhost 4000 port
剛開始就會有一篇 Hello world 的範例文章存在

# hexo 發文

```bash
hexo new [layout] "文章標題"
```

## layout type

### draft、post

產生檔案，預設 post、draft

剛看到我不太清楚 draft 跟 post 有什麼差別，是說 post 也就還沒發佈出去
但其實 hexo new post 後，文章其實就是發出去了，也就是 hexo server 看得到
但 draft 實際上還在草稿夾裡

只能說這是在 local 未發佈出去的階段，是處於準備 post 出去的階段
而在 hexo 整體真正發佈出去的時候，就會被發佈出去，而 draft 則是被留在草稿夾不會被發佈

而 draft 要被轉為 post，看來是使用 hexo publish，可能是我目前沒有要寫很多文章，還覺
得 draft 不太會需要使用到。若同時撰寫兩篇以上文章的時候，可能就真的會需要 draft 功能。
畢竟不能把還沒寫好的文章也發佈出去！

```bash
hexo publish [layout] "文章標題"
```

### page

layout 使用 page
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

值得注意的只有 tags，這部分記得要用 - (dash)去加標籤。一開始我以為是用空白去分別，
結果就得到一個含有空白的標籤啦。

# hexo TODO

- [x] 網站基礎資訊更改、hexo 發佈
      改網站標題，產生靜態檔案跟發佈就留給下一篇囉！
- hexo 改佈景
- hexo 外掛
