---
description: 'Microsoft Media Foundation декодер AAC — это Media Foundation преобразование, которое декодирует следующие дополнительные профили расширенного кодирования звука (AAC) и высокоэффективных профилей AAC (HE-AAC):'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: Декодер AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82dde090dee98cddce9658366bde593b5fc779d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701473"
---
# <a name="aac-decoder"></a>Декодер AAC

Microsoft Media Foundation декодер AAC — это [Media Foundation преобразование](media-foundation-transforms.md) , которое декодирует следующие дополнительные профили расширенного кодирования звука (AAC) и высокоэффективных профилей AAC (HE-AAC):

-   Профиль низкой сложности MPEG-2 AAC (LC) (многоканальный).
-   MPEG-4 HE-AAC v1 (многоканальный) с AAC-LC Core.
-   MPEG-4 HE-AAC v2 (стерео) с AAC-LC Core.

Декодер AAC поддерживает как необработанные AAC потоки без заголовков, так и AAC в потоке передачи звуковых данных (ADTS).

Начиная с Windows 8, декодер AAC также поддерживает декодирование потоков потокового транспорта MPEG-4 с уровнем мультиплексирования (ЛАТМ) и уровнем синхронизации (УРОВНЯМИ гарантии). Он также может преобразовать поток ЛАТМ/УРОВНЯМИ гарантии в ADTS.

## <a name="media-types"></a>Типы носителей

Декодер AAC поддерживает следующие типы носителей.

### <a name="input-types"></a>Типы входных данных

Декодер AAC поддерживает следующие подтипы звука:



| Subtype                     | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Header       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MFAudioFormat_AAC**      | Необработанный AAC или ADTS AAC.<br/> Для этого подтипа мультимедиа тип носителя предоставляет частоту выборки и число каналов перед применением средств Спектрал (SBR) Replication и параметрической стерео (PS), если они есть. Результатом работы средства SBR является двойная декодированная частота выборки по сравнению с частотой выборки ядра AAC-LC. Результатом работы средства PS является декодирование стерео из потока AAC-LC ядра Mono.<br/> Этот подтип эквивалентен **MEDIASUBTYPE_MPEG_HEAAC**, определенному в вмкодекдсп. h. См. раздел [идентификаторы GUID для звуковых подтипов](audio-subtype-guids.md). <br/> Этот подтип выводится с помощью [источника файлов MPEG-4](mpeg-4-file-source.md) и средства синтаксического анализа ADTS. <br/> | мфапи. h      |
| **MEDIASUBTYPE_RAW_AAC1** | Необработанный AAC. <br/> Этот подтип используется для AAC, содержащихся в AVI-файле, с тегом формата Audio, равным WAVE_FORMAT_RAW_AAC1 (0x00FF). <br/> Для этого подтипа тип носителя предоставляет частоту выборки и число каналов после применения инструментов SBR и PS, если они есть.<br/>                                                                                                                                                                                                                                                                                                                                                                                      | вмкодекдсп. h |



 

Чтобы настроить декодер AAC, задайте следующие атрибуты для входного типа носителя.



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
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Основной тип.</td>
<td>Необходимо <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Подтип аудио.</td>
<td>Дополнительные сведения см. в описании выше.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Профиль и уровень звука. <br/></td>
<td>Необязательный элемент. Применяется только к <strong>MFAudioFormat_AAC</strong>. <br/> Значением этого атрибута является поле <strong>аудиопрофилелевелиндикатион</strong> , ОПРЕДЕЛЕННОЕ в стандарте ISO/IEC 14496-3. <br/> Если неизвестно, задайте для параметра значение 0 или 0xFE ( &quot; профиль звука не указан &quot; ).<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>Тип полезных данных.<br/></td>
<td>Применяется только к <strong>MFAudioFormat_AAC</strong>. Декодер поддерживает следующие типы полезных данных: <br/>
<ul>
<li>0: необработанный AAC. Поток содержит только элементы raw_data_block (), как определено в формате MPEG-2.</li>
<li>1: ADTS. Поток содержит adts_sequence (), как определено в формате MPEG-2. Допускается только один raw_data_block () на adts_frame ().</li>
<li>3: потоковый транспорт потока с уровнем синхронизации (УРОВНЯМИ гарантии) и уровнем мультиплексирования (ЛАТМ). Из трех типов УРОВНЯМИ гарантии поддерживается только <strong>аудиосинкстреам</strong> . Уровень мультиплексора — <strong>аудиомукселемент</strong>, ограничен одной звуковой программой и одним слоем.</li>
</ul>
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> является необязательным. Если этот атрибут не указан, используется значение по умолчанию 0, которое указывает, что поток содержит только элементы raw_data_block.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Требуемая битовая глубина декодированного звука PCM.</td>

