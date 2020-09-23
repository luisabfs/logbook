## [TIP] Add a shell script to Ubuntu launcher

1. Go to `autostart/` folder in *.config* or create one if it not exists:

```bash
$ cd ~/.config/autostart/
// or
$ cd ~/.config
$ mkdir autostart
$ cd autostart/
```

2. Now add the following file with the name `yourScript.sh.desktop`: 

```bash
[Desktop Entry]
Type=Application
Exec="/Your/location/to/theScript/yourScript.sh"
Hidden=false
NoDisplay=false
X-GNOME-Autostart-enabled=true
Name[en_IN]=AnyNameYouWish
Name=AnyNameYouWish
Comment[en_IN]=AnyComment
Comment=AnyComment
```

[Link 1](https://askubuntu.com/questions/598195/how-to-add-a-script-to-startup-applications-from-the-command-line) | 
[Link 2](https://unix.stackexchange.com/questions/497173/how-to-automatically-start-rescuetime-on-startup-tried-crontab-and-rc-local)

