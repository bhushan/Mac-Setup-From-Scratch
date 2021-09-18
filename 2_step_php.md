Install latest PHP

```bash
brew install php
```

and run below command to prefer brew applications first

```bash
echo 'export PATH="/opt/homebrew/bin:$PATH"' >> ~/.zshrc
```

Install PHP CS FIXER

```bash
brew install php-cs-fixer
```

While setting up rule you can check https://gist.github.com/bhushan/e2779b2cd587aebe0dee6063e2f6cd94 here for more information.

Setup Xdebug

check that the path is to the correct php executable, and pecl is available

```bash
which pecl
```

returns: /usr/local/opt/php@8.0/bin/pecl

install xdebug, see https://xdebug.org/docs/install#pecl

```bash
pecl install xdebug
```

check that everything worked
`php --version`
should show a xdebug version
like:  with Xdebug v3.0.4, Copyright (c) 2002-2021, by Derick Rethans


Install Composer 

```bash
brew install composer
```

and run

```bash
echo 'export PATH="$HOME/.composer/vendor/bin:$PATH"' >> ~/.zshrc
```

Install Laravel Valet

```bash
composer global require laravel/valet
```

and run 

```bash
valet install
```

to install valet

