# HW_DRF

## Описание
Платформа для онлайн-обучения, на которой каждый желающий может размещать свои полезные материалы или курсы.


### Основные функции:

Реализован CRUD для пользователей, включая регистрацию и настройку JWT-авторизации. Эндпоинты регистрации и авторизации доступны без авторизации, остальные защищены
- Создана группа модераторов с правами управления уроками и курсами (без возможности их удаления и создания)
- Настроены права доступа:
  - Модераторы могут управлять любыми курсами и уроками
  - Пользователи вне группы модераторов могут видеть, редактировать и удалять только свои курсы и уроки
- Для профилей пользователей добавлены ограничения:
  - Авторизованный пользователь может просматривать любой профиль, но редактировать только свой 
  - При просмотре чужого профиля отображается только общая информация (без истории платежей)

## Установка

1. Клонируйте репозиторий:
```bash
https://github.com/E-Kryuger/HW_DRF.git
```
2. Установите зависимости:
```bash
pip install -r requirements.txt
```

## Подключение БД
1. Создайте БД
2. Создайте файл `.env` из файла `.env.sample`

## Применение миграций
```bash
python manage.py migrate
```

### Результат выполнения команд
| Name                                                                           | Stmts   | Miss   | Cover   |
|--------------------------------------------------------------------------------|---------|--------|---------|
| config\\_\_init__.py                                                             | 0       | 0      | 100%    |
| config\asgi.py                                                                 | 4       | 4      | 0%      |
| config\settings.py                                                             | 29      | 0      | 100%    |
| config\urls.py                                                                 | 7       | 0      | 100%    |
| config\wsgi.py                                                                 | 4       | 4      | 0%      |
| lms\\_\_init__.py                                                                | 0       | 0      | 100%    |
| lms\admin.py                                                                   | 10      | 0      | 100%    |
| lms\apps.py                                                                    | 4       | 0      | 100%    |
| lms\management\\_\_init__.py                                                     | 0       | 0      | 100%    |
| lms\management\commands\\_\_init__.py                                            | 0       | 0      | 100%    |
| lms\management\commands\fill_lms.py                                            | 17      | 17     | 0%      |
| lms\migrations\0001_initial.py                                                 | 5       | 0      | 100%    |
| lms\migrations\0002_alter_lesson_options_course_owner_lesson_owner_and_more.py | 6       | 0      | 100%    |
| lms\migrations\\_\_init__.py                                                     | 0       | 0      | 100%    |
| lms\models.py                                                                  | 34      | 3      | 91%     |
| lms\paginators.py                                                              | 5       | 0      | 100%    |
| lms\serializers.py                                                             | 27      | 0      | 100%    |
| lms\services.py                                                                | 10      | 2      | 80%     |
| lms\tests.py                                                                   | 159     | 0      | 100%    |
| lms\urls.py                                                                    | 8       | 0      | 100%    |
| lms\validators.py                                                              | 11      | 0      | 100%    |
| lms\views.py                                                                   | 66      | 8      | 88%     |
| manage.py                                                                      | 11      | 2      | 82%     |
| users\\_\_init__.py                                                              | 0       | 0      | 100%    |
| users\admin.py                                                                 | 11      | 0      | 100%    |
| users\apps.py                                                                  | 4       | 0      | 100%    |
| users\migrations\0001_initial.py                                               | 6       | 0      | 100%    |
| users\migrations\0002_payment.py                                               | 6       | 0      | 100%    |
| users\migrations\\_\_init__.py                                                   | 0       | 0      | 100%    |
| users\models.py                                                                | 50      | 16     | 68%     |
| users\permissions.py                                                           | 19      | 3      | 84%     |
| users\serializers.py                                                           | 25      | 5      | 80%     |
| users\tests.py                                                                 | 1       | 0      | 100%    |
| users\urls.py                                                                  | 7       | 0      | 100%    |
| users\views.py                                                                 | 39      | 4      | 90%     |
| **TOTAL**                                                                      | **585** | **68** | **88%** |

