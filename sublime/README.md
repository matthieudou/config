# Sublime Text 3 user config

You'll first need to install [Sublime Text 3] (https://www.sublimetext.com/3) from the web and after that you'll need to copy-paste the following lines in your terminal.

> ⚠️⚠️⚠️ You first need to download the whole config file in Dropbox or adapt these lines
⚠️⚠️⚠️ you will not be able to remove the config file after this since the user config is only linked to dropbox.

### On Mac
```
cd ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/
rm -r User
ln -s ~/Dropbox/Sublime/User
```

### On Linux
```
cd ~/.config/sublime-text-3/Packages/
rm -r User
ln -s ~/Dropbox/Sublime/User
```

### On Windows

```
cd "$env:appdata\Sublime Text 3\Packages\"
rmdir -recurse User
cmd /c mklink /D User $env:userprofile\Dropbox\Sublime\User
```
