# API_Yatube
## Это API для социальной сети Yatube.
По средствам запросов можно получать информацию о группах,постах,подписках,комментариях,кроме того изменять её.

### Как развернуть проект?
#### 1. Клонируйте репозиторий:
>git clone git@github.com:maksimivanov1/api_final_yatube.git
#### 2. Перейдите в директорию:
>cd api_final_yatube
#### 3. Создайте и активируйте виртуальное окружение:
>python3 -m venv venv

>source venv/bin/activate (MacOS)

>source venv/Scripts/activate (Windows)
#### 4. Установите зависимости из файла requirements.txt:
>python3 -m pip install --upgrade pip

>pip install -r requirements.txt
#### 5. Перейдите в директорию с файлом manage.py:
#### 6. Создайте и выполните миграции:
>python3 manage.py makemigrations

>python3 manage.py migrate
#### 7. Запустите сервер:
>python3 manage.py runserver

### Документация доступна по адресу:
> http://127.0.0.1:8000/redoc/

### Примеры запросов:
1. (GET) Получить список всех постов:
>http://127.0.0.1:8000/api/v1/posts/
2. (GET) Получить список всех групп:
>http://127.0.0.1:8000/api/v1/groups/
3. (POST) Добавление поста  .../api/v1/posts (for auth user):
```bash
{
    "text": "Test post.",
    "group": 1
}
```

 Ответ:
 ```bash
{
    "id": 1,
    "author": "Bob",
    "text": "Test post.",
    "pub_date": "2022-11-11T19:43:54.531905Z",
    "image": null,
    "group": 1
}
```

4. (GET) Получить информацию о группе .../api/v1/groups/1/

 Ответ:
```bash
{
    "id": 1,
    "title": "Test group",
    "slug": "test_slug",
    "description": "Описание группы"
}
```