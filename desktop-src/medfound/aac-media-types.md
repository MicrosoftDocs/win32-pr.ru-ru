---
description: В этом разделе описывается, как задать формат расширенного потока звука (AAC) в Media Foundation.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: Типы носителей AAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95423b26a0e2a327b599011e88a05ab2ab58c5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999857"
---
# <a name="aac-media-types"></a>Типы носителей AAC

В этом разделе описывается, как задать формат расширенного потока звука (AAC) в Media Foundation.

Для AAC Audio определены два подтипа:



| Subtype                     | Описание          | Header       |
|-----------------------------|----------------------|--------------|
| **Мфаудиоформат \_ AAC**      | Необработанный AAC или ADTS AAC. | мфапи. h      |
| **МЕДИАСУБТИПЕ \_ RAW \_ AAC1** | Необработанный AAC.             | вмкодекдсп. h |



 

<dl> <dt>

<span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>Мфаудиоформат \_ AAC
</dt> <dd>

Для этого подтипа мультимедиа тип носителя предоставляет частоту выборки и число каналов перед применением средств Спектрал (SBR) Replication и параметрической стерео (PS), если они есть. Результатом работы средства SBR является двойная декодированная частота выборки по сравнению с частотой выборки ядра AAC-LC. Результатом работы средства PS является декодирование стерео из потока AAC-LC ядра Mono.

Этот подтип эквивалентен **медиасубтипе \_ MPEG \_ хеаак**, определенному в вмкодекдсп. h. См. раздел [идентификаторы GUID для звуковых подтипов](audio-subtype-guids.md).

</dd> <dt>

<span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>МЕДИАСУБТИПЕ \_ RAW \_ AAC1
</dt> <dd>

Этот подтип используется для AAC, содержащихся в AVI-файле, с тегом формата Audio, равным \_ \_ RAW \_ -AAC1 (0x00FF).

Для этого подтипа тип носителя предоставляет частоту выборки и число каналов после применения инструментов SBR и PS, если они есть.

</dd> </dl>

Следующие атрибуты типа мультимедиа применяются к AAC аудио.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Основной тип. Необходимо <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Подтип аудио. Дополнительные сведения см. в описании выше.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Профиль и уровень звука. <br/> Значением этого атрибута является поле <strong>аудиопрофилелевелиндикатион</strong> , ОПРЕДЕЛЕННОЕ в стандарте ISO/IEC 14496-3.<br/> Если неизвестно, задайте для параметра значение 0 или 0xFE ( &quot; профиль звука не указан &quot; ).<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>Битовая скорость закодированного потока AAC в байтах в секунду.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>Тип полезных данных.<br/> Применяется только к <strong>MFAudioFormat_AAC</strong>.<br/> <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> является необязательным. Если этот атрибут не указан, используется значение по умолчанию 0, которое указывает, что поток содержит только элементы raw_data_block.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Битовая глубина декодированного звука PCM.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></td>
<td>Назначение звуковых каналов для позиционирования динамиков.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Количество каналов, включая канал с низкой частотой (НИЗКОЧАСТОТный), если он есть.<br/> Интерпретация этого значения зависит от подтипа носителя, как описано выше.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Частота выборки, в примерах в секунду.<br/> Интерпретация этого значения зависит от подтипа носителя, как описано выше.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></td>
<td>Значение этого атрибута зависит от подтипа:<br/>
<ul>
<li><strong>MFAudioFormat_AAC</strong>: содержит часть структуры <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>хеааквавеинфо</strong></a> , которая появляется после структуры <strong>вавеформатекс</strong> (то есть после элемента <strong>вфкс</strong> ). За ним следуют данные АудиоспеЦификконфиг () в соответствии с определением ISO/IEC 14496-3.</li>
<li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: содержит данные аудиоспеЦификконфиг ().</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы звуковых носителей](audio-media-types.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> <dt>

[Поддержка MPEG-4 в Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

