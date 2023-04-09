---
layout: post
title: macOS Setup
categories: Tool
description: Tool
keywords: macOS,Tool
---

# Apps
RunCat Magnet Insomniacs  
Xcode Visual Studio Code  
iTerm  
brew  

# zsh oh-my-zsh
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

# Fonts
[https://github.com/lxgw/LxgwWenKai](https://github.com/lxgw/LxgwWenKai)


# References
[https://github.com/xiaolai/apple-computer-literacy](https://github.com/xiaolai/apple-computer-literacy)  
