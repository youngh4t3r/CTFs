# OverTheWire Bandit: Level 7 → 8

## Описание задачи
Пароль находится в файле `data.txt` рядом со словом **"millionth"**

## Решение

### Шаг 1: Подключение
    ssh bandit7@bandit.labs.overthewire.org -p 2220
Пароль: `morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj` (из уровня 6→7)

### Шаг 2: Поиск пароля
1. Анализируем файл:
    grep "millionth" data.txt

## Найденный пароль
    dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

## Выводы и наблюдения
- Освоил работу с `grep` для поиска по шаблону
- Узнал как быстро анализировать большие файлы
- Понял важность точного указания ключевого слова
