---
description: В этом разделе описывается, как задать формат расширенного потока звука (AAC) в Media Foundation.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: Типы носителей AAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae70661478ad0d2267c951c80fc4a63d98c15267
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479890"
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




| attribute | Описание | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Основной тип. Необходимо <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Подтип аудио. Дополнительные сведения см. в описании выше. | 
| <a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a> | Профиль и уровень звука. <br /> Значением этого атрибута является поле <strong>аудиопрофилелевелиндикатион</strong> , ОПРЕДЕЛЕННОЕ в стандарте ISO/IEC 14496-3.<br /> Если неизвестно, задайте для параметра значение 0 или 0xFE ("не указан звуковой профиль").<br /> | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a> | Битовая скорость закодированного потока AAC в байтах в секунду. | 
| <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> | Тип полезных данных.<br /> Применяется только к <strong>MFAudioFormat_AAC</strong>.<br /><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> является необязательным. Если этот атрибут не указан, используется значение по умолчанию 0, которое указывает, что поток содержит только элементы raw_data_block.<br /> | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Битовая глубина декодированного звука PCM. | 
| <a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a> | Назначение звуковых каналов для позиционирования динамиков. | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Количество каналов, включая канал с низкой частотой (НИЗКОЧАСТОТный), если он есть.<br /> Интерпретация этого значения зависит от подтипа носителя, как описано выше.<br /> | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Частота выборки, в примерах в секунду.<br /> Интерпретация этого значения зависит от подтипа носителя, как описано выше.<br /> | 
| <a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a> | Значение этого атрибута зависит от подтипа:<br /><ul><li><strong>MFAudioFormat_AAC</strong>: содержит часть структуры <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>хеааквавеинфо</strong></a> , которая появляется после структуры <strong>вавеформатекс</strong> (то есть после элемента <strong>вфкс</strong> ). За ним следуют данные АудиоспеЦификконфиг () в соответствии с определением ISO/IEC 14496-3.</li><li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: содержит данные аудиоспеЦификконфиг ().</li></ul> | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Типы звуковых носителей](audio-media-types.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> <dt>

[Поддержка MPEG-4 в Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

