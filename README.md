# my-zsh-config

sed -i "67 i \ \ zsh-syntax-highlighting\n\ \ zsh-autosuggestions" ~/.zshrc
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
