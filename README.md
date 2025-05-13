# CTF Solutions by youngh4t3r

🔐 **О репозитории**:  
Решения задач OverTheWire Bandit с пояснениями и выводами.  

## 🎯 OverTheWire Bandit Walkthrough

| Уровень | Описание задачи | Ключевые навыки | Файл с решением |
|---------|-----------------|-----------------|-----------------|
| 0 → 1   | Базовые команды Linux | `ssh`, `ls`, `cat` | [bandit0.md](bandit/bandit0.md) |
| 1 → 2   | Файлы с спецсимволами | `cat ./-` | [bandit1.md](bandit/bandit1.md) |
| 2 → 3   | Пробелы в именах файлов | `cat "spaces in name"` | [bandit2.md](bandit/bandit2.md) |
| 3 → 4   | Скрытые файлы | `ls -a`, `cat .hidden` | [bandit3.md](bandit/bandit3.md) |
| 4 → 5   | Поиск по атрибутам файлов | `file`, `find` | [bandit4.md](bandit/bandit4.md) |
| 5 → 6   | Углубленный поиск файлов | `find -size -group -user` | [bandit5.md](bandit/bandit5.md) |
| 6 → 7   | Поиск по всей системе | `find /` | [bandit6.md](bandit/bandit6.md) |
| 7 → 8   | Поиск по шаблону | `grep "millionth"` | [bandit7.md](bandit/bandit7.md) |
| 8 → 9   | Анализ дубликатов | `sort`, `uniq -u` | [bandit8.md](bandit/bandit8.md) |
| 9 → 10  | Работа с бинарными данными | `strings`, `grep` | [bandit9.md](bandit/bandit9.md) |
| 10 → 11 | Декодирование base64 | `base64 -d` | [bandit10.md](bandit/bandit10.md) |
| 11 → 12 | Шифр ROT13 | `tr 'A-Za-z' 'N-ZA-Mn-za-m'` | [bandit11.md](bandit/bandit11.md) |
| 12 → 13 | Работа с hex-дампами | `xxd -r`, `file`, распаковка | [bandit12.md](bandit/bandit12.md) |
| 13 → 14 | SSH-ключи | `ssh -i`, `chmod 600` | [bandit13.md](bandit/bandit13.md) |
| 14 → 15 | Сетевые соединения | `nc localhost 30000` | [bandit14.md](bandit/bandit14.md) |

## 🛠 Технологии
- **Языки**: Bash
- **Инструменты**: 
  - `grep`, `awk`, `sed`
  - `nmap`, `netcat`
  - `openssl`, `base64`

## 📚 Как пользоваться
1. Перейдите в папку `bandit/`
2. Откройте файл нужного уровня
3. Каждый файл содержит:
   - Условие задачи
   - Пошаговое решение
   - Ключевые выводы

## 🔥 В процессе
- [ ] Bandit 15-33

---

💡 **Совет**: Используйте `tree` для просмотра структуры репозитория:
```bash
tree -L 2 -I '*.txt'

Основные изменения:
1. Добавлена столбец "Файл с решением" с относительными ссылками
2. Исправлены пути в формате `bandit/N.md` вместо `banditN.md`
3. Добавлены примеры ключевых команд для каждого уровня
4. Улучшена структура таблицы
5. Добавлен раздел "В процессе" для отслеживания прогресса

Для корректной работы:
1. Убедитесь, что все файлы решений лежат в папке `bandit/`
2. Имена файлов должны соответствовать шаблону `bandit[0-9]+.md`
3. Для новых уровней просто добавляйте строки в таблицу

## 🤝 **Контакты**  
- **LinkedIn**: https://www.linkedin.com/in/youngh4t3r/
- **Telegram**: @younghater  
- **Почта**: pyatinbogdan@gmail.com  

*Приветствуются вопросы и коллаборации!*  
