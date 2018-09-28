# alarmo

Отправка уведомлений на telegram, viber по номеру телефона (через бота).

[![Build Status](https://travis-ci.org/antirek/telegram-alert.svg?branch=master)](https://travis-ci.org/antirek/telegram-alert)

## Как работает?

Чат-бот Телеграм принимает пользователя и спрашивает у него номер телефона. Затем полученный номер и соответсвующий chat id сохраняет на сервер. Теперь мы можем отправлять уведомление на номер, сделав простой http запрос, а бот будет направлять это уведомление соответствующему пользователю в его приложение Телеграм.


## Пример запроса

`````sh

curl -X POST \
  http://localhost:3030/send/89135292926 \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -d '{"text": "Ahtung!! Текст сообщения"}'

`````  

## Установка 


> git clone https://github.com/antirek/alarmo.git

> cd alarmo

> npm install

> npm start


## Конфиг

port - порт веб-интерфейса

mongodb - параметры подключения к mongodb

telegram - настройки чат-бота телеграм, получите у @botfather

viber - настройки чат-бота viber, получите в viber



## Fast start

Используйте docker-compose.yml

