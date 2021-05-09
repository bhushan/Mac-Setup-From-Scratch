Instead of using node, I work on many different projects so i prefer using nvm instead

`brew install nvm`


You should create NVM's working directory if it doesn't exist:

  `mkdir ~/.nvm`

Add the following to `~/.zshrc` or your desired shell
configuration file:

```
  export NVM_DIR="$HOME/.nvm"
  [ -s "/usr/local/opt/nvm/nvm.sh" ] && . "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
  [ -s "/usr/local/opt/nvm/etc/bash_completion.d/nvm" ] && . "/usr/local/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion
```


then

`nvm install node` ==> get latest node version
`nvm use node` ==> to use latest node

`nvm install {node version}` => to install specific node version
`nvm use {node version}` ==> to use specific node
