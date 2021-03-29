---
description: Microsoft Media Foundation кодировщик MPEG-2 — это Media Foundation преобразование, которое кодирует моно или стерео аудио в MPEG-1 Audio (ISO/IEC 11172-3) или MPEG-2 Audio (ISO/IEC 13818-3).
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: Кодировщик MPEG-2 Audio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2454e542ba59f4955668bd1fcefbf5dbc0f11551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898190"
---
# <a name="mpeg-2-audio-encoder"></a>Кодировщик MPEG-2 Audio

Microsoft Media Foundation кодировщик MPEG-2 — это [Media Foundation преобразование](media-foundation-transforms.md) , которое кодирует моно или стерео аудио в MPEG-1 Audio (ISO/IEC 11172-3) или MPEG-2 Audio (ISO/IEC 13818-3).

Кодировщик поддерживает звук уровня 1 и 2. Он не поддерживает MPEG-Layer 3 (MP3) Audio. Для MPEG-2 кодировщик поддерживает часть частоты дискретизации (LSF) звука MPEG-2. Он не поддерживает многоканальные расширения. В MFT выводится простейший поток MPEG. Он не может создавать пакетные элементарные потоки, потоки программы или потоки транспорта.

## <a name="class-identifier"></a>Идентификатор класса

Идентификатор класса (CLSID) кодировщика МЕПГ-2 — это **CLSID \_ CMPEG2AudioEncoderMFT**, определенный в файле заголовка вмкодекдсп. h.

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
<td>Обязательный. Необходимо <strong>MFAudioFormat_MPEG</strong>. Этот подтип используется как для MPEG-1, так и для звука MPEG-2.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Выборок в секунду.</td>
<td>Обязательный. Для MPEG-1 и MPEG-2 поддерживаются следующие значения:
<ul>
<li>32000</li>
<li>44100</li>
<li>48000</li>
</ul>
Кроме того, для MPEG-2 LSF поддерживаются следующие значения: <br/>
<ul>
<li>16000</li>
<li>22050</li>
<li>24 000</li>
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
<td>Скорость потока закодированных потоков MPEG (в байтах в секунду).</td>
<td>Необязательный элемент.<br/> Спецификации ISO/IEC 11172-3 и ISO/IEC 13818-3 (LSF) определяют несколько битовых ставок в зависимости от частоты выборки, количества каналов и звукового уровня (1 или 2). <br/> Кодировщик по умолчанию имеет звук уровня 2. Если атрибут <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> не задан, кодировщик использует следующие скорости по умолчанию:<br/>
<ul>
<li>Стерео MPEG-1 стереосистема: 224 000 бит/с в секунду (бит/с) = 28 000 байт в секунду.</li>
<li>MPEG-1 моно: 192 000 бит/с = 24 000 байт в секунду.</li>
<li>MPEG-2 LSF, моно или стерео: 160 000 бит/с = 20 000 байт в секунду.</li>
</ul>
Для этого атрибута можно задать другие значения. Если значение не является допустимым согласно спецификациям MPEG, то этот тип мультимедиа будет отклонен.<br/> Можно также задать скорость передачи данных с помощью интерфейса <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>икодекапи</strong></a> . Дополнительные сведения см. в разделе "Примечания".<br/></td>
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



 

Кодировщик не поддерживает преобразование "выборка" или "стерео/моно". Если необязательные атрибуты не заданы, кодировщик добавляет их в тип мультимедиа после задания типа.

## <a name="codec-properties"></a>Свойства кодека

Кодировщик поддерживает следующие свойства через интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) .



