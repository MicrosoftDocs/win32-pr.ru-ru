---
description: '\_ \_ Тип перечисления мета-жанры WPD описывает широкий тип жанра файла мультимедиа.'
ms.assetid: a69cab70-5a45-4e75-abbd-230396c2b5ec
title: Перечисление WPD_META_GENRES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_META_GENRES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f6ff4875474776df1e2436e0209e6d863f5b3e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694694"
---
# <a name="wpd_meta_genres-enumeration"></a>\_Перечисление метах meta WPD \_

Тип **перечисления \_ мета- \_ жанры WPD** описывает широкий тип жанра файла мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WPD_META_GENRES { 
  WPD_META_GENRE_UNUSED                            = 0x0,
  WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE          = 0x1,
  WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE      = 0x11,
  WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES      = 0x12,
  WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK  = 0x13,
  WPD_META_GENRE_SPOKEN_WORD_NEWS                  = 0x14,
  WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS            = 0x15,
  WPD_META_GENRE_GENERIC_VIDEO_FILE                = 0x21,
  WPD_META_GENRE_NEWS_VIDEO_FILE                   = 0x22,
  WPD_META_GENRE_MUSIC_VIDEO_FILE                  = 0x23,
  WPD_META_GENRE_HOME_VIDEO_FILE                   = 0x24,
  WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE           = 0x25,
  WPD_META_GENRE_TELEVISION_VIDEO_FILE             = 0x26,
  WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE   = 0x27,
  WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE          = 0x28,
  WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO       = 0x30,
  WPD_META_GENRE_AUDIO_PODCAST                     = 0x40,
  WPD_META_GENRE_VIDEO_PODCAST                     = 0x41,
  WPD_META_GENRE_MIXED_PODCAST                     = 0x42
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**\_ \_ неиспользуемый мета жанр WPD \_**
</dt> <dd>

Жанр не задан или неприменим.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**\_ \_ \_ универсальный \_ музыкальный \_ \_ файл для мета жанра WPD**
</dt> <dd>

Это универсальный музыкальный файл (только Audio).

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**\_Универсальный музыкальный \_ \_ \_ \_ \_ \_ файл для мета жанра WPD**
</dt> <dd>

Это универсальный файл, не являющийся музыкальным, например, речь или звуковая книга.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**\_мета — \_ Жанр meta, произнесенный в формате \_ \_ Word \_ Audio \_ Book \_ Files**
</dt> <dd>

Это файл звуковой книги.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**WPD \_ meta « \_ Жанр» \_ \_ файлы Word, \_ \_ \_ незвуковая \_ Книга**
</dt> <dd>

Это звуковой файл голосового слова, который не является звуковой книгой, например собеседованием или речевым документом.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**\_Новости о \_ \_ \_ слове meta «жанр» \_**
</dt> <dd>

Это звуковой файл новостей или видеофайл.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**\_мета \_ — жанр, \_ произнесенный в Word, \_ \_ говорит \_**
</dt> <dd>

Это звуковая запись для разговора.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**\_ \_ \_ универсальный видеофайл мета жанра WPD \_ \_**
</dt> <dd>

Это универсальный видеофайл.

</dd> <dt>

<span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**\_видеофайл новостей по мета \_ ЖАНРам WPD \_ \_ \_**
</dt> <dd>

Это видеофайл новостей.

</dd> <dt>

<span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**\_ \_ \_ файл музыкального \_ видео по мета жанра WPD \_**
</dt> <dd>

Это видеофайл музыки.

</dd> <dt>

<span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**\_ \_ \_ \_ файл домашнего видео для мета жанра WPD \_**
</dt> <dd>

Это файл домашней видеозаписи.

</dd> <dt>

<span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**\_видеоролик meta « \_ жанр», \_ \_ пофильмный \_ \_ видеофайл**
</dt> <dd>

Это видеофайл с эффектом «пленка».

</dd> <dt>

<span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**\_видеофайл мета \_ ЖАНРа WPD \_ \_ \_**
</dt> <dd>

Это видеофайл программы телепередач.

</dd> <dt>

<span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**видеофайл учебного \_ курса по мета \_ ЖАНРам WPD \_ \_ \_ \_**
</dt> <dd>

Это файл учебных видеороликов.

</dd> <dt>

<span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**\_видеофайл мета \_ Жанр \_ фото \_ монтаже \_ Video \_**
</dt> <dd>

Это видеофайл, содержащий фотографию монтаже.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**\_ \_ \_ универсальный \_ \_ неаудио \_ не \_ видео по мета жанра WPD**
</dt> <dd>

Это файл без аудио или видео.

</dd> <dt>

<span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**\_ \_ \_ аудио подкаст по мета жанру WPD \_**
</dt> <dd>

Это звуковая подкаст.

</dd> <dt>

<span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**\_видеоматериалы по мета \_ ЖАНРу WPD \_ \_**
</dt> <dd>

Это видеоролик.

</dd> <dt>

<span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**\_ \_ \_ смешанная оцифрованная ВИДЕОжанра WPD \_**
</dt> <dd>

Это подкаст, содержащий аудио и видео.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление используется свойством " [ \_ meta- \_ \_ Жанр мультимедиа WPD](media-properties.md) ".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




