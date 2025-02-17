## Описание

Аддон позволяет прочитать файлы истории прослушиваний с десктоп и мобильного приложения Spotify.
Способен удалить ее из заданного массива `removeTracks`. Также перевести в полноценный массив треков `getTracks`.

> У такой истории нет даты прослушивания

Пример использования - удалить прослушанные ранее любимые треки
```js
let tracks = Source.getSavedTracks();
HistoryManager.removeTracks(tracks);
```

## Установка

1. Создайте новый скрипт и скопируйте в него содержимое `history-manager.js`.
2. Добавьте в папку `Goofy Data` на Google Диске файлы истории прослушиваний от приложений Spotify
   
   Файл называется `context_player_state_restore`

   Путь Windows: C:\Users\ **Имя пользователя** \AppData\Local\Spotify\Users\ **ИД пользователя**

   Путь Android: /android/data/com.spotify.music/files/spotifycache/users/ **ИД пользователя**

3. Переименуйте файлы, если используете оба.
3. Добавьте имена этих файлов в константу `FILES`.

> Существуют способы автоматической загрузки файлов в Google Диск с андроид и ПК. Например, программа `Air Explorer` для ПК. 
> 
> Это выходит за рамки библиотеки. Если вы знаете способ, можете описать его [на форуме](https://github.com/Chimildic/goofy/discussions).
> 
> Такой подход автоматизирует доставку истории прослушиваний и делает ее более точной в сравнении с `RecentTracks`. 
