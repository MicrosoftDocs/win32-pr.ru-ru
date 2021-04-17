---
description: Декодер Windows Media Audio декодирует звуковые потоки, закодированные кодировщиком Windows Media Audio.
ms.assetid: 2d8e4a97-34a7-4eee-9567-7ae98fa282b9
title: Декодер Windows Media Audio (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f11242f237b8d9709baea6d445a8426236913c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694745"
---
# <a name="windows-media-audio-decoder"></a>Декодер Windows Media Audio

Декодер Windows Media Audio декодирует звуковые потоки, закодированные [**кодировщиком Windows Media Audio**](windowsmediaaudioencoder.md). Кодировщик и декодер поддерживают три категории закодированных аудио: Windows Media Audio Standard, Windows Media Audio Professional и Windows Media Audio без потерь.

## <a name="class-identifier"></a>Идентификатор класса

Идентификатор класса (CLSID) для декодера Windows Media Audio представлен константой **CLSID \_ квмадекмедиаобжект**. Вы можете создать экземпляр звукового декодера, вызвав **CoCreateInstance**.

## <a name="input-formats"></a>Форматы входных данных

В следующей таблице показаны Теги звукового формата, которые представляют входные категории, поддерживаемые декодером Windows Media Audio. Сведения о том, как задать типы входных и выходных данных для декодера, см. в разделе [Настройка декодирования звука](configuringaudiodecoding.md).



| Формат константы тега             | Формат значения тега | Формат аудио                     |
|---------------------------------|------------------|----------------------------------|
| \_Формат волны \_ WMAUDIO2          | 0x0161           | Windows Media Audio Standard     |
| \_Формат волны \_ WMAUDIO3          | 0x0162           | Windows Media Audio Professional |
| \_Формат Wave \_ вмаудио \_ без потерь | 0x0163           | Windows Media Audio без потерь     |



 

## <a name="output-formats"></a>Форматы выходных данных

В следующей таблице показаны Теги звукового формата, представляющие типы выходных данных, поддерживаемые **декодером Windows Media Audio**. Сведения о том, как задать типы входных и выходных данных для декодера, см. в разделе [Настройка кодирования звука](configuringaudioencoding.md).



| Формат константы тега       | Формат значения тега | Формат аудио                                          |
|---------------------------|------------------|-------------------------------------------------------|
| формат ВОЛНового \_ \_ PCM         | 0x0001           | Формат PCM                                            |
| \_Формат волны \_ IEEE \_ float | 0x0003           | IEEE с плавающей запятой                                   |
| формат ВОЛНового \_ \_ расширения  | 0xFFFE           | Формат PCM/IEEE в структуре **вавеформатекстенсибле** |



 

## <a name="interfaces"></a>Интерфейсы

Объект звукового декодера предоставляет интерфейс **имедиаобжект** , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс **имфтрансформ** , чтобы объект можно было использовать в качестве Media Foundation преобразования (MFT).

Декодер Windows Media Audio работает как DMO или MFT в зависимости от того, какие интерфейсы получены и какая версия Windows работает. В следующей таблице показаны условия, при которых звуковой декодер ведет себя как DMO или MFT.



| Операционная система | Поведение декодера                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Декодер Windows Media Audio всегда ведет себя как DMO.                                                                                                                                |
| Windows Vista    | По умолчанию декодер Windows Media Audio ведет себя как DMO. Если вы получаете интерфейс **имфтрансформ** или интерфейс **ипропертисторе** для звукового декодера, он ведет себя как MFT. |
| Windows 7        | По умолчанию декодер Windows Media Audio ведет себя как DMO. Если вы получаете интерфейс **имфтрансформ** для звукового декодера, он ведет себя как MFT.                                    |



 

## <a name="properties"></a>Свойства

Декодер Windows Media Audio поддерживает следующие свойства.



<table>
<thead>
<tr class="header">
<th>Свойство</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></td>
<td>Указывает максимальное количество дополнительных выборок PCM, которые могут быть возвращены в конце декодирования файла.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></td>
<td>Указывает режим управления динамическим диапазоном, который будет использоваться декодером аудио.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></td>
<td>Указывает предоставляемые автором коэффициенты свертывания для декодирования многоканального звука для меньшего количества каналов, чем содержит закодированный поток. <br/> <dl> Windows XP и более поздние версии.<br />
Professional<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></td>
<td>Указывает, должен ли декодер звука предоставлять выходные данные высокого разрешения.<br/> <dl> Windows XP и более поздние версии.<br />
Профессиональная, без потерь.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></td>
<td>Указывает, должен ли звуковой декодер выполняться Lt-Rt свертывания.<br/> <dl> Windows Vista и более поздние версии.<br />
Professional.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></td>
<td>Указывает конфигурацию динамика на клиентском компьютере.<br/> <dl> Windows XP и более поздние версии.<br />
Professional.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>Указывает средний уровень громкости звукового содержимого.<br/> <dl> Windows XP и более поздние версии.<br />
Профессиональная, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></td>
<td>Указывает требуемый средний уровень громкости выходного звукового содержимого.<br/> <dl> Windows XP и более поздние версии.<br />
Профессиональная, без потерь.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>Указывает самый высокий уровень громкости в аудио содержимом.<br/> <dl> Windows XP и более поздние версии.<br />
Профессиональная, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></td>
<td>Указывает требуемый максимальный уровень громкости выходного аудио содержимого.<br/> <dl> Windows XP и более поздние версии.<br />
Профессиональная, без потерь.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows XP, Windows Vista или Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmadmod.dll</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Реализация кодека](codecimplementation.md)
</dt> </dl>

 

 




