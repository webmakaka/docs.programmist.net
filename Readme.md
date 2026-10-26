# Исходники сайта [docs.programmist.info](https://docs.programmist.info)

<br/>

## Запустить локально с возможностью редактирования

Инсталлируете docker и docker-compose, далее:

<br/>

```shell
$ cd ~
$ mkdir -p docs.programmist.info && cd docs.programmist.info
$ git clone --depth=1 https://github.com/webmakaka/docs.programmist.info.git .
$ docker-compose up
```

<br/>

Остается в браузере подключиться к localhost:80

<br/>

## (Устарело!)

<br/>

### Запустить docs.programmist.info на своем хосте с использованием docker контейнера:

```shell
$ docker run -i -t -p 80:80 --name docs.programmist.info marley/docs.programmist.info
```

<br/>

### Как сервис

```shell
$ sudo vi /etc/systemd/system/docs.programmist.info.service
```

вставить содержимое файла docs.programmist.info.service

```shell
$ sudo systemctl enable docs.programmist.info.service
$ sudo systemctl start  docs.programmist.info.service
$ sudo systemctl status docs.programmist.info.service
```

http://localhost:4006

<br/><br/>

---

<br/>

**Marley**

Any questions in english: <a href="https://docs.programmist.info/chat/">Telegram Chat</a>  
Любые вопросы на русском: <a href="https://docs.programmist.info/chat/">Телеграм чат</a>