| Свойство                                                                                | Описание                                                                                      | Значение по умолчанию                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [КОДЕКАПИ \_ авенккоммонмеанбитрате](../directshow/avenccommonmeanbitrate-property.md)               | Указывает среднюю скорость кодирования в битах в секунду.                                      | Как описано в атрибуте [ \_ среднего числа байт в \_ \_ \_ \_ \_ секунду MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) на выходном носителе, введите.                      |
| [КОДЕКАПИ \_ авенкмпакодингмоде](../directshow/avencmpacodingmode-property.md)                       | Указывает режим кодирования звука MPEG.                                                          | Стерео для двухканального аудио-канала или одного канала для каналов с одним каналом.<br/> Для высококанального звука кодировщик также поддерживает двухканальный и совместный стерео.<br/> |
| [КОДЕКАПИ \_ авенкмпакопиригхт](../directshow/avencmpacopyright-property.md)                         | Указывает, следует ли задать бит авторского права в потоке MPEG.                             | Нет авторских прав.                                                                                                                                                          |
| [КОДЕКАПИ \_ авенкмпаемфасистипе](../directshow/avencmpaemphasistype-property.md)                   | Указывает тип фильтра отмены выделения, который должен использоваться при декодировании закодированного потока. | Не указано выделение.                                                                                                                                                 |
| [авенкмпаенаблередунданципротектион](../directshow/avencmpaenableredundancyprotection-property.md) | Указывает, следует ли добавить в заголовок кадра циклическую проверку избыточности (CRC).                    | Контрольная сумма CRC записывается в поток битов.                                                                                                                           |
| [КОДЕКАПИ \_ авенкмпалайер](../directshow/avencmpalayer-property.md)                                 | Задает звуковой слой MPEG.                                                                  | Звук уровня 2.                                                                                                                                                         |
| [КОДЕКАПИ \_ авенкмпаоригиналбитстреам](../directshow/avencmpaoriginalbitstream-property.md)         | Указывает, следует ли устанавливать для исходного бита в потоке MPEG.                          | "Исходный" бит отключен.                                                                                                                                                 |
| [КОДЕКАПИ \_ авенкмпаприватеусербит](../directshow/avencmpaprivateuserbit-property.md)               | Указывает, следует ли задавать значение для закрытого бита пользователя в потоке MPEG Audio.                      | Закрытый бит пользователя отключен.                                                                                                                                               |



 

Чтобы получить указатель на интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) , вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в MFT.

MFT реализует следующие методы [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) :

