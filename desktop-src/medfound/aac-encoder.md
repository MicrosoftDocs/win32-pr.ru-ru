---
description: Кодировщик Microsoft Media Foundation AAC — это Media Foundation преобразование, которое кодирует расширенный профиль (LC) с низким уровнем сложности (AAC), как определено в стандарте ISO/IEC 13818-7 (звук MPEG-2 Audio Part 7).
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: Кодировщик AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 674ad291e1cf6b56f7ffef640fade683265b62a7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465641"
---
# <a name="aac-encoder"></a>Кодировщик AAC

Кодировщик Microsoft Media Foundation AAC — это [Media Foundation преобразование](media-foundation-transforms.md) , которое кодирует расширенный профиль (LC) с низким уровнем сложности (AAC), как определено в стандарте ISO/IEC 13818-7 (звук MPEG-2 Audio Part 7).

Кодировщик AAC не поддерживает кодирование для любых других профилей AAC, таких как Main, SSR или ЛТП.

## <a name="class-identifier"></a>Идентификатор класса

Идентификатором класса (CLSID) кодировщика AAC является **CLSID \_ аакмфтенкодер**, определенный в файле заголовка вмкодекдсп. h.

## <a name="media-types"></a>Типы носителей

Кодировщик AAC поддерживает следующие типы носителей. Можно задать типы в первом порядке ввода или тип вывода.

### <a name="input-types"></a>Типы входных данных

Задайте следующие атрибуты для входного типа носителя.




| attribute | Описание | Remarks | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Основной тип. | Необходимо <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Подтип. | Необходимо <strong>MFAudioFormat_PCM</strong>. | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Бит на выборку. | Должно быть 16. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Выборок в секунду. | Поддерживаются следующие значения.<ul><li>44100 (44,1 кГц)</li><li>48000 (48 кГц)</li></ul> | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Число каналов. | Должно быть 1 (моно) или 2 (стерео) или 6 (5,1).<blockquote>[!Note]<br />поддержка 6 звуковых каналов была представлена в Windows 10 и недоступна для более ранних версий Windows.</blockquote><br /> | 




 

После установки входного типа кодировщик получает следующие значения и добавляет их к типу мультимедиа:

