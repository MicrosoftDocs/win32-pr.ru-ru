---
description: В этом разделе перечислены наиболее распространенные свойства метаданных для файлов мультимедиа.
ms.assetid: 35187720-413a-45a0-8558-918f7c3161e1
title: Свойства метаданных для файлов мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cab541a480b03d7ef6bfb9a1a2036226b767774
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703434"
---
# <a name="metadata-properties-for-media-files"></a>Свойства метаданных для файлов мультимедиа

В этом разделе перечислены наиболее распространенные свойства метаданных для файлов мультимедиа.

-   [Общие свойства мультимедиа](#common-media-properties)
-   [Свойства общего доступа к носителю](#media-sharing-properties)
-   [Сопоставления пакета SDK Windows Media Format](#windows-media-format-sdk-mappings)
-   [См. также](#related-topics)

## <a name="common-media-properties"></a>Общие свойства мультимедиа

Система свойств оболочки определяет набор общих свойств метаданных для всех типов объектов оболочки. Подмножество этих компонентов применимо к файлам мультимедиа. В следующей таблице перечислены наиболее распространенные свойства оболочки для мультимедиа. Файлы мультимедиа могут поддерживать дополнительные свойства, не указанные здесь. Кроме того, не все форматы файлов поддерживают каждое из перечисленных свойств. Полный список свойств оболочки см. в разделе [свойства оболочки](/previous-versions//ff521730(v=vs.85)).



| PROPERTYKEY                                                              | Имя оболочки                                                                                    | Описание                                                                                                                                                                                               | Тип данных    |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [\_ \_ \_ Идентификатор профиля DLNA для содержимого мфпкэй \_](mfpkey-content-dlna-profile-id.md) | Нет                                                                                          | Идентификатор профиля Digital живая Network Alliance (DLNA).                                                                                                                                                | VT \_ LPWSTR   |
| **PKEY \_ Audio \_ чаннелкаунт**                                            | [System. Audio. Чаннелкаунт](../properties/props-system-audio-channelcount.md)                       | Число аудиоканалов.                                                                                                                                                                                 | VT \_ UI4      |
| **PKEY \_ Audio \_ енкодингбитрате**                                         | [System. Audio. Енкодингбитрате](../properties/props-system-audio-encodingbitrate.md)                 | Средняя скорость потока звука, в битах в секунду.                                                                                                                                                               | VT \_ UI4      |
| **\_Звуковой \_ Формат PKEY**                                                  | [System. Audio. Format](../properties/props-system-audio-format.md)                                   | Подтип аудио ([**MF \_ MT \_**](mf-mt-subtype-attribute.md)), выраженный в виде строки.                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ Audio \_ исвариаблебитрате**                                       | [System. Audio. Исвариаблебитрате](../properties/props-system-audio-isvariablebitrate.md)             | Указывает, использует ли аудиопоток скорость кодирования переменной.                                                                                                                                       | Логическое значение VT \_     |
| **PKEY \_ Audio \_ пеаквалуе**                                               | [System. Audio. Пеаквалуе](../properties/props-system-audio-peakvalue.md)                             | Пиковый уровень громкости звукового содержимого.                                                                                                                                                                       | VT \_ UI4      |
| **PKEY \_ Audio \_ SampleRate**                                              | [System. Audio. SampleRate](../properties/props-system-audio-samplerate.md)                           | Скорость выборки звука в примерах в секунду. Эквивалентно входным [**\_ образцам "MF MT Audio" в \_ \_ \_ \_ секунду**](mf-mt-audio-samples-per-second-attribute.md) в типе мультимедиа.                           | VT \_ UI4      |
| **PKEY \_ Audio \_ SampleSize**                                              | [System. Audio. SampleSize](../properties/props-system-audio-samplesize.md)                           | Число битов на аудио выборка. Эквивалентно параметру [**MF \_ \_ Audio \_ бит \_ на \_ выборку**](mf-mt-audio-bits-per-sample-attribute.md) в типе носителя.                                         | VT \_ UI4      |
| **PKEY \_ Audio \_ стреамнумбер**                                            | [System. Audio. Стреамнумбер](../properties/props-system-audio-streamnumber.md)                       | Идентификатор аудиопотока.                                                                                                                                                                           | VT \_ UI4      |
| **\_Автор PKEY**                                                         | [System.Author](../properties/props-system-author.md)                                               | Календаря.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **\_Комментарий PKEY**                                                        | [System. комментарий](../properties/props-system-comment.md)                                             | Комментарий, прикрепленный к файлу, обычно добавляемый пользователем.                                                                                                                                                  | VT \_ LPWSTR   |
| **\_Авторские права PKEY**                                                      | [System. ©](../properties/props-system-copyright.md)                                         | Сведения об авторских правах.                                                                                                                                                                                    | VT \_ LPWSTR   |
| **\_Защита управления правами на PKEY \_**                                               | [System. DRM. для защиты](../properties/props-system-drm-isprotected.md)                             | Указывает, защищено ли содержимое с помощью управления цифровыми правами (DRM).                                                                                                                         | Логическое значение VT \_     |
| **\_Ключевые слова PKEY**                                                       | [System.Keywords](../properties/props-system-keywords.md)                                           | Словами.                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **\_Язык PKEY**                                                       | [System. Language](../properties/props-system-language.md)                                           | Язык.                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **\_Аусорурл носителя \_ PKEY**                                               | [System. Media. Аусорурл](../properties/props-system-media-authorurl.md)                             | URL-адрес сайта автора.                                                                                                                                                                              | VT \_ LPWSTR   |
| **\_Аверажелевел носителя \_ PKEY**                                            | [System. Media. Аверажелевел](../properties/props-system-media-averagelevel.md)                       | Средний уровень громкости звукового содержимого.                                                                                                                                                                    | VT \_ UI4      |
| **\_Класспримарид носителя \_ PKEY**                                          | [System. Media. Класспримарид](../properties/props-system-media-classprimaryid.md)                   | Строковое представление идентификатора GUID, определяющего основной класс носителя. Допустимые значения см. в документации по атрибуту [**WM/медиакласспримарид**](../wmformat/wm-mediaprimaryid.md) .       | VT \_ LPWSTR   |
| **\_Класссекондарид носителя \_ PKEY**                                        | [System. Media. Класссекондарид](../properties/props-system-media-classsecondaryid.md)               | Строковое представление идентификатора GUID, определяющего вторичный класс носителя. Допустимые значения см. в документации по атрибуту [**WM/медиакласссекондарид**](../wmformat/wm-mediasecondaryid.md) . | VT \_ LPWSTR   |
| **\_Коллектионграупид носителя \_ PKEY**                                       | [System. Media. Коллектионграупид](../properties/props-system-media-collectiongroupid.md)             | Строковое представление идентификатора GUID, идентифицирующего группу коллекции.                                                                                                                                 | VT \_ LPWSTR   |
| **\_CollectionID носителя \_ PKEY**                                            | [System. Media. CollectionID](../properties/props-system-media-collectionid.md)                       | Строковое представление идентификатора GUID, идентифицирующего коллекцию.                                                                                                                                       | VT \_ LPWSTR   |
| **\_Контентдистрибутор носителя \_ PKEY**                                      | [System. Media. Контентдистрибутор](../properties/props-system-media-contentdistributor.md)           | Распространитель содержимого.                                                                                                                                                                               | VT \_ LPWSTR   |
| **Идентификатор \_ ContentID носителя "PKEY" \_**                                               | [System. Media. ContentID](../properties/props-system-media-contentid.md)                             | Строковое представление идентификатора GUID, идентифицирующего коллекцию.                                                                                                                                       | VT \_ LPWSTR   |
| **\_Датинкодед носителя \_ PKEY**                                             | [System. Media. Датинкодед](../properties/props-system-media-dateencoded.md)                         | Время кодирования содержимого.                                                                                                                                                                        | VT \_ fileTime |
| **\_Датерелеасед носителя \_ PKEY**                                            | [System. Media. Датерелеасед](../properties/props-system-media-datereleased.md)                       | Исходная дата выпуска.                                                                                                                                                                                    | VT \_ LPWSTR   |
| **\_Длительность носителя \_ PKEY**                                                | [System. Media. Duration](../properties/props-system-media-duration.md)                               | Длительность, в 100-наносекундных единицах. Эквивалентно атрибуту " [**\_ \_ Продолжительность MF PD**](mf-pd-duration-attribute.md) " в дескрипторе представления.                                                       | VT \_ UI8      |
| **\_Двдид носителя \_ PKEY**                                                   | [System. Media. ДВДИД](../properties/props-system-media-dvdid.md)                                     | Идентификатор диска цифрового видео (ДВДИД).                                                                                                                                                                    | VT \_ LPWSTR   |
| **\_Енкодедби носителя \_ PKEY**                                               | [System. Media. Енкодедби](../properties/props-system-media-encodedby.md)                             | Имя пользователя или группы, которые кодируют содержимое.                                                                                                                                                     | VT \_ LPWSTR   |
| **\_Енкодингсеттингс носителя \_ PKEY**                                        | [System. Media. Енкодингсеттингс](../properties/props-system-media-encodingsettings.md)               | Описание параметров, используемых для кодирования содержимого.                                                                                                                                                   | VT \_ LPWSTR   |
| **\_Мкди носителя \_ PKEY**                                                    | [System. Media. МКДИ](../properties/props-system-media-mcdi.md)                                       | Идентификатор музыкального компакт-диска. Это значение используется для задания компакт-диска.                                                                                                                                                 | VT \_ LPWSTR   |
| **\_Метадатаконтентпровидер носителя \_ PKEY**                                 | [System. Media. Метадатаконтентпровидер](../properties/props-system-media-metadatacontentprovider.md) | Имя поставщика содержимого метаданных. (Например, в коммерческой службе могут предоставляться метаданные.)                                                                                                 | VT \_ LPWSTR   |
| **\_Поставщик мультимедиа \_ PKEY**                                                | [System. Media. Producer](../properties/props-system-media-producer.md)                               | Имя производителя содержимого.                                                                                                                                                                      | VT \_ LPWSTR   |
| **\_Промотионурл носителя \_ PKEY**                                            | [System. Media. Промотионурл](../properties/props-system-media-promotionurl.md)                       | URL-адрес сайта, предлагающий продвижение, связанное с содержимым.                                                                                                                                             | VT \_ LPWSTR   |
| **\_Провидерратинг носителя \_ PKEY**                                          | [System. Media. Провидерратинг](../properties/props-system-media-providerrating.md)                   | Оценка содержимого, назначенного поставщиком содержимого метаданных.                                                                                                                                       | VT \_ LPWSTR   |
| **\_Провидерстиле носителя \_ PKEY**                                           | [System. Media. Провидерстиле](../properties/props-system-media-providerstyle.md)                     | Стиль или жанр содержимого, назначенный поставщиком содержимого метаданных.                                                                                                                               | VT \_ LPWSTR   |
| **\_Издатель носителя \_ PKEY**                                               | [System. Media. Publisher](../properties/props-system-media-publisher.md)                             | Издатель.                                                                                                                                                                                                | VT \_ LPWSTR   |
| **\_Подзаголовок носителя PKEY \_**                                                | [System. Media. подзаголовок](../properties/props-system-media-subtitle.md)                               | Подзаголовок.                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **\_Уникуефилеидентифиер носителя \_ PKEY**                                    | [System. Media. Уникуефилеидентифиер](../properties/props-system-media-uniquefileidentifier.md)       | Универсальная строка, которая может быть идентифицирована для файла.                                                                                                                                                        | VT \_ LPWSTR   |
| **\_ \_ Модуль записи мультимедиа PKEY**                                                  | [System. Media. Writer](../properties/props-system-media-writer.md)                                   | Средство.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **Номер \_ носителя \_ PKEY**                                                    | [System. Media. Year](../properties/props-system-media-year.md)                                       | Год публикации содержимого.                                                                                                                                                                           | VT \_ UI4      |
| **\_ \_ Албумартистная музыка PKEY**                                             | [System. Music. Албумартист](../properties/props-system-music-albumartist.md)                         | Основной исполнитель для альбома. Этот атрибут можно использовать для различения основного исполнителя альбома от исполнителя, который совместно работает с определенной дорожкой.                                            | VT \_ LPWSTR   |
| **\_ \_ Албумтитленая музыка PKEY**                                              | [System. Music. Албумтитле](../properties/props-system-music-albumtitle.md)                           | Название альбома.                                                                                                                                                                                              | VT \_ LPWSTR   |
| **" \_ Музыкальный \_ Исполнитель" PKEY**                                                  | [System. Music. исполнителя](../properties/props-system-music-artist.md)                                   | Исполнител.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **\_ \_ Беатсперминутеная музыка PKEY**                                          | [System. Music. Беатсперминуте](../properties/props-system-music-beatsperminute.md)                   | Число неритмов в минуту.                                                                                                                                                                                         | VT \_ LPWSTR   |
| **\_Композитор музыки для PKEY \_**                                                | [System. Music. Composer](../properties/props-system-music-composer.md)                               | Платформу.                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **\_Музыкальный \_ проводник PKEY**                                               | [System. Music. Проводник](../properties/props-system-music-conductor.md)                             | Выведен.                                                                                                                                                                                                | VT \_ LPWSTR   |
| **\_ \_ Контентграупдескриптионная музыка PKEY**                                 | [System. Music. Контентграупдескриптион](../properties/props-system-music-contentgroupdescription.md) | Описание группы содержимого (например, упакованный набор или ряд).                                                                                                                                      | VT \_ LPWSTR   |
| **\_Жанр для музыки на PKEY \_**                                                   | [System. Music. Жанр](../properties/props-system-music-genre.md)                                     | Название.                                                                                                                                                                                                    | VT \_ LPWSTR   |
| **\_ \_ Инитиалкэйная музыка PKEY**                                              | [System.Music.IniТиалкэй](../properties/props-system-music-initialkey.md)                           | Первоначальный ключ музыки.                                                                                                                                                                             | VT \_ LPWSTR   |
| **"Музыка" на PKEY \_ \_**                                           | [System. Music. компилятора](../properties/props-system-music-iscompilation.md)                     | Указывает, является ли музыкальный файл частью компиляции.                                                                                                                                                | Логическое значение VT \_     |
| **\_Музыкальные слова о песне PKEY \_**                                                  | [System. Music. песен](../properties/props-system-music-lyrics.md)                                   | Прилич.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **\_Настроение музыки для PKEY \_**                                                    | [System. Music. настроение](../properties/props-system-music-mood.md)                                       | Настроение.                                                                                                                                                                                                     | VT \_ LPWSTR   |
| **\_ \_ Партофсетная музыка PKEY**                                               | [System. Music. Партофсет](../properties/props-system-music-partofset.md)                             | Номер части и общее число частей в наборе, которому принадлежит файл, разделенные косой чертой.                                                                                                 | VT \_ LPWSTR   |
| **\_Период музыки на PKEY \_**                                                  | [System. музыка. period](../properties/props-system-music-period.md)                                   | Периода.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **\_ \_ Траккнумберная музыка PKEY**                                             | [System. Music. Траккнумбер](../properties/props-system-music-tracknumber.md)                         | Номер записи.                                                                                                                                                                                             | VT \_ UI4      |
| **PKEY \_ паренталратинг**                                                 | [System. Паренталратинг](../properties/props-system-parentalrating.md)                               | Родительский рейтинг.                                                                                                                                                                                          | VT \_ LPWSTR   |
| **PKEY \_ паренталратингреасон**                                           | [System. Паренталратингреасон](../properties/props-system-parentalratingreason.md)                   | Причины назначенной родительской оценки.                                                                                                                                                                 | VT \_ LPWSTR   |
| **\_Оценка PKEY**                                                         | [System. Оценка](../properties/props-system-rating.md)                                               | Оценка пользователей.                                                                                                                                                                                              | VT \_ UI4      |
| **PKEY \_ сумбнаилстреам**                                                | [System. Сумбнаилстреам](../properties/props-system-thumbnailstream.md)                             | Изображение эскиза.                                                                                                                                                                                          | \_поток VT   |
| **\_Название PKEY**                                                          | [System.Title](../properties/props-system-title.md)                                                 | Заголовок.                                                                                                                                                                                                    | VT \_ LPWSTR   |
| **\_Сжатие видео \_ PKEY**                                             | [System. видео. Compression](../properties/props-system-video-compression.md)                         | Подтип видео ([**\_ \_ подтип MF MT**](mf-mt-subtype-attribute.md)), выраженный в виде строки.                                                                                                                 | VT \_ LPWSTR   |
| **\_Директор видео \_ PKEY**                                                | [System. Video. режиссер](../properties/props-system-video-director.md)                               | Программу.                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **\_Енкодингбитрате видео о PKEY \_**                                         | [System. Video. Енкодингбитрате](../properties/props-system-video-encodingbitrate.md)                 | Средняя скорость видео в битах в секунду.                                                                                                                                                               | VT \_ UI4      |
| **\_Устройство "Video FourCC" PKEY \_**                                                  | [System. Video. FourCC](../properties/props-system-video-fourcc.md)                                   | Объект **FourCC** формата кодирования видео. Применяется только в том случае, если подтип видео может быть выражен как значение **FourCC** .                                                                                    | VT \_ UI4      |
| **\_Фрамехеигхт видео о PKEY \_**                                             | [System. Video. Фрамехеигхт](../properties/props-system-video-frameheight.md)                         | Высота кадра видео.                                                                                                                                                                                       | VT \_ UI4      |
| **Частота видеочастотного \_ видео PKEY \_**                                               | [System. Video. частота](../properties/props-system-video-framerate.md)                             | Частота кадров видео, выраженная в виде кадров в секунду × 1000.                                                                                                                                                  | VT \_ UI4      |
| **\_Фрамевидс видео о PKEY \_**                                              | [System. Video. Фрамевидс](../properties/props-system-video-framewidth.md)                           | Ширина кадра видео.                                                                                                                                                                                        | VT \_ UI4      |
| **\_Хоризонталаспектратио видео о PKEY \_**                                   | [System. Video. Хоризонталаспектратио](../properties/props-system-video-horizontalaspectratio.md)     | Горизонтальный компонент пропорций в пикселях. (Эквивалентно числителю атрибута [**\_ \_ \_ \_ соотношения пропорций MF-MT**](mf-mt-pixel-aspect-ratio-attribute.md) в типе носителя.)          | VT \_ UI4      |
| **Видео о PKEY \_ \_**                                                | [System. Video. стерео](/previous-versions//mt744507(v=vs.85))                                     | Указывает, содержит ли видеопоток видео стерео.                                                                                                                                         | Логическое значение VT \_     |
| **\_Стреамнумбер видео о PKEY \_**                                            | [System. Video. Стреамнумбер](../properties/props-system-video-streamnumber.md)                       | Идентификатор видеопотока.                                                                                                                                                                           | VT \_ UI4      |
| **\_Тоталбитрате видео о PKEY \_**                                            | [System. Video. Тоталбитрате](../properties/props-system-video-totalbitrate.md)                       | Общая скорость передачи данных для всех потоков видео и аудио в битах в секунду. (Применяется только к файлам, у которых хотя бы один поток видео.)                                                                              | VT \_ UI4      |
| **\_Вертикаласпектратио видео о PKEY \_**                                     | [System. Video. Вертикаласпектратио](../properties/props-system-video-verticalaspectratio.md)         | Вертикальный компонент пропорций в пикселях. (Эквивалентно знаменателю атрибута [**\_ \_ \_ \_ соотношения пропорций MF-MT**](mf-mt-pixel-aspect-ratio-attribute.md) в типе носителя.)          | VT \_ UI4      |



 

## <a name="media-sharing-properties"></a>Свойства общего доступа к носителю

Чтобы сделать файл мультимедиа совместимым с функцией общего доступа к мультимедиа, обработчик свойств должен предоставить следующие свойства метаданных. Эти свойства позволяют службе общего доступа к мультимедиа предлагать правильные варианты перекодирования содержимого в различные форматы или скорости.

-   [\_ \_ \_ Идентификатор профиля DLNA для содержимого мфпкэй \_](mfpkey-content-dlna-profile-id.md)
-   **PKEY \_ Audio \_ чаннелкаунт**
-   **PKEY \_ Audio \_ енкодингбитрате**
-   **\_Звуковой \_ Формат PKEY**
-   **PKEY \_ Audio \_ SampleRate** (необязательно)
-   **PKEY \_ Audio \_ SampleSize** (необязательно)
-   **PKEY \_ \_Защита DRM** (требуется для содержимого DRM)
-   **\_Длительность носителя \_ PKEY**
-   **\_Сжатие видео \_ PKEY**
-   **\_Енкодингбитрате видео о PKEY \_**
-   **\_Устройство "Video FourCC" PKEY \_**
-   **\_Фрамехеигхт видео о PKEY \_**
-   **PKEY \_ \_Частота видео** (необязательно)
-   **\_Фрамевидс видео о PKEY \_**
-   **\_Тоталбитрате видео о PKEY \_**

Если содержимое защищено с помощью DRM, требуется свойство с защитой **\_ DRM \_** . В противном случае это свойство является необязательным.

Свойства **\_ \_ частоты** **\_ аудиопотока Audio \_ SampleRate**, **PKEY \_ Audio \_ SampleSize** и PKEY не являются обязательными. Служба общего доступа к мультимедиа будет предоставлять их, если они доступны.

Свойства в **звуковой группе "PKEY" \_ \_ \* *применяются только к файлам с аудио-потоком, а свойства в* Видеогруппе _ \_ PKEY \_ \*** применяются только к файлам с видеопотоком.

## <a name="windows-media-format-sdk-mappings"></a>Сопоставления пакета SDK Windows Media Format

Источник мультимедиа ASF сопоставляет следующие ключи свойств с атрибутами заголовка ASF. В некоторых случаях типы данных различаются свойством Shell и атрибутом Format SDK.



| PROPERTYKEY                              | Формат атрибута пакета SDK                                                  |
|------------------------------------------|-----------------------------------------------------------------------|
| **PKEY \_ Audio \_ исвариаблебитрате**       | [**исвбр**](../wmformat/isvbr.md)                                           |
| **PKEY \_ Audio \_ пеаквалуе**               | [**пеаквалуе**](../wmformat/peakvalue.md)                                   |
| **\_Автор PKEY**                         | [**Автор**](../wmformat/author.md)                                         |
| **\_Комментарий PKEY**                        | [**Описание**](../wmformat/description.md)                               |
| **\_Авторские права PKEY**                      | [**Информация**](../wmformat/copyright.md)                                   |
| **\_Защита управления правами на PKEY \_**               | [**\_Защищено**](../wmformat/is-protected.md)                            |
| **\_Ключевые слова PKEY**                       | [**WM/Category**](../wmformat/wm-category.md)                               |
| **\_Язык PKEY**                       | [**WM/Language**](../wmformat/wm-language.md)                               |
| **\_Аусорурл носителя \_ PKEY**               | [**WM/Аусорурл**](../wmformat/wm-authorurl.md)                             |
| **\_Аверажелевел носителя \_ PKEY**            | [**аверажелевел**](../wmformat/averagelevel.md)                             |
| **\_Класспримарид носителя \_ PKEY**          | [**WM/Медиакласспримарид**](../wmformat/wm-mediaprimaryid.md)              |
| **\_Класссекондарид носителя \_ PKEY**        | [**WM/Медиакласссекондарид**](../wmformat/wm-mediasecondaryid.md)          |
| **\_Коллектионграупид носителя \_ PKEY**       | [**WM/Вмколлектионграупид**](../wmformat/wm-wmcollectiongroupid.md)         |
| **\_CollectionID носителя \_ PKEY**            | [**WM/Вмколлектионид**](../wmformat/wm-wmcollectionid.md)                   |
| **\_Контентдистрибутор носителя \_ PKEY**      | [**WM/Контентдистрибутор**](../wmformat/wm-contentdistributor.md)           |
| **Идентификатор \_ ContentID носителя "PKEY" \_**               | [**WM/Вмконтентид**](../wmformat/wm-wmcontentid.md)                         |
| **\_Датинкодед носителя \_ PKEY**             | [**WM/Енкодингтиме**](../wmformat/wm-encodingtime.md)                       |
| **\_Датерелеасед носителя \_ PKEY**            | [**WM/Оригиналрелеасетиме**](../wmformat/wm-originalreleasetime.md)         |
| **\_Двдид носителя \_ PKEY**                   | [**WM/ДВДИД**](../wmformat/wm-dvdid.md)                                     |
| **\_Енкодедби носителя \_ PKEY**               | [**WM/Енкодедби**](../wmformat/wm-encodedby.md)                             |
| **\_Енкодингсеттингс носителя \_ PKEY**        | [**WM/Енкодингсеттингс**](../wmformat/wm-encodingsettings.md)               |
| **\_Мкди носителя \_ PKEY**                    | [**WM/МКДИ**](../wmformat/wm-mcdi.md)                                       |
| **\_Метадатаконтентпровидер носителя \_ PKEY** | [**WM/provider**](../wmformat/wm-provider.md)                               |
| **\_Поставщик мультимедиа \_ PKEY**                | [**WM/Producer**](../wmformat/wm-producer.md)                               |
| **\_Промотионурл носителя \_ PKEY**            | [**WM/Промотионурл**](../wmformat/wm-promotionurl.md)                       |
| **\_Провидерратинг носителя \_ PKEY**          | [**WM/Провидерратинг**](../wmformat/wm-providerrating.md)                   |
| **\_Провидерстиле носителя \_ PKEY**           | [**WM/Провидерстиле**](../wmformat/wm-providerstyle.md)                     |
| **\_Издатель носителя \_ PKEY**               | [**WM/Publisher**](../wmformat/wm-publisher.md)                             |
| **\_Подзаголовок носителя PKEY \_**                | [**WM/Субтитледескриптион**](../wmformat/wm-subtitledescription.md)         |
| **\_Уникуефилеидентифиер носителя \_ PKEY**    | [**WM/Уникуефилеидентифиер**](../wmformat/wm-uniquefileidentifier.md)       |
| **\_ \_ Модуль записи мультимедиа PKEY**                  | [**WM/Writer**](../wmformat/wm-writer.md)                                   |
| **Номер \_ носителя \_ PKEY**                    | [**WM/year**](../wmformat/wm-year.md)                                       |
| **\_ \_ Албумартистная музыка PKEY**             | [**WM/Албумартист**](../wmformat/wm-albumartist.md)                         |
| **\_ \_ Албумтитленая музыка PKEY**              | [**WM/Албумтитле**](../wmformat/wm-albumtitle.md)                           |
| **" \_ Музыкальный \_ Исполнитель" PKEY**                  | [**Автор**](../wmformat/author.md)                                         |
| **\_ \_ Беатсперминутеная музыка PKEY**          | [**WM/Беатсперминуте**](../wmformat/wm-beatsperminute.md)                   |
| **\_Композитор музыки для PKEY \_**                | [**WM/Composer**](../wmformat/wm-composer.md)                               |
| **\_Музыкальный \_ проводник PKEY**               | [**WM/проводник**](../wmformat/wm-conductor.md)                             |
| **\_ \_ Контентграупдескриптионная музыка PKEY** | [**WM/Контентграупдескриптион**](../wmformat/wm-contentgroupdescription.md) |
| **\_Жанр для музыки на PKEY \_**                   | [**WM/жанр**](../wmformat/wm-genre.md)                                     |
| **\_ \_ Инитиалкэйная музыка PKEY**              | [**WM/Инитиалкэй**](../wmformat/wm-initialkey.md)                           |
| **"Музыка" на PKEY \_ \_**           | **WM/compilation**                                                  |
| **\_Музыкальные слова о песне PKEY \_**                  | [**WM/песни**](../wmformat/wm-lyrics.md)                                   |
| **\_Настроение музыки для PKEY \_**                    | [**WM/настроение**](../wmformat/wm-mood.md)                                       |
| **\_ \_ Партофсетная музыка PKEY**               | [**WM/Партофсет**](../wmformat/wm-partofset.md)                             |
| **\_Период музыки на PKEY \_**                  | [**WM/period**](../wmformat/wm-period.md)                                   |
| **\_ \_ Траккнумберная музыка PKEY**             | [**WM/Траккнумбер**](../wmformat/wm-tracknumber.md)                         |
| **PKEY \_ паренталратинг**                 | [**WM/Паренталратинг**](../wmformat/wm-parentalrating.md)                   |
| **PKEY \_ паренталратингреасон**           | [**WM/Паренталратингреасон**](../wmformat/wm-parentalratingreason.md)       |
| **\_Оценка PKEY**                         | [**WM/Шаредусерратинг**](../wmformat/wm-shareduserrating.md)               |
| **PKEY \_ сумбнаилстреам**                | [**WM/Picture**](../wmformat/wmpicture.md)                       |
| **\_Название PKEY**                          | [**Заголовок**](../wmformat/title.md)                                           |
| **\_Директор видео \_ PKEY**                | [**WM/Director**](../wmformat/wm-director.md)                               |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Метаданные мультимедиа](media-metadata.md)
</dt> <dt>

[Поставщики метаданных оболочки](shell-metadata-providers.md)
</dt> </dl>

 

 
