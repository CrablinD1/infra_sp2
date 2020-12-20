# api_yamdb
Проект YaMDb собирает отзывы пользователей на произведения
При разработке приложения использованы фреймфорки ```django и django-rest-framework```. В качестве базы выступает ```postgresql```
Запуск проекта осуществляется средствами ```docker```

## Установка

#### 1. Установка docker и docker-compose

Если у вас уже установлены docker и docker-compose, этот шаг можно пропустить, иначе можно воспользоваться официальной [инструкцией](https://docs.docker.com/engine/install/).

#### 2. Запуск контейнера
```bash
docker-compose up
```
### 3. Выключение контейнера
```bash
docker-compose down
```


## Использование
#### Сборка статических файлов:
```bash
docker exec -it <CONTAINER ID> python manage.py collectstatic
```

#### Миграции Django:
```bash
docker exec -it <CONTAINER ID> python manage.py makemigrations
docker exec -it <CONTAINER ID> python manage.py migrate
```

#### Создание суперпользователя Django:
```bash
docker exec -it <CONTAINER ID> python manage.py createsuperuser
```

#### Загрузка стартовых данных:
```bash
docker exec -it <CONTAINER ID> python manage.py loaddata fixtures.json
```

