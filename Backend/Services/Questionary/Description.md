
### Зачем нужен
Questionary Service отвечает за создание, хранение и проведение тестов и открытых вопросов для проверки знаний пользователей после прохождения лабораторных работ. Предоставляет возможность ответить на: single choice, multiple choice, open questions.

### Функции
- CRUD по тестовым вопросам: single choice, multiple choice, open questions
- **Автоматическая проверка** тестовых заданий с мгновенным результатом
- **Ручная проверка открытых вопросов** преподавателями с возможностью выставления баллов (или ИИ, или другими пользователями)
- **Привязка к лабораторным работам** для проверки усвоения конкретного материала
- **Статистика прохождения** и аналитика результатов для студентов и преподавателей


### Основные API

**Для фронтенда через API Gateway:**
- `questionary/create` - создание нового теста (для преподавателей)
- `questionary/{labId}` - получение теста, связанного с лабораторной работой
- `questionary/{id}/questions` - получение списка вопросов для прохождения
- `questionary/{id}/submit` - отправка ответов пользователя на тест
- `questionary/{id}/results` - получение результатов тестирования
- `questionary/pending` - список тестов, ожидающих ручной проверки

**От других микросервисов (gRPC):**
- `GetQuestionaryByLab` → получение теста для конкретной лабораторной работы (для Labs Service)
- `GetUserTestResults` → результаты тестирования пользователя (для Karma Service)
- `CheckTestCompletion` → проверка прохождения теста (для Users Service)
- `GetTestStats` → статистика по тестам для аналитики


### Взаимодействие с микросервисами
- **Связь с Labs Service:** Получение метаданных лабораторных работ для привязки тестов и проверки доступа к материалам
- **Интеграция с Users Service:** Валидация прав пользователей на создание тестов и получение профильной информации для результатов
- **Передача данных в Karma Service:** Результаты тестирования влияют на репутацию как студентов (за успешное прохождение), так и преподавателей (за качество вопросов)
- **Поддержка Feedback Service:** Возможность оставления отзывов о качестве и сложности вопросов в тестах


## **Типы вопросов**
- **Простые тестовые:** Multiple choice с 2-5 вариантами ответов, один правильный ответ
- **Открытые вопросы:** Текстовые поля для развернутых ответов, требующих ручной проверки преподавателем
- **Возможность расширения:** Архитектура позволяет добавлять новые типы вопросов (true/false, сопоставление, числовые ответы)


### Checks:
- [[Test]]
- [[Open]]