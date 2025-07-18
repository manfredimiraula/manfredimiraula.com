---
layout: post
vimeoId: 
title: Clean Python Installation on Mac with iTerm2, Pyenv & Oh My Zsh
image: "assets/posts/20200712/20200712.webp"
read_time: true
show_date: true
category: Technical Guides
description: Set up Python, pyenv, virtualenvwrapper, Jupyter, and a power terminal with iTerm2 and Oh My Zsh on a fresh MacOS. Follow this clean, no-error installation guide.
author: Manfredi Miraula
tags:
  - python installation mac
  - install python macos
  - pyenv setup mac
  - virtualenvwrapper mac
  - iterm2 customization
  - oh my zsh setup
  - clean python install mac
  - python zsh terminal
  - powerlevel9k iterm2
  - setup jupyter mac
  - python virtual environment mac
  - python development environment


---


Yes, this is yet another Python installation guide. However, it is different from most as I verified the steps and it should run smoothly without errors when you have a clean OS installation. I've used MacOS Catalina freshly installed.

How this is going to work? I'm going to give you the sequence of steps that you need to run to install Python, the virtual environment manager, Jupyter notebook and Oh My Zsh. Starting from a basic terminal ...

![Vanilla iTerm](/assets/img/posts/20200712/vanilla.png)_The Vanilla version of iTerm2_

You will obtain a poweruser terminal similar to this

![Poweruser iTerm](/assets/img/posts/20200712/poweruser.png)_The poweruser version of iTerm2_

If you are more of a visual person like I am, you can follow the video tutorial shows how to change and modify iTerm.


<center>
<br>
<a href="http://www.youtube.com/watch?feature=player_embedded&v=xrrd1aw-BXg
" target="_blank"><img src="http://img.youtube.com/vi/xrrd1aw-BXg/0.jpg" 
alt="Clean Python installation video tutorial" width="480" height="360" border="10" /></a>
<br>
</center>

<hr>

## How to install python in less than 9999 steps

To run the commands, you can copy directly the line after the "$" into your terminal.

```shell
  $ xcode-select --install
  $ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
  $ brew install python
  $ brew install pyenv
  $ echo 'eval "$(pyenv init -)"' >> .bash_profile
  $ echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
  $ echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
  $ echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.zshrc
  $ brew install zlib sqlite
  $ export LDFLAGS="-L/usr/local/opt/zlib/lib -L/usr/local/opt/sqlite/lib"
  $ export CPPFLAGS="-I/usr/local/opt/zlib/include -I/usr/local/opt/sqlite/include"
  -- here you can choose the Python version you want to install
  $ pyenv install 3.7.7
  $ pyenv global 3.7.7
  $ brew install pyenv-virtualenvwrapper
  -- no, it's not an error... keep the "$" while copying the command line
  $ $(pyenv which python3) -m pip install virtualenvwrapper
  $ echo 'export WORKON_HOME=~/.virtualenvs' >> .zshrc
  $ echo 'mkdir -p $WORKON_HOME' >> .zshrc
  $ echo '. ~/.pyenv/versions/3.7.7/bin/virtualenvwrapper.sh' >> .zshrc
```

### Basic virtual environment commands

You now have a working virtual environments ready to use. To create and activate a new virtual environment:

here change _[the_name_of_your_project]_ with the name of the folder in which you want to start your project

```shell
  $ mkdir [the_name_of_your_project]
  $ cd [the_name_of_your_project]
  $ mkvirtualenv $(basename $(pwd))
```

The last command creates a virtual environment with the name of the folder you are in and activates it. Once you are finished use

```shell
$ deactivate
```

If you want to check which environment you have create or swap between virtual environments you can use the command

```shell
$ workon
$ workon [the_name_of_my_virtual_environment]
```

## Prettyfiyng iTerm

