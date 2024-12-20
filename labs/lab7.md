# Лабораторная работа №7

## Задание №1

У вас есть список задач, каждая представлена в виде кортежа `(название, приоритет)`:

```python
tasks = [("Проверить почту", 3), ("Написать отчёт", 1), ("Позвонить клиенту", 2)]
```

Используя sorted и лямбда-выражение, отсортируйте задачи по возрастанию приоритета.

## Задание №2

Дан список покупок, где каждая покупка представлена в виде словаря:

```python
purchases = [
    {"item": "Laptop", "price": 1000, "quantity": 2},
    {"item": "Mouse", "price": 25, "quantity": 5},
    {"item": "Keyboard", "price": 45, "quantity": 3}
]
```

Используя `map` и лямбда-выражение, создайте новый список, содержащий общую стоимость каждой покупки `(price * quantity)`. Затем найдите самую дорогую покупку с помощью `max`.

## Задание №3

У вас есть список клиентов с их годовыми доходами:

```python
clients = [
    {"name": "Alice", "income": 50000},
    {"name": "Bob", "income": 120000},
    {"name": "Charlie", "income": 70000}
]
```

Используя `map` и лямбда-выражение, создайте новый список, где каждому клиенту добавляется категория:

- `"High"` — если доход больше 100,000
- `"Medium"` — если доход от 50,000 до 100,000
- `"Low"` — если доход меньше 50,000

Пример результата:

```python
[
    {"name": "Alice", "income": 50000, "category": "Medium"},
    {"name": "Bob", "income": 120000, "category": "High"},
    ...
]
```

## Задание №4

Дан список рейсов с информацией о времени отправления и прибытия в формате часов:

```python
flights = [
    {"flight": "A1", "departure": 9, "arrival": 12},
    {"flight": "B2", "departure": 14, "arrival": 18},
    {"flight": "C3", "departure": 6, "arrival": 8}
]
```

Используя `filter` и лямбда-выражение, выберите только те рейсы, которые заканчиваются до 12 часов дня.

## Задание №5

В фонде получены сообщения от сотрудников, которые могут содержать ссылки на аномальные ресурсы. Все ссылки должны быть удалены для обеспечения безопасности.

```python
messages = [
    {"user": "Исследователь А", "message": "Отчёт готов. Ссылка: http://foundation.org"},
    {"user": "Доктор Б", "message": "Документы можно найти здесь: https://classified.com"},
    {"user": "Охранник В", "message": "Нет аномальной активности за смену."},
    {"user": "Агент Г", "message": "Срочно изучите материалы по объекту 173 на http://statue-database.net"},
    {"user": "Д-р Кляйн", "message": "Обновлённый протокол эксперимента доступен: https://safezone.scp"},
    {"user": "Сотрудник Д", "message": "Просьба ознакомиться с https://docs.anomalies-secure.com перед сменой."},
    {"user": "Старший учёный Л", "message": "Все записи переданы. Никаких аномалий на объекте 096."},
    {"user": "Техник З", "message": "Проблема с сервером устранена. Подробнее: http://fix-report.internal"}
]
```

Используя `filter` и лямбда-выражение, отберите сообщения, содержащие ссылки (начинаются с `http`). Преобразуйте такие сообщения в формат, где вместо ссылки отображается `[ДАННЫЕ УДАЛЕНЫ]`.

```python
[
    {"user": "Исследователь А", "message": "Отчёт готов. Ссылка: [ДАННЫЕ УДАЛЕНЫ]"},
    {"user": "Доктор Б", "message": "Документы можно найти здесь: [ДАННЫЕ УДАЛЕНЫ]"}
]
```
