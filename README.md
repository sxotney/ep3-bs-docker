# ep3-bs on docker

based on lamp stack https://github.com/jcavat/docker-lamp

## setup

0. get ep3-bs `git submodule init`
1. copy .env.example to .env and add your mail settings
2. build `docker-compose build`
3. run `docker-compose up`

Open web browser [http://localhost:8001](http://localhost:8001)

### file structure

- `app` - ep3-bs repository as a git submodule
- `install` – customized config files that get copied over the original files
- `volumes` - persistent files mounted by docker, created at first run. all your important files, including the database, are here.
- `.env.example` - example for runtime variables .env

### phpmyadmin

Enable phpmyadmin by disabling the comments in docker-compose.yml. 
Open phpmyadmin at [http://localhost:8000](http://localhost:8000)

Run mysql client:

- `docker-compose exec db mysql -u root -p` 

