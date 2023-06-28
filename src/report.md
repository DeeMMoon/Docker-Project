## Part 1. Готовый докер

* Взять официальный докер образ с **nginx** и выкачать его при помощи `docker pull`
* Проверить наличие докер образа через `docker images`\
![d1](Screenshots/d1.jpeg)
* Запустить докер образ через `docker run -d [image_id|repository]`
* Проверить, что образ запустился через `docker ps`\
![d2](Screenshots/d2.jpeg)
* Посмотреть информацию о контейнере через `docker inspect [container_id|container_name]`
* По выводу команды определить и поместить в отчёт размер контейнера, список замапленных портов и ip контейнера\
![d3](Screenshots/d3.jpeg)
* Остановить докер образ через `docker stop [container_id|container_name]`
* Проверить, что образ остановился через `docker ps`\
![d4](Screenshots/d4.jpeg)
* Запустить докер с замапленными портами 80 и 443 на локальную машину через команду `run`
![d5](Screenshots/d5.jpeg)
* Проверить, что в браузере по адресу localhost:80 доступна стартовая страница **nginx**\
![d6](Screenshots/d6.jpeg)\
![d7](Screenshots/d7.jpeg)
* Перезапустить докер контейнер через `docker restart [container_id|container_name]`
* Проверить любым способом, что контейнер запустился
![d8](Screenshots/d8.jpeg)

## Part 2. Операции с контейнером

* Прочитать конфигурационный файл *nginx.conf* внутри докер контейнера через команду `exec`\
![d9](Screenshots/d9.jpeg)
* Создать на локальной машине файл *nginx.conf*
* Настроить в нем по пути */status* отдачу страницы статуса сервера **nginx**\
![d10](Screenshots/d10.jpeg)
* Скопировать созданный файл *nginx.conf* внутрь докер образа через команду `docker cp`
* Перезапустить nginx внутри докер образа через команду `exec`
* Проверить, что по адресу *localhost:80/status* отдается страничка со статусом сервера **nginx**\
![d11](Screenshots/d11.jpeg)
* Экспортировать контейнер в файл container.tar через команду export
* Остановить контейнер
* Удалить образ через docker rmi [image_id|repository], не удаляя перед этим контейнеры
![d12](Screenshots/d12.jpeg)
* Удалить остановленный контейнер\
![d13](Screenshots/d13.jpeg)
* Импортировать контейнер обратно через команду import
![d14](Screenshots/d14.jpeg)
* Запустить импортированный контейнер\
![d15](Screenshots/d15.jpeg)
* Проверить, что по адресу localhost:80/status отдается страничка со статусом сервера nginx\
![d16](Screenshots/d16.jpeg)\
![d17](Screenshots/d17.jpeg)
