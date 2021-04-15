---
description: Поддерживаемые форматы в DirectShow
ms.assetid: cd8af779-2fb5-4724-a838-5d0c8244f0d3
title: Поддерживаемые форматы в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a6c9a0c85a3ccdfd3db092ba2efce00a191493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683987"
---
# <a name="supported-formats-in-directshow"></a>Поддерживаемые форматы в DirectShow

DirectShow — это открытая архитектура, которая означает, что она может поддерживать любой формат при условии, что имеются фильтры для синтаксического анализа и декодирования. Фильтры, предоставляемые корпорацией Майкрософт как распространяемые через DirectShow или как компоненты операционной системы Windows, обеспечивают поддержку по умолчанию для следующих форматов файлов и сжатия.

Типы файлов:



| Тип файла                                                                                        | Дополнительные сведения                                                                                                                  |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Расширенный формат систем (ASF), включая Windows Media Audio (WMA) и Windows Media Video (WMV) | [Фильтр чтения WM ASF](about-the-wm-asf-reader-filter.md)<br/> [Фильтр модуля записи WM ASF](wm-asf-writer-filter.md)<br/> |
| AIFF                                                                                             | [Фильтр синтаксического анализатора волн](wave-parser-filter.md)                                                                                      |
| AU                                                                                               | [Фильтр синтаксического анализатора волн](wave-parser-filter.md)                                                                                      |
| Audio-Video Interleaved (AVI)                                                                    | [Фильтр мультиплексора AVI](avi-mux-filter.md)<br/> [Фильтр разделителя AVI](avi-splitter-filter.md)<br/>                         |
| MIDI                                                                                             | [Фильтр средства синтаксического анализа MIDI](midi-parser-filter.md)<br/> [**Фильтр модуля подготовки MIDI**](midi-renderer-filter.md)<br/>           |
| SND                                                                                              |                                                                                                                                   |
| WAV                                                                                              | [Фильтр синтаксического анализатора волн](wave-parser-filter.md)                                                                                      |



 

Форматы сжатия:



| Формат                                        | Дополнительные сведения                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AAC                                           | [**Декодер звука Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)                                                                                                                                                              |
| Цинепак                                       |                                                                                                                                                                                                                                                 |
| Цифровое видео (DV)                            | [Фильтр видеодекодера DV](dv-video-decoder-filter.md)<br/> [Фильтр кодировщика видео DV](dv-video-encoder-filter.md)<br/>                                                                                                             |
| H.264                                         | [**Видеодекодер Microsoft MPEG-2 видео**](microsoft-mpeg-2-video-decoder.md)                                                                                                                                                                        |
| Видео ISO MPEG-4, версия 1,0                  |                                                                                                                                                                                                                                                 |
| Microsoft MPEG-4 версии 3                    |                                                                                                                                                                                                                                                 |
| мжпег                                         | [Фильтр сжатия МЖПЕГ](mjpeg-compressor-filter.md)<br/> [Фильтр декомпрессора МЖПЕГ](mjpeg-decompressor-filter.md)<br/>                                                                                                         |
| MPEG Audio Layer-3 (MP3) (только распаковка) |                                                                                                                                                                                                                                                 |
| Аудио I и Layer II слоя MPEG-1             | [**Декодер звука Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)<br/> [Фильтр звукового декодера MPEG-1](mpeg-1-audio-decoder-filter.md)<br/>                                                                         |
| Видео MPEG-1                                  | [Фильтр видеодекодера MPEG-1](mpeg-1-video-decoder-filter.md)<br/> [**Видеодекодер Microsoft MPEG-2 видео**](microsoft-mpeg-2-video-decoder.md)<br/>                                                                                   |
| Звук MPEG-2                                  | [**Кодировщик Microsoft MPEG-2 Audio Encoder**](microsoft-mpeg-2-audio-encoder.md)<br/> [**Кодировщик Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md)<br/>                                                                                     |
| Видео MPEG-2                                  | [**Кодировщик Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md)<br/> [**Видеодекодер Microsoft MPEG-2 видео**](microsoft-mpeg-2-video-decoder.md)<br/> [**Видеокодировщик Microsoft MPEG-2 видео**](microsoft-mpeg-2-video-encoder.md)<br/> |



 

Сведения о доступности определенных кодеков сторонних производителей для распространения с помощью приложений DirectShow см. в изготовителе кодека.

 

 




