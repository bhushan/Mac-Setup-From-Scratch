- Install alfred app from [here](https://www.alfredapp.com)
- Install Clocker app from Appstore
- GOTO => System Preferences => Trackpad => Point & Click => Check `Tap on Click`
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

Install Slack `brew install --cask slack`
