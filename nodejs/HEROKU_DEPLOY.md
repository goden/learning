# Prepare & Deploy

## Prepare

使用 Heroku 準備的 demo 小專案來進行 app 實際操演

```bash
$ git clone https://github.com/heroku/node-js-getting-started.git
$ cd node-js-getting-started
```

## Deploy

在 Heroku 上創建 app，此時 Heroku 會與 local git repository 建立 git 關聯。Heroku 會為 app 產生一組隨時產生的專案名稱。

```bash
$ heroku create

Creating app... done, ⬢ still-shelf-52514
https://still-shelf-52514.herokuapp.com/ | https://git.heroku.com/still-shelf-52514.git
```

將 demo 專案程式碼 push 至 Heroku 上

```bash
$ git push heroku master
枚舉物件: 522, 完成.
物件計數中: 100% (522/522), 完成.
使用 4 個執行緒進行壓縮
壓縮物件中: 100% (392/392), 完成.
寫入物件中: 100% (522/522), 239.94 KiB | 119.97 MiB/s, 完成.
總共 522 (差異 95)，復用 522 (差異 95)，重用包 0
remote: Compressing source files... done.
remote: Building source:
remote: 
remote: -----> Node.js app detected
remote:     
remote: -----> Creating runtime environment
remote:     
remote:    NPM_CONFIG_LOGLEVEL=error
remote:    NODE_ENV=production
remote:    NODE_MODULES_CACHE=true
remote:    NODE_VERBOSE=false
remote:     
remote: -----> Installing binaries
remote:    engines.node (package.json): 12.x
remote:    engines.npm (package.json):  unspecified (use default)
remote:     
remote:    Resolving node version 12.x...
remote:    Downloading and installing node 12.18.1...
remote:    Using default npm version: 6.14.5
remote:     
remote: -----> Installing dependencies
remote:    Installing node modules (package.json)
remote:     
remote:    > ejs@2.7.4 postinstall /tmp/build_214d93c0e1b094856e170b819212e7dd/node_modules/ejs
remote:    > node ./postinstall.js
remote:     
remote:    added 120 packages from 107 contributors and audited 120 packages in 4.765s
remote:     
remote:    22 packages are looking for funding
remote:     run `npm fund` for details
remote:     
remote:    found 0 vulnerabilities
remote:     
remote:     
remote: -----> Build
remote:     
remote: -----> Caching build
remote:    - node_modules
remote:     
remote: -----> Pruning devDependencies
remote:    removed 69 packages and audited 51 packages in 1.532s
remote:    found 0 vulnerabilities
remote:     
remote:     
remote: -----> Build succeeded!
remote: -----> Discovering process types
remote:    Procfile declares types -> web
remote: 
remote: -----> Compressing...
remote:    Done: 22.8M
remote: -----> Launching...
remote:    Released v3
remote:    https://still-shelf-52514.herokuapp.com/ deployed to Heroku
remote: 
remote: Verifying deploy... done.
To https://git.heroku.com/still-shelf-52514.git
 \* [new branch]   master -> master
```

