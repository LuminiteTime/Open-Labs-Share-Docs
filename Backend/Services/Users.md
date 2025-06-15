### Зачем нужен
Users Service является центральным хранилищем всех пользовательских данных в системе. Он обеспечивает единую точку управления профилями. 

### Функции
- Хранение персональных данных о пользователях (name, surname, login, password, labs solved, labs published)
- CRUD по профилям пользователей
- Переброс запросов на микросервисы

### Основные API
- `users/register` - регистрация юзера
- `users/login` - вход юзера
- `users/refresh` - ручки для работы с JWT
- `users/logout` - выход из системы

**От других микросервисов**
- `/api/users/addLab` → добавить созданную работу
- `/api/users/solveLab` → добавить решённую работу


### Взаимодействие с микросервисами
- **Предоставление данных для Karma Service:** Базовая информация для расчета рейтингов
- **Связь с Labs Service:** Авторство и права доступа к лабораторным работам
- **Поддержка Feedback Service:** Профильная информация для отзывов и комментариев

### Структуры данных

**User Entity:**

| Field    | Type        |
| -------- | ----------- |
| id (PK)  | UUID / long |
| email    | string      |
| name     | string      |
| surname  | string      |
| password | hex string  |

**Labs Solved Relation**

| Field    | Type        |
| -------- | ----------- |
| user_id  | UUID / long |
| lab_id   | UUID / long |

**Labs Published Relation**

| Field    | Type        |
| -------- | ----------- |
| user_id  | UUID / long |
| lab_id   | UUID / long |