</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></td>
<td>Указывает назначение звуковых каналов для позиционирования динамиков.</td>
<td>Необязательный элемент. Дополнительные сведения см. в разделе <a href="#format-constraints">ограничения формата</a>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Количество каналов, включая канал с низкой частотой (НИЗКОЧАСТОТный), если он есть.<br/></td>
<td>Интерпретация этого значения зависит от подтипа носителя, как описано выше.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Частота выборки, в примерах в секунду.<br/></td>
<td>Интерпретация этого значения зависит от подтипа носителя, как описано выше.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></td>
<td>Дополнительные сведения о форматировании.</td>
<td>Значение этого атрибута зависит от подтипа.<br/>
<ul>
<li><strong>MFAudioFormat_AAC</strong>: содержит часть структуры <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>хеааквавеинфо</strong></a> , которая появляется после структуры <strong>вавеформатекс</strong> (то есть после элемента <strong>вфкс</strong> ). За ним следуют данные АудиоспеЦификконфиг () в соответствии с определением ISO/IEC 14496-3.</li>
<li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: содержит данные аудиоспеЦификконфиг (). Эти данные должны отобразиться; в противном случае декодер отклонит тип мультимедиа.</li>
</ul>
Длина данных АудиоспеЦификконфиг () составляет 2 байта для AAC-LC или AAC с неявным сигналом SBR/PS. Это более 2 байта для AAC с явной сигнализацией SBR/PS.<br/> Значение <strong>аудиубжекттипе</strong> , определенное в аудиоспеЦификконфиг (), должно быть равно 2, что означает AAC-LC. Значение параметра <strong>екстенсионаудиубжекттипе</strong> должно быть равно 5 для SBR или 29 для PS. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a>Типы вывода

Декодер поддерживает следующие типы выходных данных:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Subtype</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MFAudioFormat_Float</strong></td>
<td>Звук IEEE с плавающей точкой.</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>16-разрядный звук PCM.</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>Требуется Windows 8. <br/> Этот тип выходных данных можно использовать для преобразования потока AAC в формате УРОВНЯМИ гарантии/ЛАТМ в формат ADTS. <br/> Чтобы преобразовать поток УРОВНЯМИ гарантии/ЛАТМ в поток ADTS, задайте тип входных данных <strong>MFAudioFormat_AAC</strong> с типом полезных данных 3 (уровнями гарантии). Затем задайте тип выходных данных <strong>MFAudioFormat_AAC</strong> с типом полезных данных 1 (ADTS). Декодер будет переформатировать конаинтер без декодирования битовый поток. <br/>
<blockquote>
[!Note]<br />
Декодер не регистрирует <strong>MFAudioFormat_AAC</strong> как тип выходных данных. Однако если приложение задает тип входных данных, как описано, метод <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>имфтрансформ:: жетаутпутаваилаблетипе</strong></a> возвращает <strong>MFAudioFormat_AAC</strong> в списке доступных типов вывода.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

Если входной поток содержит более двух каналов, декодер AAC предоставляет два варианта выходного формата:

-   Та же конфигурация канала, что и у входного типа.
-   Переход на стереосистему.

## <a name="format-constraints"></a>Ограничения формата

Декодированная частота выборки звука должна быть одной из следующих: после применения SBR (при наличии).

-   8 кГц
-   11,025 кГц
-   12 кГц
-   16 кГц
-   22,05 кГц
-   24 кГц
-   32 кГц
-   44,1 кГц
-   48 кГц

Частоты выборки выше 48 кГц не поддерживаются.

Декодер поддерживает до 6 каналов звука. Для каждой конфигурации динамика декодер ожидает, чтобы AAC синтаксические элементы отображались в определенном порядке. В следующей таблице перечислены поддерживаемые конфигурации динамиков. В третьем столбце таблицы перечислены ожидаемые синтаксические элементы и их порядок, используя следующую нотацию:

-   <SCE1>: Single_channel_element (SCE), связанный с динамиком переднего плана.
-   <SCE2>: SCE, связанный с докладчиком центра.
-   <CPE1>: Channel_pair_element (CPE), связанный с передними динамиками.
-   <CPE2>: CPE, связанный с задними (или боковыми) динамиками
-   <LFE>: Lfe_channel_element (НИЗКОЧАСТОТный).

Дополнительные сведения об этих синтаксических элементах см. в статье ISO/IEC 13818-7.



| Конфигурация       | Маска канала                                                                                                                                                              | AAC синтаксические элементы                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Mono                | **SPEAKER_FRONT_CENTER**                                                                                                                                                | <SCE1>                                    |
| Стерео или Dual Mono | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**                                                                                                                     | <CPE1>                                    |
| 2/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**                                                                                        | <CPE1><SCE1>                        |
| 2/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                                              | <CPE1><CPE2>                        |
| 3/0                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**                                                                                       | <SCE1><CPE1>                        |
| 3/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**                                                          | <SCE1><CPE1><SCE2>            |
| 3/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                | <SCE1><CPE1><CPE2>            |
| 3/2 + НИЗКОЧАСТОТНЫЙ           | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT** | <SCE1><CPE1><CPE2><LFE> |



 

Для необработанных AAC каждый входной пример должен содержать ровно один полный сжатый кадр AAC.

