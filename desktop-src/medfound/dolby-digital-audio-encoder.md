---
description: Декодер Dolby Audio — это Media Foundation преобразование (MFT), которое кодирует моно или стерео Audio в Dolby Digital, также называемое Dolby AC-3.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Кодировщик цифрового звука Dolby
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6c5b59bc09cd8c0fd56f22703ef8afdfe3921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701319"
---
# <a name="dolby-digital-audio-encoder"></a>Кодировщик цифрового звука Dolby

Декодер Dolby Audio — это [Media Foundation преобразование](media-foundation-transforms.md) (MFT), которое кодирует моно или стерео Audio в Dolby Digital, также называемое Dolby AC-3. Кодировщик не поддерживает многоканальные входные данные, такие как конфигурация канала 5,1.

> [!IMPORTANT]
> Для версий Windows, предшествовавших Windows 8, реализация технологий Dolby Digital в корпорации Майкрософт ограничена условиями программы цифрового лицензирования Dolby, используемой приложениями Майкрософт.

 

Дополнительные сведения о цифровом звуковом стандарте Dolby см. в документе по расширенному телевидению *цифрового звука (AC-3, E-AC-3) версии B*.

## <a name="class-identifier"></a>Идентификатор класса

Идентификатором класса (CLSID) декодера Dolby Audio является **CLSID \_ кмсдолбидигиталенкмфт**, определенный в файле заголовка вмкодекдсп. h.

## <a name="output-types"></a>Типы вывода

Тип выходных данных должен быть задан первым, перед входным типом. В следующей таблице перечислены обязательные и необязательные атрибуты для выходного типа мультимедиа.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Описание</th>
<th>Remarks</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Основной тип.</td>
<td>Обязательный. Необходимо <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Подтип аудио.</td>
<td>Обязательный. Необходимо <strong>MFAudioFormat_Dolby_AC3</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Выборок в секунду.</td>
<td>Обязательный. Поддерживаются следующие значения.
<ul>
<li>32000</li>
<li>44100</li>
<li>48000</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Число каналов.</td>
<td>Обязательный. Значение должно быть либо 1 (моно), либо 2 (стерео).</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Указывает назначение звуковых каналов для позиционирования динамиков.</td>
<td>Необязательный элемент. Если задано, значение должно быть 0x3ым для стерео (передний левый и правый каналы) или 0x4 для Mono (канал Front Center).</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Скорость потока в закодированном потоке AC-3, в байтах в секунду.</td>
<td>Необязательный элемент. Допустимые значения см. в разделе Примечания. Если этот атрибут не задан, кодировщик использует битовую скорость по умолчанию, как описано в разделе Примечания.</td>
</tr>
</tbody>
</table>



 

Если необязательные атрибуты не заданы, кодировщик добавляет их в тип мультимедиа после задания типа.

## <a name="input-types"></a>Типы входных данных

В следующей таблице перечислены обязательные и необязательные атрибуты для входного типа носителя.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Описание</th>
<th>Remarks</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Основной тип.</td>
<td>Обязательный. Необходимо <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Подтип аудио.</td>
<td>Обязательный. Должен быть <strong>MFAudioFormat_PCM</strong> или <strong>MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>Число битов на аудио выборка.</td>
<td>Обязательный. Значение должно быть 16, если подтип имеет <strong>MFAudioFormat_PCM</strong>, или 32, если подтип имеет <strong>MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Выборок в секунду.</td>
<td>Обязательный. Должен соответствовать типу выходных данных.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Число каналов.</td>
<td>Обязательный. Должен соответствовать типу выходных данных.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Выравнивание блокировки в байтах.</td>
<td>Обязательный. Вычислите значение следующим образом:
<ul>
<li><strong>MFAudioFormat_PCM</strong>: число каналов × 2.</li>
<li><strong>MFAudioFormat_Float</strong>: число каналов × 4.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Битовая скорость закодированного потока AC3 в байтах в секунду.</td>
<td>Обязательный. Должно равняться выравниванию блока × Samples в секунду.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Указывает назначение звуковых каналов для позиционирования динамиков.</td>
<td>Необязательный элемент. Если параметр задан, значение должно соответствовать типу выходных данных.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Количество допустимых битов звуковых данных в каждом звуковом примере.</td>
<td>Необязательный элемент. Если значение задано, оно должно быть идентично значению <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</td>
</tr>
</tbody>
</table>



 

