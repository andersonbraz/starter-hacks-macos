# Starter Hacks macOS

My notes about starting macOS.

## Installing Google Fonts

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

