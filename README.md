# my-zsh-config

命令行一览

> 使用root用户

```
apt install zsh git wget -y
sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
sed -i "s/(git)/(\n\ \ git\n\ \ zsh-syntax-highlighting\n\ \ zsh-autosuggestions\n)/g" ~/.zshrc
source ~/.zshrc
```

### 注意

保证.zshrc文件没有被修改过，否则sed命令中可能无效

```
plugins=(
  git
  zsh-syntax-highlighting
  zsh-autosuggestions
  )
```
