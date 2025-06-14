All api adresses are started with `adress.com/api`


# Authentication

| Endpoint           | Request Type | Description                            |
| ------------------ | ------------ | -------------------------------------- |
| `/auth/register`   | `POST`       | Регистрация нового пользователя        |
| `/auth/login`      | `POST`       | Вход в систему (получение JWT-токена)  |
| `/users/me`        | `GET`        | Получение данных текущего пользователя |
| `/users/me`        | `PATCH`      | Обновление профиля                     |
| `/users/{user_id}` | `GET`        | Просмотр профиля другого пользователя  |


# Labs  

| Endpoint                   | Request Type | Description                        |
| -------------------------- | ------------ | ---------------------------------- |
| `/labs`                    | `GET`        | Список всех лаб                    |
| `/labs`                    | `POST`       | Создание новой лабы                |
| `/labs/{lab_id}`           | `GET`        | Просмотр конкретной лабы           |
| `/labs/{lab_id}`           | `PATCH`      | Редактирование лабы (только автор) |
| `/labs/{lab_id}`           | `DELETE`     | Удаление лабы (только автор)       |
| `/labs/{lab_id}/submit`    | `POST`       | Отправка решения (студентом)       |
| `/labs/{lab_id}/solutions` | `GET`        | Список решений (для проверки)      |
| `/labs/{lab_id}/review`    | `POST`       | Добавление проверки/фидбека        |


# Articles  

| Endpoint                          | Request Type | Description            |
| --------------------------------- | ------------ | ---------------------- |
| `/articles`                       | `GET`        | Список статей          |
| `/articles`                       | `POST`       | Публикация статьи      |
| `/articles/{article_id}`          | `GET`        | Просмотр статьи        |
| `/articles/{article_id}`          | `PATCH`      | Редактирование статьи  |
| `/articles/{article_id}`          | `DELETE`     | Удаление статьи        |
| `/articles/{article_id}/feedback` | `GET`        | Список фидбеков        |
| `/articles/{article_id}/feedback` | `POST`       | Добавление фидбека     |
| `/articles/{article_id}/feedback` | `PATCH`      | Редактирование фидбека |


# Feedback

| Endpoint                  | Request Type | Description                           |
| ------------------------- | ------------ | ------------------------------------- |
| `/feedback/{feedback_id}` | `GET`        | Просмотр фидбека                      |
| `/feedback/{feedback_id}` | `POST`       | Добавление фидбека (к лабе/статье)    |
| `/feedback/{feedback_id}` | `PATCH`      | Редактирование фидбека (только автор) |
| `/feedback/{feedback_id}` | `DELETE`     | Удаление фидбека                      |


# Moderation

Add `/reports` or `/admin`?
In progress...

# Monetization

Add `/subscribe` or `/ads`?
In progress...


# AI-Helper  

Add `/ai`?
In progress...