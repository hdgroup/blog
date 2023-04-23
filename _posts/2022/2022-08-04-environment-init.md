---
layout: post
title: Environment Init
categories: Tool
description: Tool
keywords: macOS,Tool
---

# macOS

## Apps

RunCat Magnet Insomniacs  
Xcode Visual Studio Code  
iTerm  
brew

## zsh oh-my-zsh

```sh
# install oh-my-zsh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# config oh-my-zsh
vim ~/.zshrc # ZSH_THEME="bira"
source ~/.zshrc

git clone https://github.com/zsh-users/zsh-autosuggestions.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
vim ~/.zshrc # plugins=(git zsh-syntax-highlighting zsh-autosuggestions)
source ~/.zshrc 
```

## Fonts

[https://github.com/lxgw/LxgwWenKai](https://github.com/lxgw/LxgwWenKai)

## References

[https://github.com/xiaolai/apple-computer-literacy](https://github.com/xiaolai/apple-computer-literacy)

# Ubuntu

## zsh oh-my-zsh

```sh
#!/bin/bash

# Install zsh
apt update
echo "Installing zsh..."
echo $SHELL
cat /etc/shells
apt update && apt install zsh -y
chsh -s /bin/zsh

# Start zsh shell in the current terminal
exec zsh

# Install oh-my-zsh
echo "Installing oh-my-zsh..."
YES=1 sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Configure oh-my-zsh
echo "Configuring oh-my-zsh..."
sed -i 's/^ZSH_THEME=.*/ZSH_THEME="bira"/' ~/.zshrc
source ~/.zshrc

# Install zsh plugins
echo "Installing zsh plugins..."
git clone https://github.com/zsh-users/zsh-autosuggestions.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
sed -i 's/^plugins=(.*/plugins=(git zsh-syntax-highlighting zsh-autosuggestions)/' ~/.zshrc

# Add aliases
echo "Adding aliases..."
echo 'alias gitpull="git pull"' >> ~/.zshrc
echo 'alias gp="git add . && git commit -m '\''build'\'' && git push"' >> ~/.zshrc
source ~/.zshrc

echo "Initialization completed!"

sed -i 's/^#ClientAliveInterval.*/ClientAliveInterval 120/' /etc/ssh/sshd_config
sed -i 's/^#ClientAliveCountMax.*/ClientAliveCountMax 720/' /etc/ssh/sshd_config
systemctl restart ssh
```

apt-get install net-tools

## 解决 vi 中文乱码问题

vim /etc/vim/vimrc
在文件结尾处增加如下三行设置

```

set fileencodings=ucs-bom,utf-8,cp936,gb18030,big5,euc-jp,euc-kr,latin1
set fileencoding=utf-8
set encoding=utf-8

```

ssh-keygen -t ed25519 -C "hoferbao@gmail.com"

vim ~/.ssh/config

```

Host \*
AddKeysToAgent yes
IdentityFile ~/.ssh/pk

```

# Windows

## Apps

### Office365

macOS 去 App Store 搜：office365，进行下载安装即可  
windows 10、windows11 office365 官网下载地址：  
下载链接：  
[https://officecdn.microsoft.com/db/492350F6-3A01-4F97-B9C0-C7C6DDF67D60/media/zh-cn/O365ProPlusRetail.img](https://officecdn.microsoft.com/db/492350F6-3A01-4F97-B9C0-C7C6DDF67D60/media/zh-cn/O365ProPlusRetail.img)

Win 系统安装激活步骤：  
1.复制链接到浏览器地址栏下载； 2.找到下载的文件鼠标右键，有装载选择装载，没有就选择“解压到 Pro...” 3.双击 setup 开始安装； 4.安装完成后打开 word 软件，在弹出的窗口点击“我不想登录或创建帐户” 5.登录账号。

```
账号：of29611@of365.ru
密码：vSDAgYa5@-Aa-Key
```

## 激活

### win10 专业版

```
6KGHG-6QV22-47MDP-VB8GB-VQ7DM
```

激活方式：

1. 点此电脑/计算机右键-属性-拉到下面点激活或者更改产品秘钥-输入秘钥
2. 点开始菜单-设置-更新与安全-激活或者更改产品秘钥-输入秘钥

错误代码末尾 028 efd ，ee2，ee7 等代码 是网络拥堵，重复输入几次即可错误代码 1023 是打错密钥，显示 210 的错误代码是版本不对

### win11 专业版

```
6KGHG-6QV22-47MDP-VB8GB-VQ7DM
```

点开始菜单-设置-激活或者更改产品秘钥-输入秘钥  
错误代码末尾 028 efd ，ee2，ee7 等代码 是网络拥堵，重复输入几次即可错误代码 1023 是打错密钥，显示 210 的错误代码是版本不对
