# Dotfiles

You need to copy/paste these lines in your terminal. Pay attention to the code that you paste and change what need to be changed.

```bash
mkdir -p ~/dotfiles && cd dotfiles
git clone git@github.com:$GITHUB_USERNAME/dotfiles.git
```

You'll need to run the installer to install the files

⚠️ Pay attention, you need `ZSH` installed to run the next lines ⚠️

```bash
zsh install.sh
```

if git is not configured yet you can also run the git installer

```bash
zsh git_setup.sh
```
you will need to enter your git informations
