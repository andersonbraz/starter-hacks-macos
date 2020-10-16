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
brew tap kitsuyui/homebrew-myip
brew install myip
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