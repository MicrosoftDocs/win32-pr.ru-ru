---
description: Объекты кодека
ms.assetid: c944e5df-c375-4bad-92dc-bb3d8c09b1b3
title: Объекты кодека
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a4f140c81f162aaee2ffc416ed1de96dfcb470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808164"
---
# <a name="codec-objects"></a>Объекты кодека

В этом разделе описываются кодировщики и декодеры, поддерживаемые в Microsoft Media Foundation. Этот раздел содержит следующие подразделы.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="aac-decoder.md"><strong>Декодер AAC</strong></a></td>
<td>Звуковой декодер, который декодирует следующие расширенные профили (AAC) и высокоэффективные AAC (HE-AAC):
<ul>
<li>Профиль низкой сложности MPEG-2 AAC (LC) (многоканальный).</li>
<li>MPEG-4 HE-AAC v1 (многоканальный) с AAC-LC Core.</li>
<li>MPEG-4 HE-AAC v2 (стерео) с AAC-LC Core.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="aac-encoder.md"><strong>Кодировщик AAC</strong></a></td>
<td>Звуковой кодировщик, который кодирует расширенный профиль с низким уровнем сложности (AAC).</td>
</tr>
<tr class="odd">
<td><a href="dv-video-decoder.md"><strong>Видеодекодер DV</strong></a></td>
<td>Видеодекодер, который декодирует видео в DV-коде.</td>
</tr>
<tr class="even">
<td><a href="h-264-video-decoder.md"><strong>Декодер видео H. 264</strong></a></td>
<td>Видеодекодер, декодированный в видео H. 264. Он поддерживает декодирование базовых, главных и высококачественных профилей вплоть до уровня 5,1.</td>
</tr>
<tr class="odd">
<td><a href="h-264-video-encoder.md"><strong>Кодировщик видео H. 264</strong></a></td>
<td>Видеокодировщик, который кодирует видео H. 264. Он поддерживает следующие профили H. 264:
<ul>
<li>Базовый профиль</li>
<li>Профиль Main</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="h-264-video-decoder.md"><strong>Декодер видео H. 265/HEVC</strong></a></td>
<td>Видеодекодер, который поддерживает декодирование содержимого H. 265/HEVC в формате приложение б и может использоваться при воспроизведении файлов MP4 и M2TS. Он поддерживает следующие профили H. 264:
<ul>
<li>Профиль Main</li>
<li>Главный профиль 10</li>
<li>Неподвижный основной рисунок</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="h-264-video-encoder.md"><strong>H. 265/HEVC видео Encoder</strong></a></td>
<td>Видеокодировщик, который кодирует формат H. 265/HEVC. Он поддерживает следующие профили H. 265:
<ul>
<li>Профиль Main</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mpeg4part2videodecoder.md"><strong>Видеодекодер (часть 2) памяти MPEG4</strong></a></td>
<td>Видеодекодер MPEG-4 Part 2.</td>
</tr>
<tr class="odd">
<td><a href="windowsmediaaudiodecoder.md"><strong>Декодер Windows Media Audio</strong></a></td>
<td>Декодер, который декодирует потоки, закодированные кодировщиком Windows Media Audio.</td>
</tr>
<tr class="even">
<td><a href="windowsmediaaudioencoder.md">Кодировщик Windows Media Audio</a></td>
<td>Звуковой кодировщик, поддерживающий три категории закодированных выходных данных:
<ul>
<li>Standard</li>
<li>Professional</li>
<li>Lossless</li>
</ul>
Стандартная категория предназначена для кодирования звука общего назначения. Категория Professional предназначена для кодирования звука с несколькими каналами или высокой четкости. Категория без потерь предназначена для сжатия звука без потери исходных данных.</td>
</tr>
<tr class="odd">
<td><a href="windowsmediaaudiovoicedecoder.md"><strong>Декодер Windows Media Audio Voice</strong></a></td>
<td>Декодер, который декодирует потоки, закодированные кодировщиком Windows Media Audio Voice.</td>
</tr>
<tr class="even">
<td><a href="windowsmediaaudiovoiceencoder.md">Кодировщик Windows Media Audio Voice</a></td>
<td>Кодировщик для кодирования звука, содержащего в основном речь.</td>
</tr>
<tr class="odd">
<td><a href="windows-media-mp3-decoder.md"><strong>Декодер MP3 Windows Media</strong></a></td>
<td>Звуковой декодер, декодированный в следующих звуковых форматах.
<ul>
<li>ISO/IEC 11172-3 (аудио MPEG-1), уровень 3</li>
<li>Стандарт ISO/IEC 13818-3 (MPEG-2 Audio), низкое расширение частоты выборки</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="windowsmediampeg4decoder.md"><strong>Декодер Windows Media MPEG4 версии 1/v2</strong></a></td>
<td>Декодер, который реализует декодирование видео MPEG-4 v1/v2.</td>
</tr>
<tr class="odd">
<td><a href="windows-media-video-7-and-8-encoders.md"><strong>Кодировщик Windows Media Video 7/8</strong></a></td>
<td>Видеокодировщик, реализующий предыдущие версии кодировщика видео Windows Media.</td>
</tr>
<tr class="even">
<td><a href="windowsmediavideo9decoder.md">Декодер Windows Media Video 9</a></td>
<td>Видеодекодер, который декодирует потоки, закодированные кодировщиком Windows Media Video 9.</td>
</tr>
<tr class="odd">
<td><a href="windowsmediavideo9encoder.md">Кодировщик Windows Media Video 9</a></td>
<td>Видеокодировщик, поддерживающий три категории выходных данных ендодед:
<ul>
<li>Windows Media Video 9</li>
<li>Расширенный профиль Windows Media Video 9</li>
<li>Изображение Windows Media Video 9,1</li>
</ul>
Категория Windows Media Video 9 предназначена для кодирования видео общего назначения. Категория расширенный профиль предназначена для кодирования видео или видео с высокой степенью четкости, которое соответствует стандарту VC-1 Advanced Profile SMPTE Standard. Категория изображений предназначена для преобразования растровых изображений в динамические видео.</td>
</tr>
<tr class="even">
<td><a href="windowsmediavideo9screendecoder.md"><strong>Декодер экрана Windows Media видео 9</strong></a></td>
<td>Декодер, который декодирует потоки, закодированные кодировщиком экрана Windows Media видео 9.</td>
</tr>
<tr class="odd">
<td><a href="windowsmediavideo9screenencoder.md"><strong>Кодировщик экрана Windows Media видео 9</strong></a></td>
<td>Кодировщик для кодирования компьютера — видео приложения (снимок экрана) или другое очень статическое видео.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по программированию в Media Foundation](media-foundation-programming-reference.md)
</dt> <dt>

[Поддерживаемые форматы мультимедиа в Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



