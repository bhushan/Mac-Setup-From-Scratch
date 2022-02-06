- Install alfred app from [here](https://www.alfredapp.com)
- Install Clocker app from Appstore
- GOTO => System Preferences => Trackpad => Point & Click => Check `Tap on Click`
- GOTO => System Preferences => Dock & Menu Bar => Untick `Show recent applications in dock`
- Install Homebrew

Run following command in terminal to install Homebrew.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
and then run below example commands, you will see same commands in your terminal once homebrew is installed

```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/rb/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

It may take long time as it also installs xcode tools. Be ready with fast internet.

- Install Chrome Browser `brew install --cask google-chrome` set it as default.
- Install Skype `brew install --cask skype` Software if needed.

Install VSCODE `brew install --cask visual-studio-code` and PHPSTORM `brew install --cask phpstorm`

add following lines in `~/.vimrc`

```bash
inoremap jj <Esc>
set clipboard+=unnamed
```
and after that run below two commands to use same settings in ideavim (PHPStorm plugin)

```bash
touch ~/.ideavimrc
echo 'source ~/.vimrc' >> ~/.ideavimrc
```

Mapping Caps Lock to Escape key
Open System Preferences and click on 'Keyboard'
Click on 'Modifier Keys...'
For 'Caps Lock (⇪) Key', choose '⎋ Escape'
Click 'OK'

Install Slack `brew install --cask slack`
