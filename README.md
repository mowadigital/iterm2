In terminal:

brew cask install iterm2

Exit Terminal

Open Iterm

brew install zsh

sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

brew tap caskroom/fonts

brew cask install font-hack-nerd-font

Then go to iterm preferences and change font and size

git clone https://github.com/romkatv/powerlevel10k $ZSH_CUSTOM/themes/powerlevel10k

vi ~/.zshrc

Change ZSH_THEME="powerlevel10k/powerlevel10k"

echo 'POWERLEVEL9K_MODE="nerdfont-complete"' >> ~/.zshrc
echo 'source ~/.oh-my-zsh/custom/themes/powerlevel10k/powerlevel10k.zsh-theme' >> ~/.zshrc

vi ~/.zshrc

Add these lines at the bottom:

POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(os_icon root_indicator ssh dir vcs)
POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=none
POWERLEVEL9K_PROMPT_ON_NEWLINE=true

restart iterm to see new effect
 

brew install zsh-syntax-highlighting

echo 'source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh' >> ~/.zshrc

do >ls to see hightlighted syntax

brew install zsh-autosuggestions

echo 'source /usr/local/share/zsh-autosuggestions/zsh-autosuggestions.zsh' >> ~/.zshrc

do >cd to see auto suggestion of folders

further modify prompt:

# Add a space in the first prompt
POWERLEVEL9K_MULTILINE_FIRST_PROMPT_PREFIX="╭ MOWA %f"
# Visual customisation of the second prompt line
local user_symbol="$"
if [[ $(print -P "%#") =~ "#" ]]; then
    user_symbol = "#"
fi
POWERLEVEL9K_MULTILINE_LAST_PROMPT_PREFIX="╰>>> $user_symbol >> "
