# Get Your Baseline

## Install `brew`

    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

Reference: https://brew.sh/

---

## Consider `zsh` (Recommended, Not Required)

Reference: https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#macos

*NOTE: Parts throughout this guide, e.g. `$PATH` updates, do assume `~/.zshrc` for simplicity - just be aware to modify as needed*

### Install `zsh`

    brew install zsh

### Set `zsh` As Default Shell

    chsh -s /usr/local/bin/zsh

---

## If You Went `zsh`, Consider `oh-my-zsh` (Recommended, Not Required)

### Install `oh-my-zsh`

Reference: https://github.com/ohmyzsh/ohmyzsh#basic-installation & https://github.com/ohmyzsh/ohmyzsh/wiki

    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

---
---

# Setting Up Python

Reference: https://opensource.com/article/19/5/python-3-default-mac#what-to-do

### Install Version Manager

    brew install pyenv

### Update Shell Path

    echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.zshrc

### Don't Forget To Source

    source ~/.zshrc

### List Python Versions Available For Installation

    pyenv install -l

### Install Python3.8.x

    pyenv install 3.8.2

### Install Python3.7.x

    pyenv install 3.7.7

### Install Python2.7.x (Necessary For Exoline)

    pyenv install 2.7.17

### Set Preferred Default(s) - (`python` References First Here)

    pyenv global 3.7.7 2.7.17

---

## Verify Configuration:

### Check `python` & `pip`

    which python
    -> /Users/elijordan/.pyenv/shims/python

    python -V
    -> Python 3.7.7

    pip -V
    -> pip 20.1.1 from /Users/elijordan/.pyenv/versions/3.7.7/lib/python3.7/site-packages/pip (python 3.7)

### Check `python3` & `pip3`

    which python3
    -> /Users/elijordan/.pyenv/shims/python3

    python3 -V
    -> Python 3.7.7

    pip3 -V
    -> pip 20.1.1 from /Users/elijordan/.pyenv/versions/3.7.7/lib/python3.7/site-packages/pip (python 3.7)

### Check `python2` & `pip2`

    which python2
    -> /Users/elijordan/.pyenv/shims/python2

    python2 -V
    -> Python 2.7.17

    pip2 -V
    -> pip 20.1.1 from /Users/elijordan/.pyenv/versions/2.7.17/lib/python2.7/site-packages/pip (python 2.7)

---

## Notes:

### Check Versions Installed Locally

    pyenv versions
    ->  system
        * 2.7.17 (set by /Users/elijordan/.pyenv/version)
        * 3.7.7 (set by /Users/elijordan/.pyenv/version)
        3.8.2

### Want to Change Directory-Level Defaut?

    pyenv local <installed-version>

### If Wanting to Virtualize... Check These Out

Reference (`venv`): https://opensource.com/article/20/4/pyenv

Reference (`virtualenvwrapper`): https://opensource.com/article/19/6/python-virtual-environments-mac

---
---

# Setting Up Ruby
Reference (-ish): https://github.com/rbenv/rbenv#installation

### Install Version Manager

    brew install rbenv ruby-build

### Update Shell Path

    echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.zshrc

### Don't Forget To Source

    source ~/.zshrc

### List Ruby Versions Available For Installation

    rbenv install -l

### Install Ruby2.7.x (Latest Available)

    rbenv install 2.7.1

### Install Ruby2.5.x (Oldest Available - Better for MuranoCLI)

    rbenv install 2.5.8

### Set Preferred Default

    rbenv global 2.7.1

---
---

# Setting Up Node
Reference: https://github.com/nvm-sh/nvm#installing-and-updating

### Install Version Manager

    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash

### Don't Forget To Source

    source ~/.zshrc

### List Node Versions Available For Installation (Note: the list is absurdly long)

    nvm ls-remote

### Install Most Recent LTS Version (Sets as Default)

    nvm install --lts

### Install Latest Version

    nvm install node

---
---

# Setting Up Some Useful Tools (For Me, Today Anyhow)

### Install `jq`

Reference: https://github.com/stedolan/jq/wiki/Installation#macos

    brew install jq

### Install `exoline`

Reference: https://github.com/exosite/exoline/#installation

    pip2 install exoline

### Install `MuranoCLI`

Reference (Private Repo): https://github.com/exosite/MuranoCLI-Deprecated#install

    rbenv global 2.5.8
    gem install MuranoCLI -v 3.2.3.beta.3

### Install `zsh-syntax-highlighting` (As `oh-my-zsh` Plugin)

Reference: https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md#oh-my-zsh

### Set Some More `oh-my-zsh` Plugins

Reference: https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins

### Replace Terminal with `iTerm2`

Reference: https://www.iterm2.com/downloads.html
