# my-shell-config

## Fish Shell

### 安装

1.安装fish
```shell
sudo apt install curl git fish -y
curl -L https://get.oh-my.fish | fish
```

2.安装agnoster主题
```shell
sudo apt install fonts-powerline
omf install agnoster
```

3.重启终端
```shell
fish
```

4.配置生效

## Zsh Shell
命令行一览

### Ubuntu 换源中科大
```shell
sudo sed -i 's/archive.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list
sudo sed -i 's/cn.archive.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list
```

### 配置终端
> 使用root用户

```shell
sudo apt install zsh git wget curl vim -y
sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
sed -i "s/(git)/(\n\ \ git\n\ \ zsh-syntax-highlighting\n\ \ zsh-autosuggestions\n)/g" ~/.zshrc
sed -i "s/robbyrussell/bira/g" ~/.zshrc
source ~/.zshrc
```

### Install Docker

```shell
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh
```

### Install pyenv

```shell
curl https://pyenv.run | bash
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

