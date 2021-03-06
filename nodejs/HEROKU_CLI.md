# 組態設定

## Heroku CLI

Heroku CLI 可用來部署管理 app，檢視 app 運作情況。Heroku CLI 需要先安裝 Git, 參考以下連結：

- [Git Installation](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Git Learning](../git/README.md) 

**Mac OS**

透過[安裝檔](https://cli-assets.heroku.com/heroku.pkg)或`brew install`方式安裝 Heroku CLI

```bash
$ brew install heroku/brew/heroku
```

**Windows**

- [64 bits 安裝檔](https://cli-assets.heroku.com/heroku-x64.exe)
- [32 bits 安裝檔](https://cli-assets.heroku.com/heroku-x86.exe)

**Linux**

```bash
$ sudo snap install heroku --classic
```

## 登入 Heroku 

登入 heroku CLI 會要求開啟瀏覽器來進行登入程序。

```bash
$ heroku login
heroku: Press any key to open up the browser to login or q to exit
Open browser to https://cli-auth.heroku.com/auth/cli/browser/42be1a4e-a3c9-48f2-8751-4bab1d5fc3dc
Logging in... done
Logged in as me@example.com
```

登入成功後，取得正常使用 CLI

<img src="captures/image-20200628203653706.png" alt="image-20200628203653706" style="zoom:50%;" />

 當然也能只透過命令列就完成登入程序，CLI 會將 email 與 API token 儲存在 `~/.netrc` 中。

```bash
$ heroku login -i
```