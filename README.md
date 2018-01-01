# command_line_linux
Liste commande line utils for linux


<p> liste all file in directory and sort by size</p>

> find ./movies -type f  -print0 | xargs -0 du -kh | sort -rn

