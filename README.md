1. VirtualBox у нас уже есть. Kali Linux просто дублировал с ИБ.
2. С закрытием портов проблем не возникло, 8080 порт был открыт для доступа к сайту keycloak.
3. PostgreSQL прописана в конфигурации докера
4. файл конфигурации докера был взят от [сюда](https://github.com/keycloak/keycloak-containers/blob/main/docker-compose-examples/keycloak-postgres.yml)
5. \-
6. \-
7. Поднял докер командой `docker-compose up -d`
8. Настроил автоматическое резервное копирование моей БД через cron
9. Создал realm, client, client scope: openid, group, user, role. Выполнил Role mapping.
10. Установил и запусти insomnia. Выполнил необходимые виды запросов. Результат приложен в скриншотах ниже.

В файле Insomnia.json содержится экспортированная коллекция тестовых запросов для Insomnia.

### Get realm info
![Img1](/Screens/Get%20realm%20info.png "Get realm info")
### Get token by pass
![Img1](/Screens/Get%20token%20by%20pass.png "Get token by pass")
### Get token by refresh
![Img1](/Screens/Get%20token%20by%20refresh.png "Get token by refresh")
### Get user
![Img1](/Screens/Get%20User.png "Get user")