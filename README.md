```bash
# Запущееные контейнеры
docker ps

# Все контейнеры контейнеры
docker ps  -a

# Лоакльные images (образы контайнеров)
docker images

# Скачать image (образы контайнера) nginx из докерхаба
docker pull nginx

# Создать контейнер из образа и запусить его
# https://docs.docker.com/engine/reference/commandline/run/
docker run [image]

# Запустить nginx
docker run -it -p 8080:80 --name web1 nginx

# Запустить nginx и удалить после остановки
docker run -it -p 8080:80 --name web1 nginx

# Запустить nginx в фоне
docker run -it -d -p 8080:80 --name web1 nginx

# Остановить контейнеры
docker stop [container_id]

# Удалить container
docker container -rm [ID]

# Удалить image
docker rmi [image]

# Логи контейнера
docker logs [container_id_or_name]

# Docker Hub
# Подготовка
gpg --generate-key
pass init [generated gpg-id public key]
# Авторизация
docker login
# Теги
docker tag (from)[image]:[version-tag]  (to)[username]/[image]:[version-tag]
docker tag hello-world:v1.1 idany2w/hello-world:v1.1
# Публикация
docker push [username]/[image]:[version-tag]
docker push idany2w/hello-world:v1.1

```