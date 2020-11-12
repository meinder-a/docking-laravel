# Docking Laravel
This project will help you setting-up a dev environment for a web app.

## Aliases
We will use custom aliases, so we don't have to write endless commands by hand.
So let's ```vim``` our ```~/.zshrc``` and add:
```
alias docker-init="git clone https://github.com/meinder-a/docking-laravel.git"
alias docker-install="docker-compose up -d --build site"
alias docker-stop="docker-compose down"
alias docker-list="docker-compose ps"

alias dpa="docker-compose run artisan"
alias dcomposer="docker-compose run composer"
alias dnpm="docker-compose run npm"
alias dphp="docker-compose run php"
```

## How2

Easy setup:
```
git clone git@github.com:meinder-a/docking-laravel.git
cd docking-laravel
docker-install
dcomposer create-project laravel/laravel ./
dnpm install && dnpm run watch --watch-poll
```

You can now visit http://localhost:8080/ and contemplate a wonderful Laravel app running on Docker.
<b>Laravel is finally docked!</b>
