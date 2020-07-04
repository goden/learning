## 建立 Gitlab 專案

[Gitlab](https://gitlab.com/) 是與 Github 齊名的源碼管控平台。在 Gitlab 註冊登入後即出現以下畫面。點選 **Create a project** 來進行創建新的專案。

<img src="../captures/image-20200704021215095.png" alt="image-20200704021215095" style="zoom: 50%;" />

填入必要資訊後，點選 **Create project** 建立專案。

<img src="../captures/image-20200704032427675.png" alt="image-20200704032427675" style="zoom: 67%;" />

專案創建完成

![image-20200704034022432](../captures/image-20200704034022432.png)

置頂的訊息中有 You won't be able to pull or push project code via SSH until you add an SSH key to your profile 內容，請先忽略。

## 安裝 Nuxt

### 參考文件

到 Nuxt 官網，目前官網有支援多國語系。可以從以下兩個語系來著手：

- [英文](https://nuxtjs.org/)
- [中文](https://zh.nuxtjs.org/)

開啟中文官網，點選**開始使用**

<img src="/Users/goden/Dev/GitHub/learning/captures/截圖 2020-07-04 下午6.04.28.png" alt="截圖 2020-07-04 下午6.04.28" style="zoom:50%;" />

Nuxt 官網很貼心，直接就告訴你怎麼安裝，只要按圖操作即可完成。這裡有兩個重點要說明，

* Nuxt 團隊打造了創建工具 [create-nuxt-app](https://github.com/nuxt/create-nuxt-app)。這是一套 Nuxt CLI 工具，提供 CLI 介面可以在短時間建立 Nuxt 專案。
* npx 會在安裝完 create-nuxt-app 後來創建 Nuxt 專案，然後就把 create-nuxt-app 給刪除掉。

<img src="/Users/goden/Dev/GitHub/learning/captures/image-20200704180844739-3857352.png" alt="image-20200704180844739" style="zoom:50%;" />

### 執行 npx

創建 Nuxt 專案

```bash
$ sudo npx create-nuxt-app hello-nuxt

create-nuxt-app v3.1.0
✨  Generating Nuxt.js project in hello-nuxt
? Project name: hello-nuxt
? Programming language: JavaScript
? Package manager: Npm
? UI framework: None
? Nuxt.js modules: 
? Linting tools: (Press <space> to select, <a> to toggle all, <i> to invert selection)
? Testing framework: None
? Rendering mode: Universal (SSR / SSG)
? Deployment target: Server (Node.js hosting)
? Development tools: jsconfig.json (Recommended for VS Code)

．．．．．(中間會有一大堆雜七雜八的安裝歷程)．．．．．

🎉  Successfully created project hello-nuxt

  To get started:

			cd hello-nuxt
			npm run dev

  To build & start for production:

			cd hello-nuxt
			npm run build
			npm run start
```