-   [**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**\_ \_ Выравнивание звукового \_ блока MF MT \_**](mf-mt-audio-block-alignment-attribute.md)
-   [**\_ \_ Средняя скорость MF \_ MT**](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a>Типы вывода

Задайте следующие атрибуты для выходного типа носителя.




| attribute | Описание | Remarks | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Основной тип. | Необходимо <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Подтип аудио. | Необходимо <strong>MFAudioFormat_AAC</strong>. | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Бит на выборку. | Должно быть 16. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Выборок в секунду. | Должен соответствовать типу входных данных. | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Число каналов. | Должен соответствовать типу входных данных. | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a> | Битовая скорость закодированного потока AAC в байтах в секунду. | Поддерживаются следующие значения.<ul><li>12000</li><li>16000</li><li>20 000</li><li>24 000</li></ul>Значение по умолчанию для Mono и стерео — 12000 (96 Кбит/с).<br /> | 
| <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> | Тип полезных данных AAC. | Необязательный элемент. Если задано, значение должно быть равно нулю, что означает, что поток содержит только элементы raw_data_block.<br /> Необязательный элемент. Если атрибут не задан, значение по умолчанию равно нулю, что означает, что поток содержит только элементы raw_data_block (необработанные AAC). <br /> в Windows 7, если этот атрибут задан, значение должно быть равно нулю.<br /> начиная с Windows 8, значение может быть равно 0 (raw AAC) или 1 (ADTS AAC). <br /> | 
| <a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a> | Профиль аудио AAC и уровень. | Необязательный элемент. Поддерживаются следующие значения.<ul><li>0x29 (по умолчанию)</li><li>0x2A</li><li>0x2B</li><li>0x2C</li><li>0x2E</li><li>0x2F</li><li>0x30</li><li>0x31</li><li>0x32</li><li>0x33</li></ul> | 


В следующей таблице перечислены значения, которые можно использовать для атрибута MF_MT_AAC_PROFILE_LEVEL_INDICATION.

| MF_MT_AAC_PROFILE_LEVEL_INDICATION значение | Профиль                           |
|------------------------------------------|-----------------------------------|
| 0x29                                     | Профиль AAC L2                    | 
| 0x2A                                     | AAC профиль 4                    | 
| 0x2B                                     | AAC профиль 5                    | 
| 0x2C                                     | Высокая эффективность v1 AAC профилирование L2 | 
| 0x2E                                     | Высокая эффективность v1 AAC профиль уровня 4 | 
| 0x2F                                     | Высокопроизводительная версия 1 AAC профиль 5 | 
| 0x30                                     | Высокопроизводительная версия 2, AAC профиль L2 | 
| 0x31                                     | Высокопроизводительная версия 2 AAC профиль L3 | 
| 0x32                                     | Высокопроизводительный v2 AAC профиль уровня 4 | 
| 0x33                                     | Высокопроизводительный v2 AAC профиль уровня 5 | 

 

После установки типа выходных данных кодировщик AAC обновляет тип, добавляя атрибут [**\_ \_ \_ данных пользователя MF MT**](mf-mt-user-data-attribute.md) . Этот атрибут содержит часть структуры [**хеааквавеинфо**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) , которая появляется после структуры [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) (то есть после элемента **вфкс** ). За ним следуют данные АудиоспеЦификконфиг () в соответствии с определением ISO/IEC 14496-3.

Каждый образец выходных данных содержит один сжатый кадр AAC без заголовка. Этот формат эквивалентен элементу необработанного \_ \_ блока данных (), определенному MPEG-2. Атрибут [ \_ \_ \_ \_ типа полезных данных MF MT AAC](mf-mt-aac-payload-type.md) , если он есть в выходном типе, должен иметь нулевое значение, чтобы указать этот тип полезной нагрузки.

Каждый пример выходных данных содержит один сжатый кадр AAC, соответствующий примерам PCM 1024. Например, при частоте выборки 48 кГц продолжительность одного сжатого кадра составляет 21,33 МС.

Если [ \_ \_ \_ \_ Тип полезной нагрузки MF MT AAC](mf-mt-aac-payload-type.md) равен нулю (значение по умолчанию), каждый образец вывода содержит один элемент необработанного \_ \_ блока данных (), определенный в стандарте ISO/IEC 13818-7.

## <a name="example-media-types"></a>Примеры типов мультимедиа

Ниже приведен пример типов мультимедиа, необходимых для кодирования из стерео аудио AAC с 44,1 кГц, 160-кбит/с в необработанном формате.

Тип входного носителя:



| attribute                                                                                    | Значение                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [**\_ \_ основной тип MF \_ MT**](mf-mt-major-type-attribute.md)                                    | **Мфмедиатипе \_ аудио** |
| [**подтип MF \_ MT \_**](mf-mt-subtype-attribute.md)                                           | **Мфаудиоформат \_ PCM** |
| [**\_ \_ звуковый бит MF MT \_ \_ на \_ выборку**](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**](mf-mt-audio-samples-per-second-attribute.md)      | 44100                  |
| [**\_ \_ каналы аудиосигнала MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 176400 (необязательно)      |
| [**\_ \_ Выравнивание звукового \_ блока MF MT \_**](mf-mt-audio-block-alignment-attribute.md)             | 4 (необязательно)           |
| [**MF \_ — \_ все \_ \_ независимые примеры**](mf-mt-all-samples-independent-attribute.md)         | 1 (необязательно)           |
| [**\_ \_ Средняя скорость MF \_ MT**](mf-mt-avg-bitrate-attribute.md)                                  | 1411200 (необязательно)     |
| [**\_ \_ примеры фиксированного \_ размера MF MT \_**](mf-mt-fixed-size-samples-attribute.md)                   | 1 (необязательно)           |



 

Тип выходного носителя:



| attribute                                                                                      | Значение                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**\_ \_ основной тип MF \_ MT**](mf-mt-major-type-attribute.md)                                      | **Мфмедиатипе \_ аудио**                                                                          |
| [**подтип MF \_ MT \_**](mf-mt-subtype-attribute.md)                                             | **Мфаудиоформат \_ AAC**                                                                          |
| [**\_ \_ звуковый бит MF MT \_ \_ на \_ выборку**](mf-mt-audio-bits-per-sample-attribute.md)              | 16                                                                                              |
| [**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**](mf-mt-audio-samples-per-second-attribute.md)        | 44100                                                                                           |
| [**\_ \_ каналы аудиосигнала MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                     | 2                                                                                               |
| [**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | 20 000                                                                                           |
| [\_ \_ \_ Тип полезных данных AAC MF MT \_](mf-mt-aac-payload-type.md)                                       | 0 (необязательно)                                                                                    |
| [\_ \_ \_ Указание уровня звукового \_ профиля \_ MF MT AAC \_](mf-mt-aac-audio-profile-level-indication.md) | 0x29 (необязательно)                                                                                 |
| [**\_ \_ Выравнивание звукового \_ блока MF MT \_**](mf-mt-audio-block-alignment-attribute.md)               | 1 (необязательно)                                                                                    |
| [**MF \_ — \_ все \_ \_ независимые примеры**](mf-mt-all-samples-independent-attribute.md)           | 0 (необязательно)                                                                                    |
| [**\_ \_ Средняя скорость MF \_ MT**](mf-mt-avg-bitrate-attribute.md)                                    | 160000 (необязательно)                                                                               |
| [**\_ \_ данные пользователя MF \_ MT**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} используемых |



 

## <a name="remarks"></a>Комментарии

В текущей реализации каждый входной пример должен иметь допустимое время и длительность. Чтобы задать время выборки, вызовите [**имфсампле:: сетсамплетиме**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime). Чтобы задать длительность выборки, вызовите метод [**имфсампле:: сетсампледуратион**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).

Если время выборки не задано, метод [**имфтрансформ::P роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) кодировщика возвращает **MF \_ E \_ без \_ образца \_ метки времени**. Если длительность выборки не задана, метод **ProcessInput** возвращает **MF \_ E \_ без \_ выборки \_ длительности**.

Длительность выборки может быть рассчитана следующим образом:


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



где *наудиосамплесперчаннел* — число выборки звука PCM на канал во входном буфере, а *нсамплесперсек* — частота выборки, в примерах в секунду.

> [!Note]  
> Из-за ошибки в текущей реализации, если длительность выборки равна нулю, вызов [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) выполняется, но последующий вызов [**Имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) будет вызывать исключение деления на ноль. Чтобы избежать этой ошибки, задайте допустимую ненулевую длительность для каждого входного образца.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mfaacenc.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[**Декодер AAC**](aac-decoder.md)
</dt> <dt>

[Типы носителей AAC](aac-media-types.md)
</dt> <dt>

[Типы звуковых носителей](audio-media-types.md)
</dt> <dt>

[Поддержка MPEG-4 в Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Поддерживаемые форматы мультимедиа в Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

