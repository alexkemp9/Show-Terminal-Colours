# Show-Terminal-Colours
BASH Script to Show the 246 Colours Possible Within a Terminal

## *Basics*
This is a remarkably simple Bash script that will print to the Terminal all of the 246 colours that it is capable of showing (note: only the 1st col is 8-color `ls --colors` compatible). One value of this little utility is to select what colour you wish to deploy within `~/.dir_colors`, which is the file used to modify the display of certain filenames under ls. And thus the following will appear within ~/.bashrc:

```bash
# enable color support of ls and also add handy aliases
# 2018-03-06 db changed to system-default '~/.dir_colors' rather than '~/.dircolors'
if [ -x /usr/bin/dircolors ]; then
    test -r ~/.dir_colors && eval "$(dircolors -b ~/.dir_colors)" || eval "$(dircolors -b)"
    alias ls='ls --color=auto'
    #alias dir='dir --color=auto'
    #alias vdir='vdir --color=auto'

    alias grep='grep --color=auto'
    alias fgrep='fgrep --color=auto'
    alias egrep='egrep --color=auto'
fi
```

## *Begin*
The following will assume that you have created a dir `~/.local/sbin` within which you store the bash-file; this is to set the script as executable for current user only:

```bash
$ chmod 0700 ~/.local/sbin/showTermColours
$ la ~/.local/sbin/add_chapters
-rwx------ 1 user user 939 Apr  6  2018 /home/user/.local/sbin/showTermColours
```
And here is what it will look like when run:

![showTermColours]()
