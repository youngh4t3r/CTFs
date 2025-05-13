# OverTheWire Bandit: Level 10 → 11

## Описание задачи
Пароль находится в файле `data.txt`, закодированном в формате **base64**

## Решение

### Шаг 1: Подключение
    ssh bandit10@bandit.labs.overthewire.org -p 2220
Пароль: `FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey` (из уровня 9→10)

### Шаг 2: Декодирование файла
1. Декодируем содержимое:
    cat data.txt | base64 -d

2. Альтернативный вариант:
    base64 -d data.txt

## Найденный пароль
    dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

## Выводы и наблюдения
- Освоил работу с командой `base64`
- Узнал о простых методах кодирования данных
