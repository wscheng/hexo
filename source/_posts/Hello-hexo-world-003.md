---
title: Hello hexo world! (003)
date: 2021-10-02 14:57:33
tags:
  - hexo
  - todo
---

# 插入圖片

## 1. 圖片存放位置選擇

首先是圖片存放問題
我自己一開始是最希望可以放在 google drive，畢竟有校園的硬碟空間可用，近乎不用思考圖片空間會用完的問題。

但 google drive 其實除了空間外，其實並沒有比較好用。google drive 的問題是每個 image 的路徑不能用相對路徑直接綁起來，那等於無法直接與文章共生，而且每次生一張圖，都要自己去 copy 那個 google drive 給的 id，實在很麻煩，而且看到 url 也無法辨識這張圖可能是什麼。

因此，不如使用本地端的空間，往後真的不夠放，就自己租台網路空間吧。總不會到了一個年紀，還沒有辦法負擔一台雲端 server 的錢。相信自己！

## 2. 往後圖片存放位置變更要怎麼辦？

使用本地 image 就沒這個問題了

## 3. 如何設定

兩步驟就完成

1. \_config.yml 中的 post_asset_folder 改為 true

```yml
post_asset_folder: true
```

2. 這之後發佈的文章就都會多出一個資料夾

{% asset_img 'img_folder.png' %}

- 那已經有發佈過的呢？
  直接建個同樣檔名的 folder 就可以囉！

3. 文章內使用

```markdown
{% asset_img 'image_file_name' %}
```

- 但發現 asset_img 不太好用，因為沒辦法改變 size 以及加一些註解文字，網路上找到了 a 方法

a. 直接加 image tag，但我發現 src 的地方實際上沒這麼單純

```html
<img
  src="/asset/[your_image]"
  width="[width]"
  height="[height]"
  alt="[alternative_text]"
  title="[title]"
/>
```

Ref: <https://github.com/hexojs/hexo/issues/2175>

```html
<img src="/asset/img_foler.png" width="200" alt="圖片ALT" title="圖片標題" />
```

會顯示找不到(如下)

<img src="/asset/img_foler.png" width="200" alt="圖片ALT" title="圖片標題">

因為實際上的路徑是

```
<img src="/hexo/2021/10/02/Hello-hexo-world-003/img_folder.png" width="200" alt="圖片ALT" title="圖片標題">
```

以下成功顯示：

<img src="/hexo/2021/10/02/Hello-hexo-world-003/img_folder.png" width="200" alt="圖片ALT" title="圖片標題">

b. 看了法 a，還是覺得難用，沒想到[官網](https://hexo.io/zh-tw/docs/asset-folders#Embedding-an-image-using-markdown)就有介紹一個外掛 hexo-renderer-marked，可以讓你直接使用原始的 markdown 語法就可以加入圖片

1. 安裝外掛

```cmd
npm install hexo-renderer-marked --save
```

2. 重新啟動 hexo server
3. 文章中加入以下，但發現 markdown 語法，其實本來就沒有辦法指定圖片大小...**_WTF_**

```markdown
![圖片ALT](img_folder.png "圖片title")
```

![圖片ALT](img_folder.png "圖片 title")

## TODO

為了讓 markdown 語法可以簡單指定圖片大小，找到這篇[Hexo 中扩展 Markdown 语法设置图片的大小]<https://bobcn.github.io/2018/03/24/hexo_reset_image_size/>，看來是要多少了解 hexo 的 theme 架構以及一些 markdown parser 的觀念，剛好之後有一篇是要寫 theme 的，就留給那篇再來解決吧！

- [ ] 增加 markdown 語法支援圖片設定大小的功能
