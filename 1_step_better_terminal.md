Install [iTerm2](https://iterm2.com) and run `touch ~/.hushlogin` to remove last login from terminal.

To install ohmyzsh we need to install wget first so run `brew install wget`

now install ohmyzsh by running

```bash
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

install `brew install zsh-syntax-highlighting`

add below line to your `~/.zshrc` to enable syntax highlighting

```bash
echo 'source /opt/homebrew/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh' >> ~/.zshrc
```

FONTS

Install fonts from https://github.com/powerline/fonts

Specifically install [Meslo LG L DZ Italic for Powerline](https://github.com/powerline/fonts/blob/master/Meslo%20Dotted/Meslo%20LG%20L%20DZ%20Italic%20for%20Powerline.ttf) and [Meslo LG L DZ Regular for Powerline](https://github.com/powerline/fonts/blob/master/Meslo%20Dotted/Meslo%20LG%20L%20DZ%20Regular%20for%20Powerline.ttf)

Goto Iterm preferences => Profiles => Text => Change Font to `Meslo LG L DZ for Powerline` and font size `15` and n/n to `120` (vertical spacing)
Goto Iterm preferences => Appearance => theme => select Minimal theme
Goto Iterm preferences => Profiles => General => Working Directory => set it to whatever you want, I personally set it to /users/rb/code

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



NOTE: If you messed up with iterm settings and want to revert it to default state then Delete `~/Library/Preferences/com.googlecode.iterm2.plist`