iTerm is a more flexible and powerful Terminal than the one that comes out-of-the-box with MacOS. The following commands and steps will give you access to a beautiful and yet useful iTerm that hopefully will enhance your efficiency. If you want to follow the video guide, you can find this section at minute 7.25 [video link]

```shell
$ brew cask install iterm2
$ brew install zsh zsh-completions
$ sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
$ git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k
$ git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
$ brew install zsh-syntax-highlighting
```

Visit [iterm2colorschemes][colorscheme] and pick your favourite colour scheme. To install

iTerm → Preferences → Profiles → Colors → Color presets → Import → import the file you downloaded

Color presets → the_file_you_downloaded

Visit [github.com/powerline/fonts][powerline] to choose your favourite font. I'm using "Meslo Slashed" for this tutorial. To download the file click "View Raw".

iTerm2 → Preferences → Profiles → Text → Change Font

### Configuring iTerm plugins

To activate and configure all the plugins we installed at the beginning, we need to tinker with the configuration file. Follow the steps below to finalise the prettification!

Open the config file via terminal

```shell
$ open ~/.zshrc
```

Add the following lines to the file

1. Search for the string "ZSH_THEME = ..." and modify the line with "ZSH_THEME="powerlevel9k/powerlevel9k"
1. Search for the string plugins = (...) and add "zsh-autosuggestions" within parenthesis
1. At the end of the config file add the following lines
   1. POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(dir rbenv vcs)
   1. POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=(status root_indicator background_jobs history time)
   1. POWERLEVEL9K_PROMPT_ON_NEWLINE=true
   1. POWERLEVEL9K_MULTILINE_FIRST_PROMPT_PREFIX="%f"
   1. POWERLEVEL9K_PROMPT_ADD_NEWLINE=true
   1. POWERLEVEL9K_VCS_MODIFIED_BACKGROUND=’red’
1. source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh

## Useful resources

### xcode

[Xcode][xcode] is a fundamental developing tool for developers on Mac. Not much to add here, it is a requirement if you want to write code on your Mac

### Homebrew

[Homebrew][brew] is a package manager and personally my preferred way to install packages on a Mac. Whenever I want to explore a new python tool or a new language (e.g. ruby, node, etc.) I tend to search for installations that use Homebrew because it does the heavy lifting for us.

### Pyenv and virtualenv wrapper

Pyenv and virtualenv wrapper are two tools that work hand-in-hand to create version controlled environments for Python. By using them, we can safely initialize multiple Python environments that work independently, without impacting the MacOS Python system.

You can learn more about Pyenv [here][pyenv]. For more information regarding [virtualenvwrapper][venv] head here:

### Echo commands

[Echo][echo] commands are used to print text output and/or write text in a file. In fact, we used this command to modify the .zshrc when we installed Python. These commands are used to set the correct PATH to our user installed Python version and link our terminal so that it knows that when we call the Python environments it needs to use the one we installed, rather than the MacOS one.

### Resources for iTerm

1. Additional [user-defined][user] iTerm configuration
1. Additional configuration can be added by modifying the config file
   $ open ~/.zshrc
1. Additional [Powerlevel9k][power] configuration and attributes []

**If you find this article useful, leave a comment. I'd love to get in touch and discuss what other type of content you might be interested in!**

[colorscheme]: https://iterm2colorschemes.com/
[powerline]: https://github.com/powerline/fonts
[xcode]: https://it.wikipedia.org/wiki/Xcode
[brew]: https://en.wikipedia.org/wiki/Homebrew_(package_manager)
[pyenv]: https://github.com/pyenv/pyenv/wiki
[echo]: http://www.linfo.org/echo.html
[venv]: https://virtualenvwrapper.readthedocs.io/en/latest/index.html
[user]: https://github.com/Powerlevel9k/powerlevel9k/wiki/Show-Off-Your-Config
[power]: https://github.com/Powerlevel9k/powerlevel9k#customizing-prompt-segments
[youtube]: https://youtu.be/xrrd1aw-BXg
