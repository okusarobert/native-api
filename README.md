artisan() {
if [ -f bin/artisan ]; then
php bin/artisan "$@"
else
php artisan "$@"
fi
}


phpunit() {
if [ -f vendor/bin/phpunit ]; then
vendor/bin/phpunit "$@"
else
phpunit "$@"
fi
}

alias serve='artisan serve'
alias tinker='artisan tinker'


# Misc PHP

t() {
if [ -f vendor/bin/phpunit ]; then
vendor/bin/phpunit "$@"
else
phpunit "$@"
fi
}