-   [**жетпараметерранже**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**жетпараметервалуес**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**Изменяемый**](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

Все остальные методы [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) возвращают **E \_ нотимпл**.

## <a name="remarks"></a>Комментарии

Каждая звуковая рамка MPEG содержит как 384 (уровень 1), так и 1152 (уровень 2) аудио выборки на канал. Однако каждый входной буфер кодировщика может содержать любое количество примеров PCM. Размер каждого входного буфера должен быть кратен выравниванию блока. Кодировщик кэширует входные образцы, пока не будет достаточно для звукового фрейма MPEG.

Каждый выходной буфер содержит один необработанный кадр MPEG. Размер каждого выходного буфера зависит от скорости потока и частоты выборки.

### <a name="configuring-the-encoder"></a>Настройка кодировщика

Чтобы изменить параметры по умолчанию для кодировщика, выполните следующие действия.

1.  Создайте экземпляр файла MFT кодировщика.
2.  Вызовите метод [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , чтобы получить список предпочтительных типов выходных данных. Кодировщик перечислит все частоты выборки для Mono и стерео. Выберите один из этих типов носителей в зависимости от частоты выборки и количества каналов. Значение [атрибута \_ \_ \_ Среднее \_ число байт в \_ \_ секунду для звука MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) указывает скорость по умолчанию (в байтах в секунду).
3.  Необязательно. можно переопределить скорость по умолчанию, задав новое значение для [среднего числа \_ байт \_ в \_ \_ \_ \_ секунду](mf-mt-audio-avg-bytes-per-second-attribute.md) на выходном типе носителя. Допустимые скорости работы зависят от частоты выборки, количества каналов и звукового уровня.
    > [!Note]  
    > На этом этапе настройки кодировщику по умолчанию присвоено звуковое сопровождение уровня 2 и принимается только скорость, равная 2 уровням. Вы сможете переключить кодировщик на слой 1 на более позднем этапе (см. шаг 7). В этом случае оставьте бит скорости по умолчанию для Now; его можно изменить на шаге 8.

     

4.  Вызовите метод [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , чтобы задать тип выходного носителя. Если вы задали собственное значение для [среднего двоичного \_ сигнала MF MT \_ \_ \_ \_ в \_ секунду](mf-mt-audio-avg-bytes-per-second-attribute.md) , а файл MFT отклоняет тип выходного носителя, скорее всего, вы указали недопустимую скорость.
5.  Вызовите [**имфтрансформ:: жетинпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) , чтобы перечислить входной тип носителя. Так как частота выборки и количество каналов должны совпадать с типом выходных данных, перечисляются только два параметра: 32-разрядный вход PCM с плавающей точкой и 16-разрядное целочисленное входное значение PCM. Выберите один из них.
6.  Вызовите [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) , чтобы задать тип входного носителя.
7.  Необязательно. для кодирования звука уровня 1 Установите для свойства [кодекапи \_ Авенкмпалайер](../directshow/avencmpalayer-property.md) значение **еавенкмпалайер \_ 1**.
8.  Необязательно. чтобы изменить скорость потока, задайте свойство [кодекапи \_ авенккоммонмеанбитрате](../directshow/avenccommonmeanbitrate-property.md) . Скорость потока должна быть одной из допустимых битов, перечисленных в спецификациях MPEG-1 или MPEG-2 LSF. Кроме того, можно вызвать метод [**икодекапи:: жетпараметервалуес**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) , чтобы получить список допустимых битовых ставок на основе текущих параметров.
9.  Необязательно. с помощью многоканального звука можно задать свойство [кодекапи \_ авенкмпакодингмоде](../directshow/avencmpacodingmode-property.md) , чтобы изменить режим кодирования на Dual-канальное или совместное стерео. Чтобы получить допустимые параметры, можно вызвать метод [**икодекапи:: жетпараметерранже**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) . (Для звука с 1 каналом единственным вариантом является Mono.)
10. Необязательно. задайте любые другие свойства [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) , перечисленные ранее.

Важно следовать порядку этих шагов. В частности, перед изменением свойств [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) задайте тип выходного носителя. Кроме того, необходимо задать свойства **икодекапи** до того, как MFT получит первый входной пример. После того как MFT получит входные данные, свойства кодека будут доступны только для чтения, а [**икодекапи:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) возвращает значение **\_ false**.

### <a name="supported-bit-rates"></a>Поддерживаемые скорости

Кодировщик поддерживает следующие скорости.



MPEG-1

MPEG-2

Уровень 1

Уровень 2

Уровень 1

Уровень 2

32

32\*

32

8

64

48\*

38

16

96

56\*

56

24

128

64

64

32

160

80\*

80

40

192

96

96

48

224

112

112

56

256

128

128

64

288

160

144

80

320

192

160

96

352

224\*\*

176

112

384

256\*\*

192

128

416

230\*\*

224

144

448

384\*\*

256

160



 

<dl> \* Только моно  
\*\* Только стерео  
</dl>

### <a name="example-media-types"></a>Примеры типов мультимедиа

Ниже приведен пример типов мультимедиа, которые необходимы для кодирования 16-разрядного целочисленного PCM 48-кГц при скорости по умолчанию.

Тип выходного носителя:

| attribute                                                                           | Значение                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [\_ \_ основной тип MF \_ MT](mf-mt-major-type-attribute.md)                               | **Мфмедиатипе \_ аудио**  |
| [подтип MF \_ MT \_](mf-mt-subtype-attribute.md)                                      | **Мфаудиоформат \_ MPEG** |
| [\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду](mf-mt-audio-samples-per-second-attribute.md) | 48000                   |
| [\_ \_ каналы аудиосигнала MF MT \_ \_](mf-mt-audio-num-channels-attribute.md)              | 2                       |



 

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
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| DLL<br/>                      | <dl> <dt>Msmpeg2enc.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> </dl>

 

 
