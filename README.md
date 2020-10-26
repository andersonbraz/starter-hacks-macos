# Starter Hacks macOS

My notes about starting macOS.

## Change ComputerName and LocalHostName

### Check Name
```
scutil --get ComputerName
scutil --get LocalHostName
```

### Set New Name
```
scutil --set ComputerName
scutil --set LocalHostName
```

## Install Google Fonts

In this section, I’ll show you how to fresh install all Google Fonts on macOS. After you finished this, you’ll be able to use the Fonts in any applications.

First, open Terminal app. It’s located at /Applications/Utilities/Terminal.app. After a Terminal window appeared, copy and paste following snippet, then press enter.

```
cd ~/Library/Fonts/
```

This will change your working directory to ~/Library/Fonts. This is the default installation path for user fonts on macOS.

The next step is to download all Google Fonts git repository. Copy and paste following snippet to your terminal window, then press enter.

```
git clone https://github.com/google/fonts.git google-fonts
```

### References

[https://github.com/google/fonts](https://github.com/google/fonts)

---

## Install Homebrew

Command:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

This will change your working directory to ~/Library/Fonts. This is the default installation path for user fonts on macOS.

The next step is to download all Google Fonts git repository. Copy and paste following snippet to your terminal window, then press enter.

```
brew install wget
brew install htop
brew install pyenv
```

### References

[https://brew.sh/index_pt-br](https://brew.sh/index_pt-br)


## Install Jenv to Manage Multiple Java Version

Manage your Java environment


### Step 01 - Install

```
brew install jenv
```

### Step 02 - Settings BASH

```
sudo echo 'export PATH="$HOME/.jenv/bin:$PATH"' >> ~/.bash_profile
sudo echo 'eval "$(jenv init -)"' >> ~/.bash_profile
```

### OR Settings ZSH

```
sudo echo 'export PATH="$HOME/.jenv/bin:$PATH"' >> ~/.zshrc
sudo echo 'eval "$(jenv init -)"' >> ~/.zshrc
```

### References

[https://www.jenv.be/](https://www.jenv.be/)

## Deactive Creation Files .DS_Store

```
defaults write com.apple.desktopservices DSDontWriteNetworkStores true
```

## Delete Files .DS_Store

```
find /Volumes/<<LOCAL>>/ -name ".DS_Store" -exec rm -v {} \;
```

## The Quick Guide (TL;DR) to Get Node.js Installed using nvm

Here's the abbreviated guide, highlighting the major steps:

Download the nvm install script via cURL:

```shell
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash
```

Ensure that nvm was installed correctly with nvm --version, which should return the version of nvm installed.

Install the version of Node.js you want

Install the latest version with:

```shell
nvm install node
```

Use the latest version with:

```shell
nvm use node
```

Install the latest LTS version with 

```shell
nvm install --lts
```

Use the latest LTS verison with 

```shell
nvm use --lts
```
