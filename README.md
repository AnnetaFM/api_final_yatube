API для приложения Yatube.


Описание.

API для приложения Yatube позволяет реализовывать базовый функционал для социальной сети:

- Создавать, редактировать, удалять и просматривать публикации.
- Просмтаривать и получать информацию о сообществах.
- Комментрировать, просмматривать один или несколько комментариев.
- Подписываться на других пользователей.

Для создания приложения использовались следующие технологии:

Django 3.2.16
djangorestframework 3.12.4
Pillow 9.3.0


Установка и запуск проекта.

В терминале склонируйте репозиторий и перейдите в него:
git clone git@github.com:AnnetaFM/api_final_yatube.git
cd api_final_yatube

Создайте и активируйте виртуальное окружение:
python3 -m venv env
source env/bin/activate

Установите зависимости из файла requirements.txt:
python3 -m pip install --upgrade pip
pip install -r requirements.txt

Выполните миграции:
python3 manage.py migrate

Запустите проект:
python3 manage.py runserver


Примеры.

Некоторые примеры запросов к API:

Получить список всех постов:
GET /api/v1/posts/

Добавление нового поста:
POST /api/v1/posts/

Получить список всех групп:
GET /api/v1/groups/

Добавление нового комментария:
POST /api/v1/posts/{post_id}/comments/

