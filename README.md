1. Install Apple's CLI, which are prerequisites for Git and Homebrew
xcode-select --install

2. Clone repo into new hidden directory
# After setting up SSH
git clone git@github.com:maarbin/dotfiles.git ~/.dotfiles

3.Create symlinks in the Home directory to the real files in the repo.
ln -s ~/.dotfiles/.zshrc ~/.zshrc
ln -s ~/.dotfiles/.gitconfig ~/.gitconfig

4. Install Homebrew, followed by the software listed in the Brewfile
# Install Homebrew
/bin/bash -c "$curl -fsSL https://raw.githubercontent.com/Homebrew/install/HEAD/install.sh)"

# Pass Brewfile location
brew bundle --file ~/.dotfiles/Brewfile

