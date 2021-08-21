---
description: Идентификаторы GUID для подтипов звука
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: Идентификаторы GUID для подтипов звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dee55534ac01fd8d29b3fb77bddc82d7ce0b5b046ebe07cc75c83130c509fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065278"
---
# <a name="audio-subtype-guids"></a>Идентификаторы GUID для подтипов звука

Определены следующие идентификаторы GUID для звуковых подтипов. Чтобы указать подтип, задайте атрибут [**\_ \_ подтипа MF MT**](mf-mt-subtype-attribute.md) для типа носителя. За исключением указанных случаев, эти константы определены в файле заголовка мфапи. h.

Если используются эти подтипы, задайте для атрибута " [ \_ \_ основной \_ тип MF MT](mf-mt-major-type-attribute.md) " значение **мфмедиатипе \_ Audio**.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Идентификатор GUID</th>
<th>Описание</th>
<th>Тег Format (FOURCC)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MEDIASUBTYPE_RAW_AAC1</strong></td>
<td>Расширенное аудио кодирование (AAC).<br/> Этот подтип используется для AAC, содержащихся в AVI-файле, с тегом формата, равным 0x00FF. <br/> Дополнительные сведения см. в разделе <a href="aac-decoder.md"><strong>декодер AAC</strong></a>.<br/> Определено в вмкодекдсп. h<br/></td>
<td>WAVE_FORMAT_RAW_AAC1 (0x00FF)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>Расширенное аудио кодирование (AAC).<br/>
<blockquote>
[!Note]<br />
Эквивалентно MEDIASUBTYPE_MPEG_HEAAC, определенному в вмкодекдсп. h.
</blockquote>
<br/> Поток может содержать необработанные данные AAC или AAC данные в потоке передачи звуковых данных (ADTS).<br/> Дополнительные сведения см. в разделе:<br/>
<ul>
<li><a href="aac-decoder.md"><strong>Декодер AAC</strong></a></li>
<li><a href="mpeg-4-file-source.md">Источник файла MPEG-4</a></li>
</ul></td>
<td>WAVE_FORMAT_MPEG_HEAAC (0x1610)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_ADTS</strong></td>
<td>Не используется.</td>
<td>WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_ALAC</strong></td>
<td>Аудиокодек Apple без потерь<br/> поддерживается в Windows 10 и более поздних версиях.<br/></td>
<td>WAVE_FORMAT_ALAC (0x6C61)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AMR_NB</strong></td>
<td>Адаптативе с несколькими скоростями<br/> поддерживается в Windows 8.1 и более поздних версиях.<br/></td>
<td>WAVE_FORMAT_AMR_NB</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_AMR_WB</strong></td>
<td>Адаптативе Multi-Rate Wideband Audio<br/> поддерживается в Windows 8.1 и более поздних версиях.<br/></td>
<td>WAVE_FORMAT_AMR_WB</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AMR_WP</strong></td>
<td>поддерживается в Windows 8.1 и более поздних версиях.<br/></td>
<td>WAVE_FORMAT_AMR_WP</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Dolby_AC3</strong></td>
<td>Dolby Digital (AC-3).<br/> То же значение GUID, что и <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, которое определено в ксууидс. h<br/></td>
<td>Отсутствует.</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></td>
<td>Dolby AC-3 аудио через Sony/Philips Digital Interface (S/PDIF).<br/> Это значение идентификатора GUID идентично приведенным ниже подтипам:<br/>
<ul>
<li><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, определенный в ксмедиа. h.</li>
<li><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, определенные в UUID. h.</li>
</ul></td>
<td>WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Dolby_DDPlus</strong></td>
<td>Dolby Digital Plus.<br/> То же значение GUID, что и <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, которое определено в вмкодекдсп. h.<br/></td>
<td>Нет</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_DRM</strong></td>
<td>Зашифрованные звуковые данные, используемые с защищенным звуковым путем.</td>
<td>WAVE_FORMAT_DRM (0x0009)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_DTS</strong></td>
<td>Звук системы цифрового кинотеатра (DTS).</td>
<td>WAVE_FORMAT_DTS (0x0008)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_FLAC</strong></td>
<td>Бесплатный аудиокодек без потерь<br/> поддерживается в Windows 10 и более поздних версиях.<br/></td>
<td>WAVE_FORMAT_FLAC (0xF1AC)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Float</strong></td>
<td>Несжатое аудио с плавающей запятой IEEE.</td>
<td>WAVE_FORMAT_IEEE_FLOAT (0x0003)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Float_SpatialObjects</strong></td>
<td>Несжатое аудио с плавающей запятой IEEE.</td>
<td>Нет</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_MP3</strong></td>
<td>Звуковой слой MPEG-3 (MP3).</td>
<td>WAVE_FORMAT_MPEGLAYER3 (0x0055)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_MPEG</strong></td>
<td>Полезные данные звука MPEG-1.</td>
<td>WAVE_FORMAT_MPEG (0x0050)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_MSP1</strong></td>
<td>Windows Голосовой кодек Media Audio 9.</td>
<td>WAVE_FORMAT_WMAVOICE9 (0x000A)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Opus</strong></td>
<td>Opus<br/> поддерживается в Windows 10 и более поздних версиях.<br/></td>
<td>WAVE_FORMAT_OPUS (0x704F)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>Несжатый звук PCM.</td>
<td>WAVE_FORMAT_PCM (1)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_QCELP</strong></td>
<td>КЦЕЛП (линейный прогноз для кода Qualcomm).</td>
<td>Нет</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_WMASPDIF</strong></td>
<td>Windows Media Audio 9 Professional кодек через S/PDIF.</td>
<td>WAVE_FORMAT_WMASPDIF (0x0164)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_WMAudio_Lossless</strong></td>
<td>Windows кодек мультимедиа media audio 9 без потерь или кодек Windows Media audio 9,1.</td>
<td>WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_WMAudioV8</strong></td>
<td>Windows кодек media audio 8, кодек Windows media audio 9 или кодек Windows Media audio 9,1.</td>
<td>WAVE_FORMAT_WMAUDIO2 (0x0161)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_WMAudioV9</strong></td>
<td>Windows media audio 9 Professional кодек или Windows media audio 9,1 Professional кодека.</td>
<td>WAVE_FORMAT_WMAUDIO3 (0x0162)</td>
</tr>
</tbody>
</table>



 

Теги формата, перечисленные в третьем столбце этой таблицы, используются в структуре **вавеформатекс** и определены в файле заголовка ммрег. h.

При наличии тега звукового формата можно создать идентификатор GUID для звукового подтипа следующим образом:

1.  Начните со значения **мфаудиоформат \_ base**, которое определено в мфаф. i.
2.  Замените первый **DWORD** этого GUID тегом Format.

Чтобы определить новую константу GUID, которая следует за этим шаблоном, можно использовать макрос [**define \_ MEDIATYPE \_ GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Типы звуковых носителей](audio-media-types.md)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[GUID типа носителя](media-type-guids.md)
</dt> <dt>

[Типы носителей](media-types.md)
</dt> </dl>

 

 




