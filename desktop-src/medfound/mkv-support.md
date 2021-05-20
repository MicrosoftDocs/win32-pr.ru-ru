---
description: В этом разделе описывается поддержка Media Foundation для файлов контейнера мультимедиа матроска (MKV).
title: Поддержка контейнера мультимедиа матроска (MKV)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd860f58087bc8a0f3fe95d278bfa81edc412d0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2021
ms.locfileid: "110154223"
---
# <a name="matroska-media-container-mkv-support"></a>Поддержка контейнера мультимедиа матроска (MKV)

В этом разделе описывается поддержка Media Foundation для файлов контейнера мультимедиа матроска (MKV).

Формат MKV может поддерживать несколько видеокодеков и аудиокодеков, таких как H. 264 и AAC Audio. В общем случае контейнеры описывают, как располагаются видео и звуковые данные и какие дополнительные сведения используются для описания этих потоков/V. Контейнеры также могут включать данные, дополняющие потоки/V, такие как название, языки звуковых потоков, подзаголовок или подзаголовки, шрифты для этих субтитров, изображения, сведения о разделах и меню. MKV — это очень гибкий формат, поддерживающий многие из этих функций контейнера. Дополнительные сведения о формате MKV см. в разделе. [https://matroska.org](https://matroska.org/)


## <a name="mkv-container-feature-support"></a>Поддержка функций контейнеров MKV
Функции контейнера MKV поддерживаются в Media Foundation следующими способами.
- При наличии одной или нескольких видеодорожек будет воспроизводиться первая дорожка.
- Если имеется одна или несколько звуковых дорожек, будет воспроизводиться первая дорожка.
- Записи субтитров поддерживаются, но не выбираются (воспроизводятся) по умолчанию.
- Если имеется один или несколько шрифтов или изображений, то заголовки и изображения не будут отображаться, хотя файл будет загружен и воспроизведен.
- Сведения о меню не поддерживаются и не отображаются, но файл будет загружен и воспроизведен.
- Если файлы с главами относятся к дополнительным файлам, дополнительные файлы не воспроизводятся.
- Миниатюрные изображения доступны при просмотре файлов на USB-накопителях с помощью обозревателя файлов.

Этот набор функций должен позволять воспроизводить большинство файлов MKV, если они содержат поддерживаемые кодеки.
Поддерживаются файлы MKV, содержащие видео и звуковые дорожки, закодированные с помощью кодеков, перечисленных в следующем разделе.

## <a name="supported-mkv-codecs"></a>Поддерживаемые кодеки MKV

### <a name="video-codec-support-for-mkv"></a>Поддержка видеокодеков для MKV

Идентификатор матроска: V_MPEG4/ИСО/АВК

- Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_H264
- Описание: H. 264 Video
- Идентификаторы FourCC или WAV: H264 Single bitrate

Идентификатор матроска: V_MPEG2

- Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_MPEG2
- Описание: видео MPEG-2

Идентификатор матроска: V_MPEG1

- Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_MPG1
- Описание: видео MPEG-1
- Идентификаторы FourCC или WAV: MPG1

Идентификатор матроска: V_MPEG4/MS/V3

- Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_MP43
- Описание: кодек Microsoft MPEG 4 версии 3
- Идентификаторы FourCC или WAV: MP43

Идентификатор матроска: V_MPEG4/ИСО/АСП

- Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Описание: видео MPEG-4 Part 2
- Идентификаторы FourCC или WAV: MP4V

Идентификатор матроска: V_MS/ВФВ/ФАУРКК

- Описание: сопоставляется с несколькими кодеками, которые обычно поддерживаются в формате AVI, доступном в консоли.

Идентификатор матроска: V_THEORA

- Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_Theora
- Описание: Сеора
- Идентификаторы FourCC или WAV: Сео

Идентификатор матроска: V_MPEG4/ИСО/СП

- Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Описание: простой профиль ISO MPEG4 (DivX4)
- Идентификаторы FourCC или WAV: MP4V

Идентификатор матроска: V_MPEG4/ИСО/ап

- Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Описание: Расширенный простой профиль MPEG4 ISO (DivX5, Ксвид, FFMPEG)
- Идентификаторы FourCC или WAV: MP4V


Идентификатор матроска: V_MPEGH/ИСО/ХЕВК 

- Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_HEVC
- Описание: HEVC/H. 265
- Идентификаторы FourCC или WAV: 

Идентификатор матроска: V_VP8

- Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_VP80
- Описание: формат кодека VP8
- Идентификаторы FourCC или WAV: VP80

Идентификатор матроска: V_VP9

- Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_VP90
- Описание: формат кодека VP9
- Идентификаторы FourCC или WAV: VP90

Идентификатор матроска: V_MJPEG

- Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_MJPG
- Описание: перемещение в формате JPEG
- Идентификаторы FourCC или WAV: МЖПГ

Идентификатор матроска: V_AV1

- Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_AV1
- Описание: Аомедиа видео 1
- Идентификаторы FourCC или WAV: AV01

### <a name="audio-codec-support-for-mkv"></a>Поддержка аудиокодеков для MKV

Идентификатор матроска: A_AAC

- Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_AAC
- Описание: расширенное аудио кодирование (AAC)
- Идентификаторы FourCC или WAV: WAVE_FORMAT_MPEG_HEAAC

Идентификатор матроска: A_AC3

- Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3
- Описание: Dolby AC3
- Идентификаторы FourCC или WAV: WAVE_FORMAT_DOLBY_AC3_SPDIF

Идентификатор матроска: A_MPEG/L3

- Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_MP3
- Описание: MPEG Audio Layer-3 (MP3)
- Идентификаторы FourCC или WAV: WAVE_FORMAT_MPEGLAYER3

Идентификатор матроска: A_MPEG/L1

- Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_MPEG
- Описание: полезные данные звука MPEG-1
- Идентификаторы FourCC или WAV: WAVE_FORMAT_MPEG

Идентификатор матроска: A_PCM/Инт/Биг

- Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_PCM
- Описание: несжатая звукозапись PCM
- Идентификаторы FourCC или WAV: WAVE_FORMAT_PCM

Идентификатор матроска: A_PCM/Инт/лит

- Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_PCM
- Описание: несжатая звукозапись PCM
- Идентификаторы FourCC или WAV: WAVE_FORMAT_PCM

Идентификатор матроска: A_PCM/ФЛОАТ/ИИЕ

- Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_Float
- Описание: несжатое аудио с плавающей запятой IEEE
- Идентификаторы FourCC или WAV: WAVE_FORMAT_IEEE_FLOAT

Идентификатор матроска: A_ALAC

- Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_ALAC
- Описание: аудиокодек Apple без звука
- Идентификаторы FourCC или WAV: 

Идентификатор матроска: A_MPEG/L2

- Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_MPEG
- Описание: MPEG Audio 1, 2 Layer II
- Идентификаторы FourCC или WAV: WAVE_FORMAT_MPEG

Идентификатор матроска: A_DTS

- Media Foundation MSFT MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD
- Описание: система Digital режим театра System
- Идентификаторы FourCC или WAV: WAVE_FORMAT_DTS

Идентификатор матроска: A_OPUS

- Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_Opus
- Описание: опус
- Идентификаторы FourCC или WAV: WAVE_FORMAT_OPUS

Идентификатор матроска: A_VORBIS

- Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_Vorbis
- Описание: Vorbis
- Идентификаторы FourCC или WAV: 

Идентификатор матроска: A_FLAC

- Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_FLAC
- Описание: бесплатный аудиокодек без потерь
- Идентификаторы FourCC или WAV: WAVE_FORMAT_FLAC

Идентификатор матроска: A_AAC/MAIN

- Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_AAC
- Описание: расширенное аудио кодирование (AAC)
- Идентификаторы FourCC или WAV: WAVE_FORMAT_MPEG_HEAAC

Идентификатор матроска: A_EAC3

- Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus
- Описание: Расширенный AC-3
- Идентификаторы FourCC или WAV: 

Идентификатор матроска: A_TRUEHD

- Media Foundation MSFT MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD
- Описание: Dolby Труехд
- Идентификаторы FourCC или WAV: 

Идентификатор матроска: A_MS/АКМ

- MSFT Media Foundation MF_MT_SUBTYPE: сопоставляется с несколькими WAVE_FORMAT звуковыми типами, определенными в ммрег. h


### <a name="subtitles-codec-support-for-mkv"></a>Поддержка кодеков субтитров для MKV

Идентификатор матроска: S_TEXT/АСЦИИ

- Media Foundation MSFT MF_MT_SUBTYPE: MFSubtitleFormat_SRT
- Описание: текст ASCII

Идентификатор матроска: S_TEXT/UTF8

- Media Foundation MSFT MF_MT_SUBTYPE: MFSubtitleFormat_SRT
- Описание: обычный текст в кодировке UTF-8

Идентификатор матроска: S_TEXT/ССА

- Media Foundation MSFT MF_MT_SUBTYPE: MFSubtitleFormat_SSA
- Описание: формат субтитров

Идентификатор матроска: S_TEXT/АСС

- Media Foundation MSFT MF_MT_SUBTYPE: MFSubtitleFormat_SSA
- Описание: формат расширенных субтитров

Идентификатор матроска: S_VOBSUB

- Media Foundation MSFT MF_MT_SUBTYPE: MFSubtitleFormat_VobSub
- Описание: субтитры Вобсуб

Идентификатор матроска: S_HDMV/ПГС

- Media Foundation MSFT MF_MT_SUBTYPE: MFSubtitleFormat_PGS
- Описание: ХДМВ презентации субтитры графики (ПГС)


## <a name="technical-details-regarding-codecs"></a>Технические сведения о кодеках

Технические сведения о кодеках см. в следующих статьях.

- [Спецификации кодека матроска](http://www.matroska.org/technical/specs/codecid/index.html)
- [Идентификаторы GUID для подтипов звука](audio-subtype-guids.md)
- [Идентификаторы GUID для подтипов видео](video-subtype-guids.md)


## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Поддерживаемые форматы мультимедиа в Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Media Foundationое программное руководством](media-foundation-programming-guide.md)
</dt> </dl>

 

 



