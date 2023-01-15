# Программа

Работает с сайтом [TMDB](https://www.themoviedb.org/). Позволяет скачать базу данных из 1000 фильмов, искать в ней фильмы по ключевым словам или по найти похожие фильмы.

# Установка

Скачать гит репозиторий.

# Требования к использованию

Требуется [Python](https://www.python.org/downloads/) версии 3.7 или выше и установленный [pip](https://pip.pypa.io/en/stable/getting-started/). Для работы со скриптами требуется завсети ключ API [здесь](https://www.themoviedb.org/documentation/api). Также нужно создать файл `MyFilmDB.json` в корневой директории. Для установки необходимых зависимостей используйте команду:  
1. Для Unix/macOs:
```commandline
python -m pip install -r requirements.txt
```
2. Для Windows:
```commandline
py -m pip download --destination-directory DIR -r requirements.txt
```

# Скрипты

Все скрипты запускаются без параметров как python скрипт. Пример запуска:
```python
python3 hello_api_TMDB.py
```

## hello_api_TMDB.py

Скрипт просит ввести ключ API, после чего выводит бюджет фильма с номером 215.

Пример вывода скрипта:
```comandline
Enter your api key v3:
4000000
```

## search_in_db.py

Скрипт просит ввести путь к базе данных фильмов. Затем просит указать ключевую фразу. Выводит список всех фильмов из подключонной базы данных, в названии которых содержится ключевая фраза.

Пример вывода скрипта:
```comandline
Enter path to DataBase:MyFilmDB.json
Enter film to search for:room
Four Rooms
```

## find_similar.py

Скрипт просит ввести путь к базе данных фильмов. Затем просит указать название фильма. Из подключонной базы данных, выводит до 8 фильмов наиболее близких к указанному.

Пример вывода скрипта:
```comandline
Enter path to DataBase:MyFilmDB.json
Enter film to search for:Four Rooms
Ariel
Judgment Night
Life in Loops (A Megacities RMX)
Sonntag im August
Varjoja paratiisissa
```

## make_own_db.py

Скрипт просит ввести ключ API. Затем скачивает 1000 фильмов и помещает их в файл `MyFilmDB.json`.

Пример вывода скрипта:
```comandline
Enter your api key v3:
please, wait, this operation may take smth like 15-20 minutes
0.0 percent complete
0.1 percent complete
...
99.9 percent complete
```

## own_db_helpers.py

Скрипт содержит функцию, которая возвращает данные по фильмам в формате .json из выбранного файла. При запуске ничего не выводит.

## tmdb_helpers.py

Скрипт содержит функции для получения информации по фильмам через запросы к API. При запуске ничего не выводит.