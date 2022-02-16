# dotfiles
## Preparations
Install oh-my-zsh: `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
Install Homebrew: `sh -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
Install Formulae: `brew install git, gnupg, gradle, jenv, nvm, podman, tldr, tree, vim, zsh-autosuggestions, zsh-syntax-highlighting`
Install Casks: `brew install 1password, clipy, font-cousine, google-chrome, intellij-idea-ce, iterm2, microsoft-teams, slack, spectacle, spotify, virtualbox, visual-studio-code, webstorm`
Clone this repo: `git clone --bare git@github.com:beerChili/dotfiles.git $HOME/.cfg`
Create config alias: `alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'`
Backup existing files: `mkdir -p .config-backup && config checkout 2>&1 | egrep "\s+\." | awk {'print $1'} | xargs -I{} mv {} .config-backup/{}`
Checkout repo: `config checkout`
Hide untracked files: `config config --local status.showUntrackedFiles no`
