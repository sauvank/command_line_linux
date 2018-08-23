# command_line_linux
Liste commande line utils for linux


<p> liste all file in directory and sort by size</p>

>  du -ah Path/folder | grep -i '.avi\\|.mkv\\|.mp4' |sort -hr > movie_sort_by_size.log


## change_background_auto

### create your file

> exemple : change.bash

### insert into : 

<pre><code>
#!/bin/bash
# Wallpaper's directory.
dir="PATH_TO_THE_DIR_CONTENT_PICTURE"
# export DBUS_SESSION_BUS_ADDRESS environment variable
PID=$(pgrep gnome-session)
export DBUS_SESSION_BUS_ADDRESS=$(grep -z DBUS_SESSION_BUS_ADDRESS /proc/$PID/environ|cut -d= -f2-)
# Random wallpaper.
random="$(find $dir -maxdepth 1 -type f | shuf -n1)"
# Change wallpaper.
gsettings set org.gnome.desktop.background picture-uri "file://$random"
</code></pre>

### in the terminal

$ crontab -e

### edit your contab

*/1 * * * * PATH_TO_THE_FILE_BASH

> */1 = run every 1 minute
