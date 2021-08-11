---
description: В разделе содержится перечень форматов мультимедиа, которые Microsoft Media Foundation поддерживает изначально.
ms.assetid: 69c12a28-4b58-4979-b4d8-ae37efa847fe
title: Поддерживаемые форматы мультимедиа в Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ecbc5024ab70e9e0bdd07d6213ad9779c21e2b7f34f10f3e2d3fe538a784734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238193"
---
# <a name="supported-media-formats-in-media-foundation"></a>Поддерживаемые форматы мультимедиа в Media Foundation

В разделе содержится перечень форматов мультимедиа, которые Microsoft Media Foundation поддерживает изначально. Сторонние лица могут поддерживать дополнительные форматы, создавая пользовательские подключаемые модули.

## <a name="file-containers"></a>Контейнеры файлов



| Формат                                           | Расширения файлов          | Источник мультимедиа                                 | Приемник мультимедиа                                   | Требования                                                              |
|--------------------------------------------------|--------------------------|----------------------------------------------|----------------------------------------------|-----------------------------------------------------------------------|
| 3GP                                              | .3G2,. 3GP,. 3GP2,. 3GPP | [Источник файла MPEG-4](mpeg-4-file-source.md) | Приемник файла 3GP                                | Windows 7                                                             |
| Расширенный формат потоковой передачи (ASF)                  | . ASF,. WMA,. WMV         | [Источник носителя ASF](asf-media-source.md)     | [Приемник мультимедиа ASF](asf-media-sinks.md)        | Windows Vista                                                         |
| Поток транспорта аудиоданных (ADTS).              | . AAC,. ADTs              | Источник файла ADTS                             | None                                         | Windows 7                                                             |
| AVI                                              | .avi                     | Источник файла AVI                              | None                                         | Windows 7                                                             |
| MP3                                              | .mp3                     | [**Источник MP3-файла**](mp3-file-source.md)   | Приемник файлов в формате MP3                                | источник файла: Windows Vista<br/> приемник файла: Windows 7<br/> |
| MPEG-4                                           | . m4a,. m4v,. mov, .mp4   | [Источник файла MPEG-4](mpeg-4-file-source.md) | [**Приемник файлов MPEG-4**](mpeg-4-file-sink.md) | Windows 7                                                             |
| Синхронизированный доступный медиа-обмен (SAMI) | . samid,. SMI              | [Источник носителя SAMI](sami-media-source.md)   | None                                         | Windows Vista                                                         |
| ЗВУКОВ                                             | .wav                     | Источник файла AVI                              | None                                         | Windows 7                                                             |



 

## <a name="audio-codecs"></a>Аудиокодеки



| Формат                                              | Показан                                                                                                                                                          | Кодировщик                                                                                                                                                          | Требования      |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| μное написание закона                                        | Μ-кодек диспетчера аудиосжатия (ACM)                                                                                                                      | None                                                                                                                                                             | Windows Vista |
| Адаптивное разностное импульсное программное средство модуляции (ADPCM) | Кодек ADPCM ACM                                                                                                                                                  | None                                                                                                                                                             | Windows Vista |
| Расширенное аудио кодирование (AAC)                         | [**Декодер AAC**](aac-decoder.md)                                                                                                                               | [**Кодировщик AAC**](aac-encoder.md)                                                                                                                               | Windows 7     |
| MP3                                                 | [**Windows Декодер MP3 Media**](windows-media-mp3-decoder.md)                                                                                                   | None                                                                                                                                                             | Windows Vista |
| GSM 6.10                                            | Кодек ACM GSM 6,10                                                                                                                                               | None                                                                                                                                                             | Windows Vista |
| Звуковые файлы в формате WMA                           | [**Windows Декодер мультимедиа**](windowsmediaaudiodecoder.md)<br/> [**Windows Декодер мультимедиа аудио**](windowsmediaaudiovoicedecoder.md)<br/> | [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md)<br/> [**Windows Кодировщик Media Audio Voice**](windowsmediaaudiovoiceencoder.md)<br/> | Windows Vista |



 

> [!Note]  
> Media Foundation предоставляет оболочки для нескольких кодеков ACM, перечисленных в предыдущей таблице. Однако Media Foundation не поддерживает произвольные кодеки ACM.

 

## <a name="video-codecs"></a>Видеокодеки



| Формат                                                                                                         | Показан                                                                                                                                                                  | Кодировщик                                                                                                                             | Требования      |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Видео DV                                                                                                       | [**Видеодекодер DV**](dv-video-decoder.md)                                                                                                                             | None                                                                                                                                | Windows 7     |
| H.264                                                                                                          | [**Декодер видео H. 264**](h-264-video-decoder.md)                                                                                                                       | [**Кодировщик видео H. 264**](h-264-video-encoder.md)                                                                                  | Windows 7     |
| H.263<br/> (H. 264, базовый профиль, совместимый с MPEG-4 PT2 короткий режим заголовков видео)<br/> | [**Видеодекодер MPEG-4 Part 2**](mpeg4part2videodecoder.md)                                                                                                            | None                                                                                                                                | Windows 8     |
| мжпег                                                                                                          | Декодер МЖПЕГ                                                                                                                                                            | None                                                                                                                                | Windows 7     |
| MPEG-4, часть 2                                                                                                  | [**Видеодекодер MPEG-4 Part 2**](mpeg4part2videodecoder.md)                                                                                                            | None                                                                                                                                | Windows 7     |
| MPEG-4 v1/v2/v3                                                                                                | [**Windows Декодер Media MPEG-4 v3**](./windowsmediampeg4v3decoder.md)<br/> [**Windows Декодер Media MPEG4 v1/v2**](windowsmediampeg4decoder.md)<br/>         | None                                                                                                                                | Windows Vista |
| Видеофайлы в формате WMV                                                                                      | [**Windows Декодер Media Video 9**](windowsmediavideo9decoder.md)<br/> [**Windows Экранный декодер видео 9**](windowsmediavideo9screendecoder.md)<br/> | Windows Кодировщик Media Video 9<br/> Windows Кодировщик экрана видео в Media 9<br/> Windows Кодировщик Media Video 7/8<br/> | Windows Vista |



 

> [!Note]  
> В столбце "требуется" перечислены минимальные операционные системы, необходимые для использования этих кодеков в приложении Media Foundation. некоторые из этих кодеков появились до Windows Vista в качестве [объектов мультимедиа DirectX](../directshow/directx-media-objects.md) (дмос). если кодек поддерживает DMO функциональные возможности, его можно использовать с [DirectShow](../directshow/directshow.md) или [пакетом SDK для Windows Media Format](../wmformat/windows-media-format-11-sdk.md).

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Media Foundationое программное руководством](media-foundation-programming-guide.md)
</dt> <dt>

[Источники и приемники мультимедиа](media-sources-and-sinks.md)
</dt> </dl>

 

 
