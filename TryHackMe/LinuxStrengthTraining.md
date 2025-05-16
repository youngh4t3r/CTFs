
# Linux Strength Training

## Подключение через SSH
Для подключения к удаленному хосту `topson`, используем следующую команду:
```bash
ssh topson@10.10.*.*
```
Введите пароль:
```
topson
```

## Переход в директорию
Перейдите в нужную директорию:
```bash
cd /home/topson/chatlogs
```

## Поиск по ключевому слову
Для поиска по ключевому слову используем команду `grep`:
```bash
grep -iRl 'keyword'
```

## Чтение файла
Для просмотра содержимого файла и поиска по ключевому слову используем `less`:
```bash
less ****-**-**
/keyword
```
Чтобы выйти из режима чтения, нажмите `q`.

## Поиск флага
Теперь найдем файл `ReadMeIfStuck.txt` с помощью команды `find`:
```bash
find ~ -type f -name ReadMeIfStuck.txt 2>/dev/null
```
Откроем файл:
```bash
less /home/topson/ReadMeIfStuck.txt
```
![Скриншот 1](screenshot_1)

## Поиск файла `additionalHINT`
Теперь ищем файл `additionalHINT`:
```bash
find / -type f -name 'additionalHINT' 2>/dev/null
```
Откроем файл:
```bash
cat <path_to_file>/additionalHINT
```
![Скриншот 2](screenshot_2)

## Поиск и переход в директорию `telephone numbers`
Для поиска директории с пробелами в названии используем обратный слэш:
```bash
find / -type d -name 'telephone\ numbers' 2>/dev/null
```
Переходим в директорию:
```bash
cd <path_to_directory>/telephone\ numbers
```
Просмотрим содержимое:
```bash
ls
```
Читаем файл:
```bash
cat readME.txt
```
![Скриншот 3](screenshot_3)

## Поиск директории `workflows` и файла, модифицированного 2016-09-12
Для поиска директории `workflows` используем команду:
```bash
find / -type d -name workflows 2>/dev/null
```
Переходим в найденную директорию:
```bash
cd <path_to_directory>/workflows
```
Читаем файл:
```bash
less <file>
```

## Поиск флага
Ищем флаг в файле:
```bash
/Flag
```

## Заключение
Мы научились использовать различные команды Linux для поиска файлов, чтения их содержимого и нахождения флагов в системе. Мы освоили команды `grep`, `find`, `less`, `cat` и другие для работы с файлами и директориями в Linux.
