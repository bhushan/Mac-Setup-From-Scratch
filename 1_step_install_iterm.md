- Install iTerm2 for mac from https://iterm2.com/

Remove Last Login info by running `touch ~/.hushlogin`
 - run `exit` command and supress closing prompt for always.

To install ohmyzsh we need to install wget first so run `brew install wget`

now install ohmyzsh by running

```bash
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

