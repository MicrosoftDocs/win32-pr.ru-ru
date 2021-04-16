---
description: В разделе содержится перечень форматов мультимедиа, которые Microsoft Media Foundation поддерживает изначально.
ms.assetid: 69c12a28-4b58-4979-b4d8-ae37efa847fe
title: Поддерживаемые форматы мультимедиа в Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e8f698179d37fc6bde8d5d1dab25214727cd38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664825"
---
# <a name="supported-media-formats-in-media-foundation"></a>Поддерживаемые форматы мультимедиа в Media Foundation

В разделе содержится перечень форматов мультимедиа, которые Microsoft Media Foundation поддерживает изначально. Сторонние лица могут поддерживать дополнительные форматы, создавая пользовательские подключаемые модули.

## <a name="file-containers"></a>Контейнеры файлов



| Формат                                           | Расширения файлов          | Источник мультимедиа                                 | Приемник мультимедиа                                   | Требуется                                                              |
|--------------------------------------------------|--------------------------|----------------------------------------------|----------------------------------------------|-----------------------------------------------------------------------|
| 3GP                                              | .3G2,. 3GP,. 3GP2,. 3GPP | [Источник файла MPEG-4](mpeg-4-file-source.md) | Приемник файла 3GP                                | Windows 7                                                             |
| Расширенный формат потоковой передачи (ASF)                  | . ASF,. WMA,. WMV         | [Источник носителя ASF](asf-media-source.md)     | [Приемник мультимедиа ASF](asf-media-sinks.md)        | Windows Vista                                                         |
| Поток транспорта аудиоданных (ADTS).              | . AAC,. ADTs              | Источник файла ADTS                             | Нет                                         | Windows 7                                                             |
| AVI                                              | .avi                     | Источник файла AVI                              | Нет                                         | Windows 7                                                             |
| MP3                                              | .mp3                     | [**Источник MP3-файла**](mp3-file-source.md)   | Приемник файлов в формате MP3                                | Источник файла: Windows Vista<br/> Приемник файла: Windows 7<br/> |
| MPEG-4                                           | . m4a,. m4v,. mov,. MP4   | [Источник файла MPEG-4](mpeg-4-file-source.md) | [**Приемник файлов MPEG-4**](mpeg-4-file-sink.md) | Windows 7                                                             |
| Синхронизированный доступный медиа-обмен (SAMI) | . samid,. SMI              | [Источник носителя SAMI](sami-media-source.md)   | Нет                                         | Windows Vista                                                         |
| ЗВУКОВ                                             | .wav                     | Источник файла AVI                              | Нет                                         | Windows 7                                                             |



 

## <a name="audio-codecs"></a>Аудиокодеки



| Формат                                              | Показан                                                                                                                                                          | Кодировщик                                                                                                                                                          | Требуется      |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| μное написание закона                                        | Μ-кодек диспетчера аудиосжатия (ACM)                                                                                                                      | Нет                                                                                                                                                             | Windows Vista |
| Адаптивное разностное импульсное программное средство модуляции (ADPCM) | Кодек ADPCM ACM                                                                                                                                                  | Нет                                                                                                                                                             | Windows Vista |
| Расширенное аудио кодирование (AAC)                         | [**Декодер AAC**](aac-decoder.md)                                                                                                                               | [**Кодировщик AAC**](aac-encoder.md)                                                                                                                               | Windows 7     |
| MP3                                                 | [**Декодер MP3 Windows Media**](windows-media-mp3-decoder.md)                                                                                                   | Нет                                                                                                                                                             | Windows Vista |
| GSM 6.10                                            | Кодек ACM GSM 6,10                                                                                                                                               | Нет                                                                                                                                                             | Windows Vista |
| Звуковые файлы в формате WMA                           | [**Декодер Windows Media Audio**](windowsmediaaudiodecoder.md)<br/> [**Декодер Windows Media Audio Voice**](windowsmediaaudiovoicedecoder.md)<br/> | [**Кодировщик Windows Media Audio**](windowsmediaaudioencoder.md)<br/> [**Кодировщик Windows Media Audio Voice**](windowsmediaaudiovoiceencoder.md)<br/> | Windows Vista |



 

> [!Note]  
> Media Foundation предоставляет оболочки для нескольких кодеков ACM, перечисленных в предыдущей таблице. Однако Media Foundation не поддерживает произвольные кодеки ACM.

 

## <a name="video-codecs"></a>Видеокодеки



| Формат                                                                                                         | Показан                                                                                                                                                                  | Кодировщик                                                                                                                             | Требуется      |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Видео DV                                                                                                       | [**Видеодекодер DV**](dv-video-decoder.md)                                                                                                                             | Нет                                                                                                                                | Windows 7     |
| H.264                                                                                                          | [**Декодер видео H. 264**](h-264-video-decoder.md)                                                                                                                       | [**Кодировщик видео H. 264**](h-264-video-encoder.md)                                                                                  | Windows 7     |
| H.263<br/> (H. 264, базовый профиль, совместимый с MPEG-4 PT2 короткий режим заголовков видео)<br/> | [**Видеодекодер MPEG-4 Part 2**](mpeg4part2videodecoder.md)                                                                                                            | Нет                                                                                                                                | Windows 8     |
| мжпег                                                                                                          | Декодер МЖПЕГ                                                                                                                                                            | Нет                                                                                                                                | Windows 7     |
| MPEG-4, часть 2                                                                                                  | [**Видеодекодер MPEG-4 Part 2**](mpeg4part2videodecoder.md)                                                                                                            | Нет                                                                                                                                | Windows 7     |
| MPEG-4 v1/v2/v3                                                                                                | [**Декодер Windows Media MPEG-4 v3**](./windowsmediampeg4v3decoder.md)<br/> [**Декодер Windows Media MPEG4 версии 1/v2**](windowsmediampeg4decoder.md)<br/>         | Нет                                                                                                                                | Windows Vista |
| Видеофайлы в формате WMV                                                                                      | [**Декодер Windows Media Video 9**](windowsmediavideo9decoder.md)<br/> [**Декодер экрана Windows Media видео 9**](windowsmediavideo9screendecoder.md)<br/> | Кодировщик Windows Media Video 9<br/> Кодировщик экрана Windows Media видео 9<br/> Кодировщик Windows Media Video 7/8<br/> | Windows Vista |



 

> [!Note]  
> В столбце "требуется" перечислены минимальные операционные системы, необходимые для использования этих кодеков в приложении Media Foundation. Некоторые из этих кодеков появились до Windows Vista в качестве [объектов мультимедиа DirectX](../directshow/directx-media-objects.md) (дмос). Если кодек поддерживает функции DMO, его можно использовать с [DirectShow](../directshow/directshow.md) или [пакетом SDK Windows Media Format](../wmformat/windows-media-format-11-sdk.md).

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Media Foundationое программное руководством](media-foundation-programming-guide.md)
</dt> <dt>

[Источники и приемники мультимедиа](media-sources-and-sinks.md)
</dt> </dl>

 

 
