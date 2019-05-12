# 在 Bash 中登入 username 和 useremail
- git config --global user.name "username"
- git config --global user.email "name@gmail.com"

# 將檔案下載到本機
- git clone https://github.com/$$$$/*****.git

## 第一次上傳到 repositories 才需做
- git remote add origin https://github.com/$$$$/*****.git
- git remote add origin \<url\>
	- $$$$ is github account
	- ***** is github repository name

# 更改一些設定檔的名字，之後會必較好操作
- 查看目前設定檔
	- cat ~/.gitconfig
```git=
[user]
	name = kellyhu0109
	email = kellyhu0109@gmail.com
[color]
	ui = true
[alias]
	lg = log --color --graph --all --pretty=format:?Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset?--abbrev-commit ?
	co = commit
[core]
	editor = vim
```

- 更改設定檔
	- vim ~/.gitconfig
```git=
[alias]
	cm = commit -m
	s = status
	l = log
	upload = push origin master
```

# 如何操作 git
- cd Desktop/\<filename\>/
	- 進入要更新/推到 git 上的檔案
- git init . 
	- initialization
	- 將檔案文件初始化
- git status
	- 查看目前資料夾 git 的狀態
- git commit -am "\<txt\>"
	- 將這次要 commit 紀錄的文字傳上去
- git add .
	- 將檔案內的文件都更新上去
- git push origin master
	- 將檔案推上 master

# 其他 git 的指令
- git branch
	- 查看目前的 git 上有哪些分支
- git branch \<name\>
	- 新增一個名為 \<name\> 分支
- git checkout \<A\>
	- 切換到 A 分支
- git checkout master
	- 切回 master 分支

# 錯誤解決 worng
1. ! [rejected] master -> master (fetch first)
- git pull

2. ! [rejected] master -> master (non-fast-forward)
- git pull origin master
	- <branch master -> FETCH_HEAD>
	fatal: refusing to merge unrelated histories

- git pull origin master --allow-unrelated-histories
	- By default, git merge command refuses to merge histories that do not share a common ancestor.

