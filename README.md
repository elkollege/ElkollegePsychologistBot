# ElkollegePsychologistBot

#### Telegram-бот для оказания психологической помощи в ЭК

---

## Оглавление

- [Контакты](#контакты)
    - [Связь с разработчиком](#связь-с-разработчиком)
    - [Прочие ссылки](#прочие-ссылки)
- [Сборка и запуск](#сборка-и-запуск)
    - [Необходимые компоненты](#необходимые-компоненты)
    - [.env](#env)
    - [config.ini](#configini)
        - [Раздел `Settings`](#раздел-settings)
    - [Docker](#docker)

---

## Контакты

#### Связь с разработчиком

- [Telegram для связи](https://t.me/diquoks)
- [Почта для связи](mailto:diquoks@yandex.ru)

#### Прочие ссылки

- [Telegram-канал с новостями](https://t.me/diquoks_channel)

---

## Сборка и запуск

### Необходимые компоненты

- [Docker Desktop](https://docs.docker.com/desktop)
- [Git](https://git-scm.com/downloads)
- [Python 3.14](https://www.python.org/downloads)

### .env

| Переменная           | Описание              |
|:---------------------|:----------------------|
| `TELEGRAM_BOT_TOKEN` | Токен бота в Telegram |

### config.ini

#### Раздел `Settings`

| Настройка               |  Тип   | Описание                                       |
|:------------------------|:------:|:-----------------------------------------------|
| `admins_list`           | `list` | Список ID аккаунтов администраторов в Telegram |
| `file_logging`          | `bool` | Использовать логирование в файлы `.log`        |
| `psychologists_chat_id` | `int`  | ID группы психологов в Telegram                |
| `psychologists_list`    | `list` | Список ID аккаунтов психологов в Telegram      |
| `skip_updates`          | `bool` | Пропускать ожидающие события при запуске бота  |

### Docker

##### Перейдите в корневую директорию

##### Создайте образ

```shell
docker build -t elkollege_psychologist_bot .
```

##### Запустите контейнер

```shell
docker run -d --env-file .env --name ElkollegePsychologistBot elkollege_psychologist_bot
```
