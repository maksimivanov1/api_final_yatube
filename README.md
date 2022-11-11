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
