# 關於 RM_will-jekyll-template

這個專案是源自於 willianjusten 的 will-jekyll-template, 由於此專案已經停止維護, 所以我將其 fork 過來, 並加入了一些 javascript 工具, 以下的說明僅適用於 Linux 或 Mac, Windows 暫時沒有說明, 如果喜歡這個 Jekyll 部落格主題, 歡迎前往原專案給顆 star

## 事前準備

1. 安裝 Ruby

```console
sudo apt install ruby
```

2. 安裝 Jekyll

```console
sudo gem install jekyll
```

3. 安裝 NodeJS

```console
sudo apt install node
```

4. 安裝 Gulp (注意版本不得超過 3.9.1, 不然會出錯)

```console
sudo npm install -g gulp@3.9.1
```

## 部落格設定

1. 依照下方的註解填寫 _config.yml

```xml
# Site settings
title: # 部落格名稱
description: # 部落格簡介
baseurl: "" # 部落格位置 (可留白)
url: "" # 部落格網址

# User settings
username: # 作者名稱
user_description: # 作者自述
user_title: # 首頁自述
email: # 電子郵件
twitter_username: # twitter 使用者名稱
github_username: # github 使用者名稱
```

### 範例

```xml
# Site settings
title: 我的部落格
description: 紀錄生活的部落格
baseurl: ""
url: "https://t6y4sun.github.io"

# User settings
username: sun
user_description: 住在火星, 目前在 NASA 工作
user_title: 歡迎來到我的部落格
email: t6u4sun@gmail.com
twitter_username: t6u4sun
github_username: t6u4sun
```

### 設定作者的照片

更改 assets/img/blog-author.jpg

### 部落格 icon

更改 assets/img/icons 裡的 favico.ico, favicon-16x16.ico

### 部落格主題參數

src/styl/_variables.styl

### 更改的檔案

1. src/js/simpleJekyllSearch.js

第 4 行
```js
jsonFile        : 'https://你的使用者名稱.github.io/search.json',
```

解說: 讓搜尋功能運作

2. _includes/footer.html

第 2 行
```html
<p>此部落格為 <a href="https://github.com/你的使用者名稱" target="_blank">你的使用者名稱</a> 擁有</p>
```

解說: 更改部落格的 footer

# 建立文章

以下指令可以建立一篇新的文章

```console
./initpost.sh -c 文章名稱
```

# 注意事項

about.html 需要自己編輯, 可能會需要基本的 HTML 知識, 請斟酌編輯

# 最終! build 你的部落格!

1. cd 到您的部落格位置

```console
cd yourblog/
```

2. 安裝 node 插件 (只有第一次需要執行)

```console
npm install
```

__可能會有許多 warning, 無須理會__

3. 執行 gulp

```console
gulp
```
