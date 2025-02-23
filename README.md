# Curso GRATUITO de Laravel 11.x

- :movie_camera: [Acesse o Curso](https://academy.especializati.com.br/curso/laravel-11-completo-e-gratuito) | [Youtube](https://www.youtube.com/watch?v=80JFKFFIWmM&list=PLVSNL1PHDWvThyUgAgJoulpg5kB7GpYqS)


Links Úteis:

- :tada: [Saiba Mais](https://linktr.ee/especializati)

## Passo a passo para rodar o projeto
Clone o projeto
```sh
git clone https://github.com/especializati/curso-laravel-11 laravel-11
```
```sh
cd laravel-11/
```


Crie o Arquivo .env
```sh
cp .env.example .env
```


Atualize essas variáveis de ambiente no arquivo .env
```dosini
APP_NAME="Especializa Ti"
APP_URL=http://localhost:8989

DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=nome_que_desejar_db
DB_USERNAME=nome_usuario
DB_PASSWORD=senha_aqui

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```


Suba os containers do projeto
```sh
docker-compose up -d
```


Acesse o container
```sh
docker-compose exec app bash
```


Instale as dependências do projeto
```sh
composer install
```

Observação: caso você esteja usando Linux e ocorra erro indicando que o diretório vendor não existe, então basta criar o diretório na raiz do projeto (usando o vscode).


Gere a key do projeto Laravel
```sh
php artisan key:generate
```

Criar tabelas no banco no mysql
```sh
php artisan migrate
```

Acesse o projeto
[http://localhost:8989](http://localhost:8989)


### Aula 04 - Autenticação


```sh
composer require laravel/breeze --dev
```

```sh
php artisan breeze:install
```
_Obs: na instalação selecionar "Blade with Alpine"_


```sh
npm run dev
```
_Obs: caso do linux permissão no dir "node_modules"


Realizar teste
```sh
php artisan test
```
