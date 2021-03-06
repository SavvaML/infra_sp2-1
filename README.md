# infra_sp2
infra_sp2 это API проекта api_yamdb, который собирает отзывы (Review) пользователей на произведения (Title). 
Произведения делятся на категории (Category). В каждой категории есть произведения: книги, фильмы или музыка.
Произведению может быть присвоен жанр (Genres) из списка предустановленных. Новые жанры может создавать только администратор.\
Благодарные или возмущённые читатели оставляют к произведениям текстовые отзывы (Review) и выставляют произведению рейтинг. \
Сами произведения в api_yamdb не хранятся, здесь нельзя посмотреть фильм или послушать музыку.

---
<h3> Установка и развертывание </h3>
Клонировать репозиторий

    $ git clone https://github.com/Ilia-Abrosimov/infra_sp2

Запуск приложения

    $ docker-compose up
  
Выполнить миграции

    $ docker-compose exec web python manage.py migrate

Копировать статику

    $ docker-compose exec web python manage.py collectstatic --noinput
   
Заполнение базы начальными данными

    $ docker-compose exec web python manage.py loaddata fixtures.json 
 
Документация по API доступна по адресу\
http://localhost:1337/redoc

Доступ к админке\
http://localhost:1337/admin

Перечь произведений\
http://localhost:1337/api/v1/titles/