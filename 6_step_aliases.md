```bash
touch ~/.aliases
```
copy following aliases to `.aliases` file.

```bash
alias cc="clear"
alias x="exit"
alias dump="composer dump-autoload -o"
alias watch="npm run watch"
alias gaa="git add ."
alias gst="git status"
alias gl="git log --all --decorate --oneline --graph"
alias wip="git add . && git commit -m 'WIP'"
alias push="git push"
alias wpush="git add . && git commit -m 'WIP' && git push"
alias nah="git reset --hard && git clean -df"
alias p="./vendor/bin/phpunit"
alias pf="./vendor/bin/phpunit --filter "
alias art="php artisan "
alias migrate="php artisan migrate"
alias fresh="php artisan migrate:fresh"
alias seed="php artisan migrate:fresh --seed"
alias pstorm="open -a PhpStorm "

# Opens database in applications like TablePlus
# Example 1: `db` command will check env file in its directory and grab env variables and will open that database
# Example 2: `db test` command will open test database
db() {
    if [ $# -eq 0 ]; then
        [ ! -f .env ] && {
            echo "No .env file found."
            return 0
        }

        DB_HOST=$(grep DB_HOST .env | grep -v -e '^\s*#' | cut -d '=' -f 2-)
        DB_PORT=$(grep DB_PORT .env | grep -v -e '^\s*#' | cut -d '=' -f 2-)
        DB_DATABASE=$(grep DB_DATABASE .env | grep -v -e '^\s*#' | cut -d '=' -f 2-)
        DB_USERNAME=$(grep DB_USERNAME .env | grep -v -e '^\s*#' | cut -d '=' -f 2-)
        DB_PASSWORD=$(grep DB_PASSWORD .env | grep -v -e '^\s*#' | cut -d '=' -f 2-)

        DB_URL="mysql://${DB_USERNAME}:${DB_PASSWORD}@${DB_HOST}:${DB_PORT}/${DB_DATABASE}"
    fi

    if [ $# -eq 1 ]; then
        DB_URL="mysql://127.0.0.1/$1"
    fi

    open $DB_URL
}
```
now run `echo 'source ~/.aliases' >> ~/.zshrc`

and restart terminal to aliases to take effect.