Кодировщик не поддерживает преобразование "выборка" или "стерео/моно".

## <a name="remarks"></a>Комментарии

Каждый звуковой кадр Dolby AC-3 содержит 1536 аудио образцов на канал. Однако каждый входной буфер кодировщика может содержать любое количество примеров PCM. Размер каждого входного буфера должен быть кратен выравниванию блока. Кодировщик кэширует входные примеры, пока не будет достаточно для 1536 аудио образцов на канал. на этом этапе кодировщик выводит один кадр AC-3.

Каждый выходной буфер содержит один необработанный кадр AC-3. Длительность будет равна длительности 1536 выборки PCM по текущей частоте выборки (32 МС) в 48 кГц выборка, 34,83 МС в 44,1 кГц и 48 МС в 32 кГц). Размер каждого выходного буфера зависит от скорости потока и частоты выборки.

Чтобы задать скорость кодирования, установите атрибут " [ \_ \_ \_ Среднее \_ число байт в секунду" \_ для \_ звукового сигнала MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) в типе вывода. В следующей таблице показана связь между скоростью кодирования и \_ \_ \_ средним числом звуковых аудиоданных MF \_ \_ в \_ секунду.



| Скорость потока (кбит/с) | [\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) | Комментарии                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| 64              | 8000                                                                                     | Только моно.                                              |
| 80              | 10000                                                                                    | Только моно.                                              |
| 96              | 12000                                                                                    | Только моно.                                              |
| 112             | 14000                                                                                    | Только моно.                                              |
| 128             | 16000                                                                                    | Моно или стерео.                                         |
| 160             | 20 000                                                                                    | Моно или стерео.                                         |
| 192             | 24 000                                                                                    | Моно или стерео. Это значение по умолчанию для Mono.   |
| 224             | 28000                                                                                    | Моно или стерео.                                         |
| 256             | 32000                                                                                    | Моно или стерео. Это значение по умолчанию для стерео. |
| 320             | 40 000                                                                                    | Только стерео.                                            |
| 384             | 48000                                                                                    | Только стерео.                                            |
| 448             | 56000                                                                                    | Только стерео.                                            |



 

Скорость кодирования по умолчанию устанавливается в 256 кбит/с для стерео и 192 кбит/с для Mono. Параметры по умолчанию отражаются в типах носителей, возвращаемых методом [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) кодировщика.

### <a name="example-media-types"></a>Примеры типов мультимедиа

Ниже приведен пример типов мультимедиа, которые необходимы для кодирования 16-разрядного целочисленного PCM 48-кГц при скорости по умолчанию 256 кбит/с.

Тип выходного носителя:

| attribute                                                                           | Значение                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [\_ \_ основной тип MF \_ MT](mf-mt-major-type-attribute.md)                               | **Мфмедиатипе \_ аудио**        |
| [подтип MF \_ MT \_](mf-mt-subtype-attribute.md)                                      | **Мфаудиоформат \_ Dolby \_ AC3** |
| [\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду](mf-mt-audio-samples-per-second-attribute.md) | 48000                         |
| [\_ \_ каналы аудиосигнала MF MT \_ \_](mf-mt-audio-num-channels-attribute.md)              | 2                             |



 

Тип входного носителя:

| attribute                                                                                | Значение                  |
|------------------------------------------------------------------------------------------|------------------------|
| [\_ \_ основной тип MF \_ MT](mf-mt-major-type-attribute.md)                                    | **Мфмедиатипе \_ аудио** |
| [подтип MF \_ MT \_](mf-mt-subtype-attribute.md)                                           | **Мфаудиоформат \_ PCM** |
| [\_ \_ звуковый бит MF MT \_ \_ на \_ выборку](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [\_ \_ каналы аудиосигнала MF MT \_ \_](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [\_ \_ Выравнивание звукового \_ блока MF MT \_](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                               |
| DLL<br/>                      | <dl> <dt>Msac3enc.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> </dl>

 

 




