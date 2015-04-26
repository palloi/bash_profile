bash_profile
============

This repo contains bash_profile specific, such as color control or PS1 manipulation, that can be shared with other to increase productivity.  It is suggested to link the default user file ~/.bash_profile.

Supported
============
Linux and Mac

Usage
============

1. Open and edit your file:
  vi ~/.bash_profile

2. Paste:
  git_prompt_info() {
    git symbolic-ref HEAD 2> /dev/null | sed -e 's/refs\/heads\/\(.*\)/ \(\1\)/' 2> /dev/null
  }
  
  PS1="\[\033[1;34m\]\w\[\033[1;31m\]\$(git_prompt_info)\[\033[0m\] \$(~/.rvm/bin/rvm-prompt) "

3. Save: asc and :wq
