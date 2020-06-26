# 移除 NodeJS

## Windows

在 Windows 安裝 NodeJS 是用安裝檔 step by step 安裝，當然移除就是直接就控制台反安裝操作。

## Linux

安裝 NodeJS 時會連帶安裝 NPM 系統。所以反安裝時也要先移除 NPM 後再移除 NodeJS

```bash
sudo npm uninstall -g npm
```

查詢 node 安裝目錄位置，先取得安裝目錄後切換至安裝目錄，假設安裝目錄為 `/path/bin/node` 

```bash
which node            // the path to install node
cd /path/bin/node     // switch to installation directory.

// remove the related installation folders.
rm -r bin/node bin/node-waf include/node lib/node lib/pkgconfig/nodejs.pc share/man/man1/node.1
```

如果當初是採用 apt-get 方式進行安裝，那麼也請直接使用 apt-get 方式來移除

```bash
sudo apt-get remove nodejs
```

## Mac OS

### Homebrew

如果是以 `brew install node` 方式來安裝，可執行以下指令。

```bash
brew uninstall node	     // remove node from system
brew doctor & brew cleanup   // remove symlinks and softlinks 
```

### 手動移除

```bash
rm -rf /usr/local/lib/node* 		  // remove node and node_modules from /usr/local/lib
rm -rf /usr/local/include/node*           // remove node and node_modules from /usr/local/include
rm -rf /usr/local/bin/node*		  // remove node, node-debug and node-gyp from /usr/local/bin
rm -rf ~/.npmrc				  // remove .npmrc which contains npm settings from home directory.  										                  // recommended to keep if you wanbt a re-installation.
rm -rf ~/.npm ~/.node-gyp ~/.node_repl_history
rm -rf /usr/local/share/man/man1/node*
rm -rf /usr/local/share/man/man1/npm*
rm -rf /usr/local/lib/dtrace/node.d
rm -rf /opt/local/bin/node /opt/local/include/node
rm -rf /opt/local/lib/node_modules
rm -rf /usr/local/share/doc/node
rm -rf /usr/local/share/systemtap/tapset/node.stp
```

網路上其它人的做法([原文](https://www.positronx.io/how-to-uninstall-node-js-and-npm-from-macos/))

```bash
cd /usr/local/include & sudo rm -R node
cd /usr/local/lib & sudo rm -R node_modules
cd /usr/local/bin & sudo rm -R node
```

回到 [NodeJS](./README.md)

回到[首面](../README.md)

