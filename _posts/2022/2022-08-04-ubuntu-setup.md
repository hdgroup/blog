---
layout: post
title: Ubuntu Setup
categories: Tool
description: Tool
keywords: macOS,Tool
---

# zsh oh-my-zsh

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

# 解决 vi 中文乱码问题

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

```

```
