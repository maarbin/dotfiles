# Dotfiles Setup Guide (macOS)

## 1. Install Apple's Command Line Tools (required for Git and Homebrew)

```bash
xcode-select --install
```

---

## 2. Clone the Dotfiles Repository into a Hidden Directory

> ⚠️ Make sure you've set up SSH access to GitHub first.

```bash
git clone git@github.com:maarbin/dotfiles.git ~/.dotfiles
```

---

## 3. Create Symlinks in the Home Directory

Link your config files from the repo to your home directory:

```bash
ln -s ~/.dotfiles/.zshrc ~/.zshrc
ln -s ~/.dotfiles/.gitconfig ~/.gitconfig
```

---

## 4. Install Homebrew and Packages from Brewfile

### Install Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Install Software from the Brewfile

```bash
brew bundle --file ~/.dotfiles/Brewfile
```

