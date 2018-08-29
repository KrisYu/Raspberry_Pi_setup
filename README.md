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


----------------------------------------------

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

 


