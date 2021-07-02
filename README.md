# Описание сервиса
Проект API для Yatube - сервиса который собирает отзывы пользователей на произведения. Произведения делятся на категории: «Книги», «Фильмы», «Музыка».


# Стек технологий
Python
Django
Django REST framework
Postgres
Docker Compose


# Установка проекта
1. Скопируйте проект к себе на компютер ```git clone https://github.com/Lookin44/infra_sp2.git```
2. Склонируйте репозиторий. В корневой директории создайте файл .env со значениями: 
```DB_ENGINE=django.db.backends.postgresql```
```DB_NAME=postgres```
```POSTGRES_USER=postgres```
```POSTGRES_PASSWORD=postgres```   # ваш пароль
```DB_HOST=db```
```DB_PORT=5432```
3. Запустите Docker: ```sudo docker-compose up```
4. Выполните миграции внутри докера ```sudo docker-compose exec web python manage.py migrate --noinput```
5. Создайте суперпользователя внутри докера ```sudo docker-compose exec web python manage.py createsuperuser```
6. Соберите статику внутри докера ```sudo docker-compose exec web python manage.py collectstatic --no-input```
7. Заполнитe базу тестовыми данными ```sudo docker-compose exec web python manage.py loaddata fixtures.json```


# Документация к проекту
1. Запустите сервер
2. Перейдите на http://localhost:8000/redoc/
