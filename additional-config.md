# Run after Brewfile

When the brewfile is done running you can do the following:

## Create ssh key for github
https://docs.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account

1. Create new SSH key (Or check for existing - see url above)
`$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

1. Copy the SSH key to your clipboard
`$ pbcopy < ~/.ssh/id_rsa.pub`


## Use dotfiles from this repo
sym link files

  `ln -s ~/Documents/www/mac-setup/.dotfiles/.gitconfig ~/.gitconfig`
  `ln -s ~/Documents/www/mac-setup/.dotfiles/.zshrc ~/.zshrc`

## Setup brew autoupdate with notification
I haven't really see this working but it would be nice to keep everything up-to-date.
https://github.com/DomT4/homebrew-autoupdate
https://github.com/julienXX/terminal-notifier

`$ brew autoupdate --enable-notification`
`$ brew autoupdate --start`

## Setup ZSH theme
https://github.com/romkatv/powerlevel10k#features

`$ echo "source $(brew --prefix)/opt/powerlevel10k/powerlevel10k.zsh-theme" >>~/.zshrc`

Then type `p10k configure` to access the builtin configuration wizard.
..
