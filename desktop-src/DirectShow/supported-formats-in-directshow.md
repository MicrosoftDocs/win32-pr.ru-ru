---
description: Поддерживаемые форматы в DirectShow
ms.assetid: cd8af779-2fb5-4724-a838-5d0c8244f0d3
title: Поддерживаемые форматы в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10e42079f29ce89ba66fcd0c03a6520769a91538eb1a9b8901115b6895420d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633234"
---
# <a name="supported-formats-in-directshow"></a>Поддерживаемые форматы в DirectShow

DirectShow является открытой архитектурой, то есть она может поддерживать любой формат при условии, что имеются фильтры для синтаксического анализа и декодирования. фильтры, предоставляемые корпорацией майкрософт как распространяемые по DirectShow или как компоненты операционной системы Windows, обеспечивают поддержку по умолчанию для следующих форматов файлов и сжатия.

Типы файлов:



| Тип файла                                                                                        | Дополнительные сведения                                                                                                                  |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| расширенный формат систем (ASF), включая Windows media Audio (WMA) и Windows media Video (WMV) | [Фильтр чтения WM ASF](about-the-wm-asf-reader-filter.md)<br/> [Фильтр модуля записи WM ASF](wm-asf-writer-filter.md)<br/> |
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



 

сведения о доступности определенных кодеков сторонних производителей для распространения с помощью DirectShow приложений, обратитесь к изготовителю кодека.

 

 




