Install latest PHP

`brew install php`

Install PHP CS FIXER
`brew install php-cs-fixer`

Setup Xdebug

check that the path is to the correct php executable, and pecl is available
`which pecl`
returns: /usr/local/opt/php@7.0/bin/pecl

install xdebug, see https://xdebug.org/docs/install#pecl
`pecl install xdebug`

check that everything worked
`php --version`
should show a xdebug version
like:  with Xdebug v2.6.0, Copyright (c) 2002-2018, by Derick Rethans
