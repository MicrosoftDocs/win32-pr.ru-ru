---
description: 'Кодировщик Windows Media Audio кодирует звуковые потоки. Кодировщик поддерживает три категории закодированных выходных данных: Windows Media Audio Standard, Windows Media Audio Professional и Windows Media Audio без потерь.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Кодировщик Windows Media Audio (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f1d5b9e5f890a43958bcc304dd2d305844fdb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718090"
---
# <a name="windows-media-audio-encoder"></a>Кодировщик Windows Media Audio

Кодировщик Windows Media Audio кодирует звуковые потоки. Кодировщик поддерживает три категории закодированных выходных данных: Windows Media Audio Standard, Windows Media Audio Professional и Windows Media Audio без потерь.

## <a name="class-identifier"></a>Идентификатор класса

Идентификатор класса (CLSID) для кодировщика Windows Media Audio представлен константой **CLSID \_ квмаенкмедиаобжект**. Вы можете создать экземпляр звукового кодировщика, вызвав **CoCreateInstance**.

## <a name="input-formats"></a>Форматы входных данных

В следующей таблице показаны Теги звукового формата, представляющие входные категории, поддерживаемые кодировщиком Windows Media Audio. Сведения о том, как задать типы входных и выходных данных для кодировщика, см. в разделе [Настройка кодирования звука](configuringaudioencoding.md).



| Формат константы тега       | Формат значения тега | Формат аудио                                          |
|---------------------------|------------------|-------------------------------------------------------|
| формат ВОЛНового \_ \_ PCM         | 0x0001           | Формат PCM                                            |
| \_Формат волны \_ IEEE \_ float | 0x0003           | IEEE с плавающей запятой                                   |
| формат ВОЛНового \_ \_ расширения  | 0xFFFE           | Формат PCM/IEEE в структуре **вавеформатекстенсибле** |



 

## <a name="output-formats"></a>Форматы выходных данных

В следующей таблице показаны Теги звукового формата, представляющие категории вывода, поддерживаемые кодировщиком Windows Media Audio.



| Формат константы тега             | Формат значения тега | Формат аудио                     |
|---------------------------------|------------------|----------------------------------|
| \_Формат волны \_ WMAUDIO2          | 0x0161           | Windows Media Audio Standard     |
| \_Формат волны \_ WMAUDIO3          | 0x0162           | Windows Media Audio Professional |
| \_Формат Wave \_ вмаудио \_ без потерь | 0x0163           | Windows Media Audio без потерь     |



 

## <a name="interfaces"></a>Интерфейсы

Объект audio ендодер предоставляет интерфейс **имедиаобжект** , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс **имфтрансформ** , чтобы объект можно было использовать в качестве Media Foundation преобразования (MFT).

Кодировщик Windows Media Audio работает как DMO или MFT в зависимости от того, какие интерфейсы получены и какая версия Windows работает. В следующей таблице показаны условия, при которых звуковый кодировщик ведет себя как DMO или MFT.



| Операционная система | Поведение кодировщика                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Кодировщик Windows Media Audio всегда ведет себя как DMO.                                                                                                                                |
| Windows Vista    | По умолчанию кодировщик Windows Media Audio ведет себя как DMO. Если вы получаете интерфейс **имфтрансформ** или интерфейс **ипропертисторе** в звуковом кодировщике, он ведет себя как MFT. |
| Windows 7        | По умолчанию кодировщик Windows Media Audio ведет себя как DMO. Если вы получаете интерфейс **имфтрансформ** в звуковом кодировщике, он ведет себя как MFT.                                    |



 

## <a name="encoder-properties"></a>Свойства кодировщика

Кодировщик Windows Media Audio поддерживает следующие свойства.



