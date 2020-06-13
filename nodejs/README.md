# NodeJS

基於 Chrome V8 engine 打造而成的 javascript runtime.

官網：https://nodejs.org/zh-tw/

NodeJS可區分為LTS與Current版本：

- **LTS**，**L**ong-**T**erm **S**upport。官方長期維謢的穩定版，建議大家採用LTS版本。(目前最新版本為**12.18.0**)
- **Current**，屬於嘗鮮版本，新功能可於此版出現。

## 安裝

下載網址：https://nodejs.org/zh-tw/download/

目前支援 Windows、Mac 與 Linux 版本。如果對 NodeJS有多版本的需求，可以參考以下章節來了解NVM的安裝方式與使用方式。

## NVM

**N**odeJS **V**ersion **M**anager，NodeJS 版本管理系統。支援管理個人主機上的所有NodeJS版本，安裝NVM即是為了管理不同版本的NodeJS。

### 各平台安裝方式

#### Mac

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```

​		或

```bash
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```

Mac 安裝後的畫面如下：

![image-20200613142405760](captures/image-20200613142405760.png)

#### Windows

可以至Windows NVM的github專案 ([windows-nvm](https://github.com/coreybutler/nvm-windows/releases)) 下載套新版本

