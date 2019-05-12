# �b Bash ���n�J username �M useremail
- git config --global user.name "username"
- git config --global user.email "name@gmail.com"

# �N�ɮפU���쥻��
- git clone https://github.com/$$$$/*****.git

## �Ĥ@���W�Ǩ� repositories �~�ݰ�
- git remote add origin https://github.com/$$$$/*****.git
- git remote add origin \<url\>
	- $$$$ is github account
	- ***** is github repository name

# ���@�ǳ]�w�ɪ��W�r�A����|�����n�ާ@
- �d�ݥثe�]�w��
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

- ���]�w��
	- vim ~/.gitconfig
```git=
[alias]
	cm = commit -m
	s = status
	l = log
	upload = push origin master
```

# �p��ާ@ git
- cd Desktop/\<filename\>/
	- �i�J�n��s/���� git �W���ɮ�
- git init . 
	- initialization
	- �N�ɮפ���l��
- git status
	- �d�ݥثe��Ƨ� git �����A
- git commit -am "\<txt\>"
	- �N�o���n commit ��������r�ǤW�h
- git add .
	- �N�ɮפ�����󳣧�s�W�h
- git push origin master
	- �N�ɮױ��W master

# ��L git �����O
- git branch
	- �d�ݥثe�� git �W�����Ǥ���
- git branch \<name\>
	- �s�W�@�ӦW�� \<name\> ����
- git checkout \<A\>
	- ������ A ����
- git checkout master
	- ���^ master ����

# ���~�ѨM worng
1. ! [rejected] master -> master (fetch first)
- git pull

2. ! [rejected] master -> master (non-fast-forward)
- git pull origin master
	- <branch master -> FETCH_HEAD>
	fatal: refusing to merge unrelated histories

- git pull origin master --allow-unrelated-histories
	- By default, git merge command refuses to merge histories that do not share a common ancestor.

