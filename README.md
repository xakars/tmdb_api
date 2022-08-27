# tmdb_api

Приведенные скрипты позволяют скачивать информацию о фильмах из сайта [themoviedb.org](https://www.themoviedb.org/) и создать локальную "базу" в файле MyFilmDB.json, и далее по этой базе искать фильмы, получать рекомендации фильмов(на основе рейтинга какого-нибудь фильма). Прежде чем воспользоваться утилитами необходимо получить api_key из выше указанного сайта.

## Описание скриптов
hello_api_TMDB.py скрип выводит потраченный бюджет для фильма "Пила 2". При работе скрипта используется файл tmdb_helpers.py, где реализованы основные функции такие как: получение от пользователя api_key, отправка запроса на API.
```
$ python3 hello_api_TMDB.py
Enter your api key v3:
4000000
```
make_own_db.py скрипт создает локальную "базу" с информацией о фильмах. Данные сохраняются в файл MyFilmDB.json.
```
python3 make_own_db.py
Enter your api key v3:
please, wait, this operation may take smth like 15-20 minutes
0.0 percent complete
33.333333333333336 percent complete
66.66666666666667 percent complete 
```
search_in_db.py скрипт ищет фильм. Просит пользователя ввести название фильма, которое хотим найти.
``` 
python3 search_in_db.py
Enter path to DataBase:MyFilmDB.json
Enter film to search for:Saw
Saw 
Saw II
Saw III
Saw IV
```  
find_similar.py скрип выводит похожий фильм. Просит пользователя ввести название похожего фильма по которому будет формироваться рекомендация. При работе использует файл own_db_helpers где рализовано достование "базы".
```
python3 find_similar.py
Enter path to DataBase:MyFilmDB.json
Enter film to search for:Saw
Four Rooms
Harold and Maude
Judgment Night

```

