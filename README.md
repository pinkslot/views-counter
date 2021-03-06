### Задание
Написать код на PHP, реализующий REST API, предназначенный для учёта посещений сайта с разбиением по странам.

Сервис должен предоставлять два метода:

Обновление статистики, принимает один аргумент – код страны (ru, us, it...).
Предполагаемая нагрузка: 1 000 запросов в секунду.
Получение собранной статистики по всем странам, возвращает JSON-объект вида:
{ код страны: количество, cy: 123, us: 456, ... }.
Предполагаемая нагрузка: 1 000 запросов в секунду.
Хранилище данных: Redis.
Допустимо использование готовых библиотек, фреймворков и т.п..

На оценку влияет готовность к высоким нагрузкам, читаемость кода, обработка ошибок.

### Установка
Выполните `make composer-up && make docker-start` в директории с проектом

### Использование
#### Увеличение счетчика
Выполните запрос
```
POST http://localhost:8000/views
Content-Type: application/json

{
"country": "US"
}
```

чтобы увеличить значение счётчика для страны "US" на единицу.
Код страны указывается в формате ISO 3166-1 alpha-2.

#### Получение значений
Выполните запрос
```
GET http://localhost:8000/views
```
для получения значений всех счетчиков
