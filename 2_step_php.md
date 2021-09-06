Install latest PHP

`brew install php`

Install PHP CS FIXER
`brew install php-cs-fixer`

Setup Xdebug

check that the path is to the correct php executable, and pecl is available
`which pecl`
returns: /usr/local/opt/php@8.0/bin/pecl

install xdebug, see https://xdebug.org/docs/install#pecl
`pecl install xdebug`

check that everything worked
`php --version`
should show a xdebug version
like:  with Xdebug v3.0.4, Copyright (c) 2002-2021, by Derick Rethans


Install Composer 

`brew install composer`

and run

```bash
echo 'export PATH="$HOME/. composer/vendor/bin:$PATH"' >> ~/.zshrc
```
