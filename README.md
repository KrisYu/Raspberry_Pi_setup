
### SetUp

- replace Raspberry Pi source list


```
sudo vi /etc/apt/sources.list
deb http://mirrors.shu.edu.cn/raspbian/raspbian/ stretch main contrib non-free rpi
```

- install Chinese input 


```
sudo apt-get install fcitx fcitx-googlepinyin fcitx-module-cloudpinyin fcitx-sunpinyin
```

- tell which bash using


```
echo $0
```

https://stackoverflow.com/questions/3349370/how-to-tell-which-unix-shell-i-am-using


- use open command as on Mac


add this to ~/.bashrc


```
alias open = "xdg-open" 
```

https://stackoverflow.com/questions/3349370/how-to-tell-which-unix-shell-i-am-using


- shutdown Raspberry Pi

```
shutdown -r now #reboot
shutdown -h now #shutdown
```

- kill a not responding process

```
ps -a # list the running process
kill -p <pid>
```

- run commands from Python 

```
import os
os.system('your command')
```

for example, we can write a shutdown script:

shutdown script


```
#!/usr/bin/env python
import os
os.system('shutdown -h now')
```

chmod u+x shutdown.py



----------------------------------------------

### Special Habits

- remap the Alt key to Control key


```
xmodmap -e "remove mod1 = Alt_L"
xmodmap -e "add control = Alt_L"
```

Or put 


```
remove mod1 = Alt_L
add control = Alt_L
```

in `modmap.file` and then `xmodmap modmap.file`


-----------------------------------------------

### Apps

- ReText  

for markdown edit, install using `sudo apt-get install retext`

use it from Terminal : retext
or find it under Office menu

- scrot

screenshot, install using `sudo apt-get install scrot`

use if from Terminal : scrot
`scort -s` choose a rectangle to capture


-----------------------------------------------

### Git

- git clone empty repo


```
$ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
```


- git ignore files


```
touch .gitignore
# then add ignore files
```

- download single folder of github


```
# change /tree/master/ in URL to /trunk/, then use svn
svn checkout url
```


---------------------------------------------------

### Vim

- change the comment blue color 

 change the comment blue color to LightBlue for better reading


```
hi Comment ctermfg = LightBlue
```

- set autoindent to 2 spaces

```
set autoindent
set shiftwidth=2
```


add this to ~/.vimrc

- copy all file contents 


```
gg"*yG
```

https://stackoverflow.com/questions/1620018/copy-all-the-lines-to-clipboard

---------------------------------------------------

### C

- binary numbers

though standard C doesn't represent binary representaion, but in gcc it supports

```
int foo = 0b00100101;
```

https://stackoverflow.com/questions/6413956/c-represent-int-in-base-2


---------------------------------------------------

### Shell

- find file 

ls -a can list all files, but we can combine with grep, such as:


```
ls -a | grep RE
```

we can find all the files who's file name have chars 'RE' inside.

```

