# WebApp_Template 專案指引

## 專案摘要
傳統 Web App 開發用「專案模版」，含：jQuery, Bootstrap 。

專案源頭起自 [Yemoan WebApp Generator](https://github.com/yeoman/generator-webapp) ，因「需求」考量，經編修而得。　

 - 編譯工具： Babel
 - 組建工具： Gulp
 - 測試工具： Mocha BDD 模式
 - JavaScript：可使用 ES2016 (ES6)

為使以下「開發作業程序」、「組建作業程序」能正常操作，請依「作業前置準備」章節內容所述，在開發機備妥應安裝之軟體套件。


---

## 開發作業程序

想在開發機觀察本專案之輸出結果；或是要以本專案當基底，開始進行程式的開發工作，請依以下所述之程序進行操作。

### （1）下載專案檔案
```
$ git clone git@github.com:AlanJui/WebApp_Template.git
```

### （2）進入專案資料夾
```
$ cd WebApp_Template
```

### （3）安裝專案所需的 NodeJS 套件
```
$ npm install
```

### （4）安裝 Web 前端所需之 JavaScript / CSS 套件
```
$ bower install
```

### （5）啟動自動編譯與瀏覽結果功能
```
$ gulp serve
```

### （6）瀏覽輸出結果
使用 Web 瀏覽器，瀏覽以下網址：
```
http://localhost:9000
```

### （7）使用編輯器／IDE工具進行開發工作
在開發過程進行之中，屬 HTML、CSS 的檔案，若有內容的變更，或是使用者做了存檔動作，Web 瀏覽器內的內容亦會隨之更新。


---


## 組建（Build）作業程序

### （1）進入專案資料夾根路徑
先進入專案資料夾的「根路徑」，再進行後續之操作。

### （2）執行組建指令
執行以下指令，組建完成的結果，將輸出放進 `dist` 目錄之中。
```
$ gulp build
```


---

## 佈署（Deploy）作業程序

### （1）完成組建作業
先完成以上「組建作業」所述之各項工作，令專案根目錄下的 `dist` ，放入已完成組建及打包的檔案，供後續的佈署使用。

### （2）複製檔案
將 `dist` 目錄之下的所有檔案複製出來。複製檔案時務必留意，因 dist 目錄之下，還有子目錄。

【範例】：
```
$ cp -r dist/* /var/www/html
```

## 佈署到 Git Page 作業程序

Git Hub 提供的 Git Page 功能，可當作「靜態 Web 伺服器」來使用。

以下的佈署作業程序，僅適用於佈署到 Gig Page 使用。

【參考資料】：

 - [Git Page 快速入門](https://pages.github.com/)
 
 - [Configuring a publishing source for GitHub Pages](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/)

### （1）進入專案資料夾根路徑
先進入專案資料夾的「根路徑」，再進行後續之操作。

### （2）執行組建指令
執行以下指令，組建完成的結果，將輸出放進 `dist` 目錄之中。
```
$ gulp build
```

### （3）佈署到 Git Page 
因為本專案在 Git Hub Repo 的設定為：「Git Page 取自 Master Branch 中 docs 目錄中的檔案」，所以，只需 `git push` 指令，即可完成佈署相關工作。
```
$ gulp push
```

---


## 作業前置準備

使用本專案的原始程式碼之前，須在開發機中，先完成以下軟體之安裝。

 - Git
 - NodeJS & NPM
 - Bower
 - Glup (gulp-cli)


---


## 參考指南

 - [Yemoan WebApp Getting Started](https://github.com/yeoman/generator-webapp/blob/master/docs/README.md)：專案常用指令操作說明

 - [Yeoman WebApp Recipes](https://github.com/yeoman/generator-webapp/blob/master/docs/recipes/README.md)：想要將其它主流技術納入（如：Less, Handlebars），卻不知從何下手時，可參考此處之說明文件。

