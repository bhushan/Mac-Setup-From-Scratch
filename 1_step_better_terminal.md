Install iTerm2 and run `touch ~/.hushlogin` to remove last login from terminal.

Goto iterm Preferences => Profiles => Colors and choose Solarized Dark

To install ohmyzsh we need to install wget first so run `brew install wget`

now install ohmyzsh by running

```bash
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```



Oh My Zsh auto suggestions
Clone this repository into $ZSH_CUSTOM/plugins (by default ~/.oh-my-zsh/custom/plugins)

git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
Add the plugin to the list of plugins for Oh My Zsh to load (inside ~/.zshrc):

plugins=(zsh-autosuggestions)
Start a new terminal session.

install `brew install zsh-syntax-highlighting`

FONTS

Install fonts from https://github.com/powerline/fonts

Specifically install `Meslo LG L DZ Italic for Powerline` and `Meslo LG L DZ Regular for Powerline`

Goto Iterm preferences => Profiles => Text => Change Font to `Meslo LG L DZ for Powerline` and font size `15` and n/n to `120` (vertical spacing)


To remove the username and host from the prompt, modify:
```
sudo vim ~/.oh-my-zsh/themes/agnoster.zsh-theme
```

to

```
## Main prompt
build_prompt() {
  RETVAL=$?
  prompt_status
  prompt_virtualenv
  prompt_aws
  #prompt_context
  prompt_dir
  prompt_git
  prompt_bzr
  prompt_hg
  prompt_end
}
```
