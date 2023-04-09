---

layout: post
title: Ubuntu Setup
categories: Tool
description: Tool
keywords: macOS,Tool

---

# zsh oh-my-zsh
```sh
# install zsh
echo $SHELL
cat /etc/shells
apt update && apt install zsh -y
chsh -s /bin/zsh
reboot

# install oh-my-zsh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# config oh-my-zsh
vim ~/.zshrc # ZSH_THEME="bira"
source ~/.zshrc

git clone https://github.com/zsh-users/zsh-autosuggestions.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
vim ~/.zshrc # plugins=(git zsh-syntax-highlighting zsh-autosuggestions)
alias gitpull="git pull"
alias gp="git add . && git commit -m 'build' && git push
source ~/.zshrc 
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
