---
layout: post
title: "My bashrc github Settings"
date: 2015-05-15 13:39:00
categories: my settings
---
{% highlight sh %}
. ~/.git-prompt.sh

PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[1;35m\]$(__git_ps1 "(%s)")\[\033[00m\]\$ '

alias gm='git commit -a -m '
alias gc='git checkout'
alias gpd='git pull origin develop'
alias gd='gc develop'
alias gffs='git flow feature start'
alias gp='git push'
alias gthis='git rev-parse --abbrev-ref HEAD'
alias gpushthis='git push origin `gthis`'
alias gpullthis='git pull origin `gthis`'
{% endhighlight %}
