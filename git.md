# ¦b Bash ¤¤µn¤J username ©M useremail
- git config --global user.name "username"
- git config --global user.email "name@gmail.com"

# ±NÀÉ®×¤U¸ü¨ì¥»¾÷
- git clone https://github.com/$$$$/*****.git

## ²Ä¤@¦¸¤W¶Ç¨ì repositories ¤~»Ý°µ
- git remote add origin https://github.com/$$$$/*****.git
- git remote add origin <url>
	- $$$$ is github account
	- ***** is github repository name

# §ó§ï¤@¨Ç³]©wÀÉªº¦W¦r¡A¤§«á·|¥²¸û¦n¾Þ§@
- ¬d¬Ý¥Ø«e³]©wÀÉ
	- cat ~/.gitconfig
```git=
[user]
	name = kellyhu0109
	email = kellyhu0109@gmail.com
[color]
	ui = true
[alias]
	lg = log --color --graph --all --pretty=format:¿%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset¿ --abbrev-commit ¿
	co = commit
[core]
	editor = vim
```

- §ó§ï³]©wÀÉ
	- vim ~/.gitconfig
```git=
[alias]
	cm = commit -m
	s = status
	l = log
	upload = push origin master
```

# ¦p¦ó¾Þ§@ git
- cd Desktop/<filename>/
	- ¶i¤J­n§ó·s/±À¨ì git ¤WªºÀÉ®×
- git init . 
	- initialization
	- ±NÀÉ®×¤å¥óªì©l¤Æ
- git status
	- ¬d¬Ý¥Ø«e¸ê®Æ§¨ git ªºª¬ºA
- git commit -am "<txt>"
	- ±N³o¦¸­n commit ¬ö¿ýªº¤å¦r¶Ç¤W¥h
- git add .
	- ±NÀÉ®×¤ºªº¤å¥ó³£§ó·s¤W¥h
- git push origin master
	- ±NÀÉ®×±À¤W master

# ¨ä¥L git ªº«ü¥O
- git branch
	- ¬d¬Ý¥Ø«eªº git ¤W¦³­þ¨Ç¤À¤ä
- git branch <name>
	- ·s¼W¤@­Ó¦W¬° <name> ¤À¤ä
- git checkout <A>
	- ¤Á´«¨ì A ¤À¤ä
- git checkout master
	- ¤Á¦^ master ¤À¤ä

# ¿ù»~¸Ñ¨M worng
1. ! [rejected] master -> master (fetch first)
- git pull

2. ! [rejected] master -> master (non-fast-forward)
- git pull origin master
	- <branch master -> FETCH_HEAD>
	fatal: refusing to merge unrelated histories

- git pull origin master --allow-unrelated-histories
	- By default, git merge command refuses to merge histories that do not share a common ancestor.

