# TryHackMe: Linux Strength Training - Работа с файлами

## Поиск скрытого файла readME_hint.txt

``` bash
find ~ -type f -name readME_hint.txt
cat <file_path>/readME_hint.txt

![Поиск readME_hint.txt](screenshots/screenshot_4.png)

## Поиск и перемещение скрытого файла MoveMe.txt

Задание казалось бы простое, но требует нескольких шагов:
1. Найти файл
2. Найти директорию
3. Переместить файл
4. Исполнить скрипт

Первая попытка найти файл не увенчалась успехом:

``` bash
find ~ -type f -name 'MoveMe.txt' 2>/dev/null

Файл не найден, но мы знаем, что он существует. Вероятно, имя файла начинается со специальных символов. Пробуем:

``` bash
find ~ -type f -name '*MoveMe.txt' 2>/dev/null

Теперь файл найден! Аналогично ищем директорию (не забываем про пробел в названии):

``` bash
find ~ -type d -name '*march\ folder' 2>/dev/null

## Перемещение файла и выполнение скрипта

Перемещаем файл в нужную директорию:

``` bash
mv <file_path>/-MoveMe.txt <directory_path>/-march\ folder
cd <directory_path>/-march\ folder

Проверяем содержимое папки:

``` bash
ls -la

Видим исполняемый файл `-runME.sh`. Запускаем его:

``` bash
./-runME.sh

**Флаг найден!**