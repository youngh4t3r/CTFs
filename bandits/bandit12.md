# OverTheWire Bandit: Уровень 12 → 13

## Описание задачи
Пароль хранится в файле `data.txt`, который:
1. Был преобразован в hex-дамп
2. Многократно сжат разными алгоритмами (gzip, bzip2, tar)

## Решение

### Шаг 1: Подключение
    ssh bandit12@bandit.labs.overthewire.org -p 2220
Пароль: `7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4` (с уровня 11→12)

### Шаг 2: Восстановление и распаковка
1. Создаем рабочую директорию:
    mkdir /tmp/restored
    cd /tmp/restored
    cp ~/data.txt ./

3. Конвертируем hex-дамп обратно в бинарный файл:
    xxd -r data.txt > data.bin

4. Определяем тип файла и распаковываем поэтапно:
    file data.bin  # Проверяем тип файла
    # Последовательность распаковки:
    mv data.bin data.gz && gzip -d data.gz
    mv data data.bz2 && bzip2 -d data.bz2
    mv data data.tar && tar xf data.tar
    mv data5.bin data5.tar && tar xf data5.tar
    mv data6.bin data6.bz2 && bzip2 -d data6.bz2
    mv data6 data6.tar && tar xf data6.tar
    mv data8.bin data8.gz && gzip -d data8.gz

5. Читаем результат:
    cat data8

## Найденный пароль
    FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

## Выводы и наблюдения
- Освоил работу с утилитой `xxd` для hex-дампов
- Узнал как определять тип файла через `file`
- Понял принцип последовательной распаковки вложенных архивов
- Научился работать с gzip, bzip2 и tar в командной строке
