# my-zsh-config

命令行一览

> 使用root用户

```
apt install zsh git wget -y
sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
sed -i "67 i \ \ zsh-syntax-highlighting\n\ \ zsh-autosuggestions" ~/.zshrc
```
注意：保证.zshrc文件没有被修改过，否则sed命令中的67可能无效，可以尝试使用sed命令的正则表达式功能解决

## 之前的参考说明

```
sed -i "67 i \ \ zsh-syntax-highlighting\n\ \ zsh-autosuggestions" ~/.zshrc
```
或者直接手动修改
vim ~/.zshrc

```
plugins=(
  git
  zsh-syntax-highlighting
  zsh-autosuggestions
)
```

source ~/.zshrc
