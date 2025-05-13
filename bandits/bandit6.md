# OverTheWire Bandit: Level 6 → 7

## Описание задачи
Пароль находится где-то на сервере и соответствует следующим условиям:
- Принадлежит пользователю `bandit7`
- Принадлежит группе `bandit6`
- Размер 33 байта

## Решение

### Шаг 1: Подключение
    ssh bandit6@bandit.labs.overthewire.org -p 2220
Пароль: `HWasnPhtq9AVKe0dmk45nxy20cvUa6EG` (из уровня 5→6)

### Шаг 2: Поиск файла
1. Ищем по всему серверу:
    find / -user bandit7 -group bandit6 -size 33c 2>/dev/null

2. Читаем найденный файл:
    cat /var/lib/dpkg/info/bandit7.password

## Найденный пароль
    morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

## Выводы и наблюдения
- Научился искать файлы по всей системе
- Узнал о перенаправлении ошибок (`2>/dev/null`)
- Понял важность точного указания атрибутов поиска
