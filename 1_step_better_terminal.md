Install iTerm2 and run `touch ~/.hushlogin` to remove last login from terminal.

Goto iterm Preferences => Profiles => Colors and choose Solarized Dark

To install ohmyzsh we need to install wget first so run `brew install wget`

now install ohmyzsh by running

```bash
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

```text
For reference only

https://www.freecodecamp.org/news/jazz-up-your-bash-terminal-a-step-by-step-guide-with-pictures-80267554cb22/
```

Go to http://ethanschoonover.com/solarized

Scroll down and download the Theme (solarized.zip)

Extract the solarized.zip file

Open the osx-terminal.app-colors-solarized folder. This folder contains Theme for the terminal.

Double click “Solarized Dark ansi.terminal” file — This is the specific Theme file for Terminal.app. Note: If you get a warning that this is from an unidentified 

developer, Right-click on the file and select “Open with” > Terminal option.

At this point, you have the Theme installed into your Terminal. We just need to make it a default Theme.

Open Terminal > Preferences > Text and select the “Solarized Dark …” theme and click on “Default”.


Install Powerline

Install python by running `brew install python`

Install pip — A package manager for Python (similar to npm)

```bash
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py

```

```bash
python3 get-pip.py
```

now to install powerline run `pip3 install --user powerline-status`


Now you can figure out the location of Powerline by running the following: `pip3 show powerline-status` Copy the value from the `Location` field.

now paste the below code in ~/.zshrc to add powerline daemon

```bash
export PATH=$PATH:$HOME/Library/Python/3.9/bin
powerline-daemon -q
POWERLINE_BASH_CONTINUATION=1
POWERLINE_BASH_SELECT=1
. /Users/bhushan/Library/Python/3.9/lib/python/site-packages
```



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