Для ADTS каждый входной образец может содержать несколько звуковых кадров, а также частичные кадры, т. е. фреймы могут охватывать границы выборки. За каждым заголовком ADTS должен следовать один кадр AAC.

Декодер AAC не поддерживает следующие действия:

-   Основной профиль, Sample-Rate масштабируемый профиль (SRS) или профиль долгосрочного прогноза (ЛТП).
-   Формат обмена звуковых данных (АДИФ).
-   Транспортные потоки ЛАТМ/Лаос.
-   Элементы сопряженного канала (Кцес). Декодер пропустит звуковые кадры с помощью Кцес.
-   AAC-LC с 960-примерным размером кадра. Поддерживаются только 1024-образцы кадров.

## <a name="transform-attributes"></a>Атрибуты преобразования

Декодер AAC реализует метод [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Приложения могут использовать этот метод для получения или установки следующих атрибутов.



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
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></td>
<td>Указывает, кодируется ли двухканальный аудио-канал как стерео или два Mono. Рассматривать как доступное только для чтения.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></td>
<td>Указывает, как декодер воспроизводит два моно аудио. Значение по умолчанию — <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: output CH1 для левого и правого докладчика. <br/> Приложения могут установить это свойство, чтобы изменить поведение по умолчанию.<br/></td>
</tr>
<tr class="odd">
<td><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></td>
<td>Декодер AAC не обрабатывает изменения динамического формата и должен быть сброшен или очищен до установки нового типа входного носителя. Рассматривайте этот атрибут как доступный только для чтения. <br/>
<blockquote>
[!Note]<br />
Декодер AAC неправильно сообщает значение <strong>true</strong> для этого атрибута.
</blockquote>
<br/> <br/> В Windows 7 декодер неправильно сообщает значение <strong>true</strong> для этого атрибута. В Windows 8 декодер сообщает <strong>false</strong>, что является правильным значением<br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a>Примеры типов мультимедиа

Ниже приведен пример типа входного носителя, необходимого для потока AAC-LC с 6 каналами, 48 кГц, с использованием необработанных полезных данных AAC:



| attribute                                                                                      | Значение                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                      | **MFMediaType_Audio**                                                               |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat_AAC**                                                               |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)        | 48000                                                                                |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                     | 6                                                                                    |
| [MF_MT_AAC_PAYLOAD_TYPE](mf-mt-aac-payload-type.md)                                       | 0                                                                                    |
| [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x2A, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0} |
| [MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION](mf-mt-aac-audio-profile-level-indication.md) | 0x2A (необязательно)                                                                      |



 

Первые 12 байт [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) соответствуют следующим элементам структуры [**хеааквавеинфо**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) :

-   **впайлоадтипе** = 0 (необработанный AAC)
-   **ваудиопрофилелевелиндикатион** = 0X2a (профиль AAC, уровень 4)
-   **вструкттипе** = 0

Последние два байта [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) содержат значение аудиоспеЦификконфиг () в соответствии с определением MPEG-4.

-   АудиоспеЦификконфиг. Аудиубжекттипе = 2 (AAC LC) (5 бит)
-   АудиоспеЦификконфиг. Самплингфрекуенцииндекс = 3 (4 бита)
-   АудиоспеЦификконфиг. Чаннелконфигуратион = 6 (4 бита)
-   ГаспеЦификконфиг. Фрамеленгсфлаг = 0 (1 бит)
-   ГаспеЦификконфиг. Депендсонкорекодер = 0 (1 бит)
-   ГаспеЦификконфиг. Екстенсионфлаг = 0 (1 бит)

Учитывая этот тип входных данных, используйте следующий тип выходного носителя для получения 6-канального звука PCM с плавающей запятой, 32-битного из декодера:



| attribute                                                                                    | Значение                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                    | **MFMediaType_Audio**   |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat_Float** |
| [**MF_MT_AUDIO_BITS_PER_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md)            | 32                       |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)      | 48000                    |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                   | 6                        |
| [**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 1152000 (необязательно)       |
| [**MF_MT_AUDIO_BLOCK_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)             | 24 (необязательно)            |
| [**MF_MT_AUDIO_CHANNEL_MASK**](mf-mt-audio-channel-mask-attribute.md)                   | 0x3F (необязательно)          |



 

Если установлена поддержка обновления платформы для Windows Vista, то декодер AAC Audio доступен в Windows Vista, но доступен только в Windows Vista с помощью [средства чтения исходного кода](source-reader.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                                                                                                  |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                                                                                                     |
| DLL<br/>                      | <dl> <dt>Msmpeg2adec.dll в Windows 7; </dt> <dt>MSAudDecMFT.dll в Windows 8</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Типы носителей AAC](aac-media-types.md)
</dt> <dt>

[Типы звуковых носителей](audio-media-types.md)
</dt> <dt>

[**Декодер звука Microsoft MPEG-1/DD/AAC**](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[Поддержка MPEG-4 в Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Поддерживаемые форматы мультимедиа в Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>
