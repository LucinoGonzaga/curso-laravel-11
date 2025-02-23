# Curso GRATUITO de Laravel 11.x

- :movie_camera: [Acesse o Curso](https://academy.especializati.com.br/curso/laravel-11-completo-e-gratuito) | [Youtube](https://www.youtube.com/watch?v=80JFKFFIWmM&list=PLVSNL1PHDWvThyUgAgJoulpg5kB7GpYqS)


Links Úteis:

- :tada: [Saiba Mais](https://linktr.ee/especializati)

## Passo a passo para rodar o projeto
Clone o projeto

> git clone https://github.com/especializati/curso-laravel-11 laravel-11


> cd laravel-11/



Crie o Arquivo .env

> cp .env.example .env



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

> docker-compose up -d



Acesse o container

> docker-compose exec app bash



Instale as dependências do projeto

> composer install


Observação: caso você esteja usando Linux e ocorra erro indicando que o diretório vendor não existe, então basta criar o diretório na raiz do projeto (usando o vscode).


Gere a key do projeto Laravel

> php artisan key:generate


Criar tabelas no banco no mysql

> php artisan migrate


Acesse o projeto
[http://localhost:8989](http://localhost:8989)


### Aula 04 - Autenticação



> composer require laravel/breeze --dev



> php artisan breeze:install

_Obs: na instalação selecionar "Blade with Alpine"_



> npm run dev

_Obs: caso do linux permissão no dir "node_modules"_


Realizar teste

> php artisan test


### Aula 05 - Como funcionam os models e migration

#### 5.1 Acessar o container

> docker compose exec app bash


#### 5.2 Gerenciar a estrutura do banco

O comando abaixo vai criar a model "Category" e a migration "categories".

> php artisan make:model Category -m

- Boa praticas: o model deve iniciar em maiúsculo e no singular e tabelas no plural.
- Para criar o migrate adicione -m no final do comando.
- Para criar o controler adicione -c no final do comando.
- Para criar o controler e migrate adicione -mc no final do comando.
- Os modelf ficam disponiveis no diretórios "/database/migrations".
- Em caso de dúvidas consultas a [documentação](https://laravel.com/docs/11.x/migrations).


#### 5.2 Criar estrutura do banco


> php artisan migrate


Para verificar as outras opções do artisan executar o comando

> php artisan

```sh
 migrate
  migrate:fresh             Drop all tables and re-run all migrations
  migrate:install           Create the migration repository
  migrate:refresh           Reset and re-run all migrations
  migrate:reset             Rollback all database migrations
  migrate:rollback          Rollback the last database migration
  migrate:status            Show the status of each migration
```