<table>
<thead>
<tr class="header">
<th>Свойство</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></td>
<td>Указывает, использует ли кодировщик среднее-управляемое кодирование VBR.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с пиковой скоростью.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></td>
<td>Указывает, должен ли кодировщик проверять согласованность данных между проходами при выполнении двусторонней кодировки VBR. <br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></td>
<td>Указывает, ограничивается ли кодировщик максимальным требованием к задержке декодера.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></td>
<td>Указывает, ограничена ли сложность алгоритма кодирования.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></td>
<td>Указывает, ограничивается ли кодировщик максимальным требованием к задержке.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Указывает, ограничены ли режимы, перечисленные кодировщиком, теми, которые соответствуют требованиям к качеству.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Указывает профиль сложности закодированного содержимого.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Задает требуемый уровень качества для кодирования VBR.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></td>
<td>Указывает, использует ли кодировщик подстановку шума.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></td>
<td>Указывает, использует ли кодировщик ограничение диапазона PCM.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></td>
<td>Указывает максимальную закодированную пропускную способность, допустимую при усечении полосы пропускания в кодировщике.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></td>
<td>Указывает минимальную закодированную пропускную способность, допустимую при усечении полосы пропускания в кодировщике.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></td>
<td>Определяет качество, при котором разрешена Минимальная пропускная способность. <br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></td>
<td>Определяет качество, при котором разрешена максимальная пропускная способность.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></td>
<td>Указывает, выполняет ли кодировщик чередование усечения.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></td>
<td>Указывает, использует ли кодировщик стиль вычисления маски, выполняемый в версии 7 кодировщика Windows Media Audio.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></td>
<td>Указывает, выполняет ли кодировщик обработку стерео изображений. <br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></td>
<td>Указывает окно буфера (в миллисекундах) для кодировщика, который настроен для использования среднего управляемого кодирования VBR.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></td>
<td>Указывает среднюю скорость потока в битах в секунду для кодировщика, который настроен для использования среднего управляемого кодирования VBR.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></td>
<td>Указывает сложность алгоритма кодирования.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Задает конец прохода кодирования.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></td>
<td>Указывает, использует ли основной кодировщик &quot; функцию «плюс» &quot; .<br/> <dl> Windows Vista и более поздние версии.<br />
Professional.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></td>
<td>Указывает максимальную задержку для декодера в миллисекундах.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></td>
<td>Указывает максимальную задержку кодировщика в миллисекундах.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Задает уровень качества VBR последнего перечислимого типа выходных данных.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Указывает максимальное число проходов, поддерживаемое кодировщиком.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Указывает число проходов, которые кодировщик будет использовать для кодирования содержимого.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></td>
<td>Указывает, ограничивается ли скорость кодировщика пиковым битом.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></td>
<td>Указывает предпочтительное количество выборок на кадр.<br/> <dl> Windows Vista и более поздние версии.<br />
Professional.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></td>
<td>Указывает, должен ли кодировщик использовать предпочтительный размер кадра.<br/> <dl> Windows Vista и более поздние версии.<br />
Professional.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Указывает пиковую скорость потока (в битах в секунду), используемую для ограниченного 2-прохода с переменной скоростью (VBR). <br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></td>
<td>Указывает среднее окно буфера (в миллисекундах) закодированного потока.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></td>
<td>Указывает максимальное окно буфера (в миллисекундах) закодированного потока.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></td>
<td>Указывает среднюю скорость в битах в секунду для закодированного потока.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></td>
<td>Указывает максимальную скорость в битах в секунду для закодированного потока.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Указывает, использует ли кодировщик кодирование VBR.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></td>
<td>В настоящее время это свойство не используется кодеком Windows Media Audio.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>Указывает средний уровень громкости звукового содержимого.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>Указывает самый высокий уровень громкости в аудио содержимом.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></td>
<td>Указывает среднее число байтов в секунду для звука с кодировкой VBR.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></td>
<td>Указывает, должен ли кодировщик создавать 1 пакет WMA на кадр.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></td>
<td>Указывает, должен ли кодировщик создавать динамические параметры управления диапазоном.<br/> <dl> Windows Vista и более поздние версии.<br />
Standard, Professional, без потерь.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></td>
<td>Указывает структуру <strong>вавеформатекс</strong> , описывающую входное звуковое содержимое.<br/> <dl> Windows XP и более поздние версии.<br />
Standard, Professional.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></td>
<td>Указывает, должен ли кодировщик включать кодирование S/PDIF в реальном времени.<br/> <dl> Windows Vista и более поздние версии.<br />
Professional.<br />
Read/write.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows XP, Windows Vista или Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmadmoe.dll</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Реализация кодека](codecimplementation.md)
</dt> </dl>

 

 




