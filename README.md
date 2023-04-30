API для приложение Yatube
Програмный интерфейс приложения Yatube - новой социальной сети. Используется для взаимодействия программ. С помощью GET и POST- запросов клиент может получать или добавлять/изменять информацию в база денных приложения. Передача данных осуществляется в формате JSON.

Ресурсы API YaMDb
AUTH: аутентификация.

USERS: пользователи.

TITLES: произведения, к которым пишут отзывы (определённый фильм, книга или песенка).

CATEGORIES: категории (типы) произведений ("Фильмы", "Книги", "Музыка").

GENRES: жанры произведений. Одно произведение может быть привязано к нескольким жанрам.

REVIEWS: отзывы на произведения. Отзыв привязан к определённому произведению.

COMMENTS: комментарии к отзывам. Комментарий привязан к определённому отзыву.

Используемые технологии
Django 3.2.16
djangorestframework 3.12.4
djangorestframework-simplejwt 4.7.2
Pillow 9.3.0
Как запустить проект
Клонировать репозиторий и перейти в него в командной строке:
git clone https://git@github.com:DmitryOstrovskiy/api_final_yatube.git

cd api_final_yatube

Cоздать и активировать виртуальное окружение:
python3 -m venv env

Windows: source venv\scripts\activate; Linux/Mac: sorce venv/bin/activate

Установить зависимости из файла requirements.txt:
python -m pip install --upgrade pip

pip install -r requirements.txt

Выполнить миграции:
python manage.py migrate

Запустить проект:
python manage.py runserver

Примеры запросов к API
Запрос GET: http://127.0.0.1:8000/api/v1/posts/ Ответ: { "count": 123, "next": "http://api.example.org/accounts/?offset=400&limit=100", "previous": "http://api.example.org/accounts/?offset=200&limit=100", "results": [ { "id": 0, "author": "string", "text": "string", "pub_date": "2021-10-14T20:41:29.648Z", "image": "string", "group": 0 } ] }

Запрос POST: http://127.0.0.1:8000/api/v1/posts/ { "text": "string", "image": "string", "group": 0 } Ответ: { "id": 0, "author": "string", "text": "string", "pub_date": "2019-08-24T14:15:22Z", "image": "string", "group": 0 }
