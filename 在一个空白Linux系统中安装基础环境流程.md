# 在一个空白Linux系统中安装基础环境流程

> 本文命令基于CentOS

## 安装zsh

```
yum install zsh -y
```

通过以下命令检查是否存在/bin/zsh

```
chsh -l
chsh -s /bin/zsh
```

## 安装git

```
yum install git -y
```

通过以下命令检查是否安装成功

```
git --version
```

## 安装ohmyzsh

```
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

```
git clone git@gist.github.com:0e7843815331e76b8442a31d74a12d7c.git zshconfig
mv ~/.zshrc ~/.zshrc.bak
mv ./zshconfig/.zshrc ~
mv ./zshconfig/.alias ~
mv ./zshconfig/.paths ~

git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
source ~/.zshrc
```

## 安装NVM

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
```

## 安装Node.js

```
nvm ls-remote
nvm install v8.10.0
nvm current
node --version
npm --version
```

## 安装Yarn

```
curl --silent --location https://dl.yarnpkg.com/rpm/yarn.repo | sudo tee /etc/yum.repos.d/yarn.repo
yum install yarn -y
yarn --version
```