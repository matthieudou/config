# Instructions

> This file is directly inspired from [lewagon/setup](https://github.com/lewagon/setup/blob/master/OSX.md)

Take whatever you want to take, zsh or everything else.

## Installing ZSH

Using `ZSH` instead of `Bash`

```bash
curl -L http://install.ohmyz.sh | sh
```

You'll need to see this at the end.
```bash
         __                                     __
  ____  / /_     ____ ___  __  __   ____  _____/ /_
 / __ \/ __ \   / __ `__ \/ / / /  /_  / / ___/ __ \
/ /_/ / / / /  / / / / / / /_/ /    / /_(__  ) / / /
\____/_/ /_/  /_/ /_/ /_/\__, /    /___/____/_/ /_/
                        /____/                       ....is now installed!
```

please restart the terminal after this.

> You can import iTerm preferences in the folder iTerm2


## Github

Generating a SSH key is something important to authenticate you on GitHub and others like Heroku

Open a terminal and type this, replacing the email with yours (the same one you used to create your GitHub account). It will prompt for information. Just press enter until it asks for a passphrase.

```bash
mkdir -p ~/.ssh && ssh-keygen -t rsa -C "your_email@example.com"
```

You will need to provide your public SSH key to GitHub

```bash
cat ~/.ssh/id_rsa.pub
```

It will show your public key in the terminal. After that you will need to add this key on [GitHub](https://github.com/settings/keys)

You can check if it worked

```bash
ssh -T git@github.com
```

Should return you something like this

```bash
# Hi --------! You've successfully authenticated, but GitHub does not provide shell access
```

## Ruby with some useful gems

### Ruby

First, let's clean ruby...

```bash
rvm implode && sudo rm -rf ~/.rvm
# If you got "zsh: command not found: rvm", carry on. It means `rvm` is not
# on your computer, that's what we want!

sudo rm -rf $HOME/.rbenv /usr/local/rbenv /opt/rbenv /usr/local/opt/rbenv
```

Now let's get `rbenv` and `ruby-build` packages from Homebrew, they'll be useful.
```bash
brew uninstall --force rbenv ruby-build
unset RBENV_ROOT && source ~/.zshrc
brew install rbenv ruby-build && source ~/.zshrc
```

after that you can install a proper version of ruby

```bash
rbenv install 2.3.3
```
> Replace 2.3.3 with the version that you want to download

Set this version to default

```bash
rbenv global 2.3.3
```
> Same as above, replace 2.3.3 with the version that you just installed

Check your ruby version
```bash
ruby -v
```

### Gems 💎

Some useful gems...
> You can add some gems if you want. Just separate with a space

```bash
gem install bundler rspec rubocop pry pry-byebug hub colored gist
```


