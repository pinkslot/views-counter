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
Выполните `composer-up && docker-start` в директории с проектом
