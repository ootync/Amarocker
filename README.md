# Amarocker: Amarok2 star!

## English

The script allows:

* List star-rated tracks
* Upload star-rated tracks to a media player, optionally - converting them to mp3
* Easily access MySQL-console & hack into Amarok's database
* Forcibly write statistics (FMPS Rating, Playcount, Score) into all tracks (Amarok2 does it not)

Relax, you no longer need to keep Amarok's DB safe :) Just ensure 'Write statistics to file' checkbox is set.

Usage:

* `amarocker ls` — list all star-rated tracks
* `amarocker ls-data` — list star-rated tracks + ratings
* `amarocker mysql` — MySQL-console for manual data operations
* `amarocker wrstats` — Force write Amarok statistics to files: Rating, Score, Playcount
* `amarocker copy /media/iPod/` — Copy star-rated tracks with rsync to a media player
* `amarocker conv /media/iPod/` — Convert star-rated tracks to mp3 and upload them to a media player. Multi-threaded! You can specify another format & bitrate: `amarocker conv /media/iPod/ 'mp3' '-2.2'`

While converting, album art is also copied (when the file is in the same folder with the audio track). Tracks are not re-uploaded: you can update your collection. Additionally, ID3 tags are converted to 2.4 so Android can handle non-ASCII.

## Russian

Amarok2 позволяет отмечать звёздами понравившиеся треки, однако эта информация хранится в встроенной базе данных. Проблема появляется когда хочется перекачать на плеер только лучшие треки, и не дай бог — сконвертировать их в MP3 чтобы оно всё поместилось!

Скрипт позволяет:

* Получить список звёздных треков
* Залить на плеер звёздные треки, конвертируя их в mp3 (или просто копировать)
* Легко получить mysql-консоль и поковыряться внутри базы Amarok2 :)
* Насильно вписать во ВСЕ звёздные треки метаинформацию о рейтинге (Amarok2 это не делает!)

Теперь можно не бояться что Amarok потеряет базу :) Убедитесь что установлена галка "Записывать статистику в файл".

Использование:

* amarocker ls — получить список звёздных треков
* amarocker ls-data — список треков + циферки-рейтинги
* amarocker mysql — MySQL-консоль для ручной работы с данными
* amarocker wrstats — Записать в метаданные всех треков их статистику: Rating, Score, Playcount
* amarocker copy /media/iPod/ — Скопировать rsync'ом все звёздные треки на плеер
* amarocker conv /media/iPod/ — Сконвертировать все звёздные треки в mp3 и залить на плеер. Многопоточно. Можно указать битрейт и другой формат: amarocker conv /media/iPod/ 'mp3' '-2.2' 

При конвертации — на плеер также улетают обложки альбомов (если лежат в той же папке что и сам трек). Однажды закачанные треки повторно не конвертируются: коллекцию можно обновлять. Кроме того, id3 преобразуется в версию 2.4 чтобы на Android нормально читались русские композиции :)