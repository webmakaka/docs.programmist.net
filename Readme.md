# Исходники сайта [docs.programmist.net](https://docs.programmist.net)

<br/>

## Запустить локально с возможностью редактирования

Инсталлируете docker и docker-compose, далее:

<br/>

```shell
$ cd ~
$ mkdir -p docs.programmist.net && cd docs.programmist.net
$ git clone --depth=1 https://github.com/webmakaka/docs.programmist.net.git .
$ docker-compose up
```

<br/>

Остается в браузере подключиться к localhost:80

<br/>

## (Устарело!)

<br/>

### Запустить docs.programmist.net на своем хосте с использованием docker контейнера:

```shell
$ docker run -i -t -p 80:80 --name docs.programmist.net marley/docs.programmist.net
```

<br/>

### Как сервис

```shell
$ sudo vi /etc/systemd/system/docs.programmist.net.service
```

вставить содержимое файла docs.programmist.net.service

```shell
$ sudo systemctl enable docs.programmist.net.service
$ sudo systemctl start  docs.programmist.net.service
$ sudo systemctl status docs.programmist.net.service
```

http://localhost:4006

<br/><br/>

---

<br/>

**Marley**

Any questions in english: <a href="https://docs.programmist.net/chat/">Telegram Chat</a>  
Любые вопросы на русском: <a href="https://docs.programmist.net/chat/">Телеграм чат</a>
