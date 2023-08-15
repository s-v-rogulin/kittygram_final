# Проект Kittygram_Final
### Разработчики:

 - [Рогулин Степан](https://github.com/s-v-rogulin)
 - Ребята из яндекса

### О проекте:

Kittygram — социальная сеть для обмена фотографиями любимых питомцев. Это полностью рабочий проект, который состоит из бэкенд-приложения на Django и фронтенд-приложения на React.

Примененные технологии:
 - Python 
 - Django
 - Git
 - Pytest
 - React
 - и др.

В проекте реализовано:
- настроен запуск проекта Kittygram в контейнерах;
- настроено автоматическое тестирование и деплой этого проекта на удалённый сервер.
- Автоматизация с помощью сервиса GitHub Actions.
- подключены Docker volumes:
    - static — для хранения файлов статики контейнеров backend и frontend. Доступ к этому volume у контейнера gateway, чтобы Nginx мог раздавать эти файлы.
    - media — для хранения файлов, загружаемых пользователями. Доступ к этому volume и у контейнера backend, и у контейнера gateway, чтобы Nginx мог раздавать эти файлы.
    - pg_data — для хранения данных PostgreSQL из контейнера db.



### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/yandex-praktikum/kittygram_backend.git
```

```
cd kittygram_backend
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

* Если у вас Linux/macOS

    ```
    source env/bin/activate
    ```

* Если у вас windows

    ```
    source env/scripts/activate
    ```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```