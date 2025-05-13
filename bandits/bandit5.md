# OverTheWire Bandit: Level 5 → 6

## Описание задачи
Пароль находится в файле где:
- Размер 1033 байта
- Неисполняемый файл
- Принадлежит группе bandit6
- Принадлежит пользователю bandit7

Расположен где-то в директории `inhere`

## Решение

### Шаг 1: Подключение
    ssh bandit5@bandit.labs.overthewire.org -p 2220
Пароль: `4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw` (из уровня 4→5)

### Шаг 2: Поиск файла
1. Переходим в директорию:
    cd inhere

2. Ищем файл по заданным параметрам:
    find . -size 1033c -group bandit6 -user bandit7 -type f ! -executable

3. Читаем найденный файл:
    cat ./maybehere07/.file2

## Найденный пароль
    HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

## Выводы и наблюдения
- Научился использовать `find` с множественными параметрами
- Узнал как искать файлы по:
  - Точному размеру (`-size`)
  - Группе (`-group`)
  - Пользователю (`-user`)
  - Типу (`-type f`)
  - Отсутствию прав на исполнение (`! -executable`)

## Альтернативные методы
1. Поиск с выводом дополнительной информации:
    find . -size 1033c -ls 2>/dev/null

2. Поиск всех файлов нужного размера:
    find . -size 1033c -type f 2>/dev/null
    file $(find . -size 1033c -type f 2>/dev/null)
