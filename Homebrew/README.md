# Homebrew

Homebrew 是 Mac/Linux 常見的一種套件管理工具，透過 `brew` 指定來快速安裝套件。

## 安裝 Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

## 使用 Homebrew

### 安裝套件

使用 `brew install` 指令來安裝指定套件名稱，例：安裝 wget

```
brew install wget
```

### 更新套件

`brew update` 指的是更新 Homebrew 以及套件清單; `brew upgrade` 指的是升級套件清單; `brew cleanup` 則是清除暫存檔。

```
brew update && brew upgrade && brew cleanup
```

### 查詢已安裝的套件

```
brew list
```

### 搜尋套件

使用 `brew search` 加上套件名稱或關鍵字來搜尋標的套件，例：搜尋 git

```bash
brew search git
```

### 顯示套件資訊

使用 `brew info` 來顯示套件的詳細資訊，例：顯示 git 套件的明細。

```
brew info git
```

### 移除套件名稱

使用 brew uninstall 加上套件名稱或關鍵字來移除特定套件，例：移除 firefox。

```
brew uninstall firefox
```

### 顯示已安裝但已過時的套件

一般都用於要更新升級套件的場境下，提供升級依據的相關資訊。

```
brew outdated
```

# Homebrew Cask

相對於Homebrew利用 brew 指令來安裝套件，homebrew cask 則是協助快速安裝軟體。

## 安裝 Cask

```
brew tap caskroom/cask
```

## 用途

### 搜尋軟體

```
brew cask search <軟體名稱or關鍵字>
```

### 安裝軟體

```
brew cask install <軟體名稱or關鍵字>
```

### 移除軟體

```
brew cask uninstall <軟體名稱or關鍵字>
```

### 更新軟體

```
brew cask update
```

