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
# <a name="wpd_meta_genres-enumeration"></a><span data-ttu-id="ecbe7-103">\_Перечисление метах meta WPD \_</span><span class="sxs-lookup"><span data-stu-id="ecbe7-103">WPD\_META\_GENRES enumeration</span></span>

<span data-ttu-id="ecbe7-104">Тип **перечисления \_ мета- \_ жанры WPD** описывает широкий тип жанра файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-104">The **WPD\_META\_GENRES** enumeration type describes a broad genre type of a media file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecbe7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecbe7-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="ecbe7-106">Константы</span><span class="sxs-lookup"><span data-stu-id="ecbe7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ecbe7-107"><span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**\_ \_ неиспользуемый мета жанр WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-107"><span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**WPD\_META\_GENRE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-108">Жанр не задан или неприменим.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-108">The genre has not been set, or is not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-109"><span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**\_ \_ \_ универсальный \_ музыкальный \_ \_ файл для мета жанра WPD**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-109"><span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**WPD\_META\_GENRE\_GENERIC\_MUSIC\_AUDIO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-110">Это универсальный музыкальный файл (только Audio).</span><span class="sxs-lookup"><span data-stu-id="ecbe7-110">This is a generic music file (audio only).</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-111"><span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**\_Универсальный музыкальный \_ \_ \_ \_ \_ \_ файл для мета жанра WPD**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-111"><span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**WPD\_META\_GENRE\_GENERIC\_NON\_MUSIC\_AUDIO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-112">Это универсальный файл, не являющийся музыкальным, например, речь или звуковая книга.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-112">This is a generic non-music audio file, for example, a speech or audio book.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-113"><span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**\_мета — \_ Жанр meta, произнесенный в формате \_ \_ Word \_ Audio \_ Book \_ Files**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-113"><span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_AUDIO\_BOOK\_FILES**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-114">Это файл звуковой книги.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-114">This is an audio book file.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-115"><span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**WPD \_ meta « \_ Жанр» \_ \_ файлы Word, \_ \_ \_ незвуковая \_ Книга**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-115"><span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_FILES\_NON\_AUDIO\_BOOK**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-116">Это звуковой файл голосового слова, который не является звуковой книгой, например собеседованием или речевым документом.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-116">This is a spoken-word audio file that is not an audio book, for example, an interview or speech.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-117"><span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**\_Новости о \_ \_ \_ слове meta «жанр» \_**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-117"><span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_NEWS**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-118">Это звуковой файл новостей или видеофайл.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-118">This is a news audio or video file.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-119"><span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**\_мета \_ — жанр, \_ произнесенный в Word, \_ \_ говорит \_**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-119"><span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_TALK\_SHOWS**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-120">Это звуковая запись для разговора.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-120">This is an audio recording of a talk show.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-121"><span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**\_ \_ \_ универсальный видеофайл мета жанра WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-121"><span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**WPD\_META\_GENRE\_GENERIC\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-122">Это универсальный видеофайл.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-122">This is a generic video file.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-123"><span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**\_видеофайл новостей по мета \_ ЖАНРам WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-123"><span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**WPD\_META\_GENRE\_NEWS\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-124">Это видеофайл новостей.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-124">This is a news video file.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-125"><span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**\_ \_ \_ файл музыкального \_ видео по мета жанра WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-125"><span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**WPD\_META\_GENRE\_MUSIC\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-126">Это видеофайл музыки.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-126">This is a music video file.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-127"><span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**\_ \_ \_ \_ файл домашнего видео для мета жанра WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-127"><span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**WPD\_META\_GENRE\_HOME\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-128">Это файл домашней видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-128">This is a home video file.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-129"><span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**\_видеоролик meta « \_ жанр», \_ \_ пофильмный \_ \_ видеофайл**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-129"><span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**WPD\_META\_GENRE\_FEATURE\_FILM\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-130">Это видеофайл с эффектом «пленка».</span><span class="sxs-lookup"><span data-stu-id="ecbe7-130">This is a feature film video file.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-131"><span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**\_видеофайл мета \_ ЖАНРа WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-131"><span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**WPD\_META\_GENRE\_TELEVISION\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-132">Это видеофайл программы телепередач.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-132">This is a television program video file.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-133"><span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**видеофайл учебного \_ курса по мета \_ ЖАНРам WPD \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-133"><span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**WPD\_META\_GENRE\_TRAINING\_EDUCATIONAL\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-134">Это файл учебных видеороликов.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-134">This is an educational video file.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-135"><span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**\_видеофайл мета \_ Жанр \_ фото \_ монтаже \_ Video \_**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-135"><span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**WPD\_META\_GENRE\_PHOTO\_MONTAGE\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-136">Это видеофайл, содержащий фотографию монтаже.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-136">This is a video file featuring a photo montage.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-137"><span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**\_ \_ \_ универсальный \_ \_ неаудио \_ не \_ видео по мета жанра WPD**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-137"><span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**WPD\_META\_GENRE\_GENERIC\_NON\_AUDIO\_NON\_VIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-138">Это файл без аудио или видео.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-138">This is a file without audio or video.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-139"><span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**\_ \_ \_ аудио подкаст по мета жанру WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-139"><span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**WPD\_META\_GENRE\_AUDIO\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-140">Это звуковая подкаст.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-140">This is an audio podcast.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-141"><span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**\_видеоматериалы по мета \_ ЖАНРу WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-141"><span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**WPD\_META\_GENRE\_VIDEO\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-142">Это видеоролик.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-142">This is a video podcast.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe7-143"><span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**\_ \_ \_ смешанная оцифрованная ВИДЕОжанра WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-143"><span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**WPD\_META\_GENRE\_MIXED\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="ecbe7-144">Это подкаст, содержащий аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-144">This is a podcast containing both audio and video.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecbe7-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ecbe7-145">Remarks</span></span>

<span data-ttu-id="ecbe7-146">Это перечисление используется свойством " [ \_ meta- \_ \_ Жанр мультимедиа WPD](media-properties.md) ".</span><span class="sxs-lookup"><span data-stu-id="ecbe7-146">This enumeration is used by the [WPD\_MEDIA\_META\_GENRE](media-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecbe7-147">Требования</span><span class="sxs-lookup"><span data-stu-id="ecbe7-147">Requirements</span></span>



| <span data-ttu-id="ecbe7-148">Требование</span><span class="sxs-lookup"><span data-stu-id="ecbe7-148">Requirement</span></span> | <span data-ttu-id="ecbe7-149">Значение</span><span class="sxs-lookup"><span data-stu-id="ecbe7-149">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecbe7-150">Header</span><span class="sxs-lookup"><span data-stu-id="ecbe7-150">Header</span></span><br/> | <dl> <span data-ttu-id="ecbe7-151"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecbe7-151"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecbe7-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecbe7-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecbe7-153">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="ecbe7-153">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




