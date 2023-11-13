# Looking for a way to spice up your shell experience? Look no further!

#### It should not be used in a real environment, unless you want to ruin your system and your life.

# .bash_profile
## ------- ALIASES -------
#### Commit and push with a single uninterrupted command, because you're a busy person. Upstream be damned.
`alias git-yolo='git commit --no-verify && git push --force'`
#### If you exit the shell shut the whole system down. You're done here, go home.
`alias exit="shutdown -h now"`
`alias quit="shutdown -h now"`
#### If you want to edit a file, you should have to learn vi first.
`alias nano='vi'`
#### Backup all deleted files to your home directory. You never know when you might need them. Never delete anything again. Ever.
`alias rm='mv --backup=/home/$(whoami)/.Trash'`

## ------- ENVIRONMENT -------
#### Nothing should come between you all and my code. Not even a firewall. Flush it.
`iptables -F`
#### Never see another permission denied error again!
`chmod -R 777 /`
#### Disable the "man" aka SELinux from constantly watching you.
`setenforce 0`
#### Sick of having to add new directories to your path? Just add them all.
`export PATH=$(find / -type d -not -path '*/\.*' 2>/dev/null | tr '\n' ':' | sed 's/:*$//'):$PATH`

## ------- PASSWORDS -------
#### Change the root password to password
`echo "root:password" | chpasswd`
#### Login to mysql as root without a password.
`mysql -u root --skip-grant-tables`


