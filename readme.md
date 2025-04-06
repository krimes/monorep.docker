# Настройка

## Переключение конфига для запуска nginx без сертификата (первичный запуск)
Строку в docker-compose/
`      - ./nginx/nginx.conf:/etc/nginx/nginx.conf:ro` 
поменять на 
`      - ./nginx/nginx.conf1:/etc/nginx/nginx.conf:ro` 

## Запуск nginx 
`docker-compose up nginx --build -d`

## Запуск бота для получение сертификата 
`docker-compose up certbot --build`

## Переключение конфига для запуска nginx с сертификатом
Строку в docker-compose/
`      - ./nginx/nginx.conf1:/etc/nginx/nginx.conf:ro` 
поменять на 
`      - ./nginx/nginx.conf:/etc/nginx/nginx.conf:ro` 

## Запуск nginx 
`docker-compose up nginx --build -d`

## Запуск backend 
`docker-compose up backend --build -d`
