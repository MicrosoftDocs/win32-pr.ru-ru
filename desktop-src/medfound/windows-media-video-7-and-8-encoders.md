---
description: кодировщик Windows media video 7/8 реализует предыдущие Windows версии кодировщика видео мультимедиа.
ms.assetid: c4165614-b9ec-4216-b36c-f57bc05e3a8e
title: Windows Кодировщик Media Video 7/8 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252a015d2cae826e36eb27b29162df9f5bea525be19e074cf1af2e22b204fa19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117688296"
---
# <a name="windows-media-video-78-encoder"></a>Windows Кодировщик Media Video 7/8

кодировщик Windows media video 7/8 реализует предыдущие Windows версии кодировщика видео мультимедиа.

## <a name="class-identifier"></a>Идентификатор класса

идентификатор класса (clsid) для кодировщика Windows Media Video 7/8 — это **CLSID \_ квмвксенкмедиаобжект**. Экземпляр кодировщика можно создать, вызвав **CoCreateInstance**.

## <a name="interfaces"></a>Интерфейсы

объект видеокодировщика предоставляет интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , чтобы объект можно было использовать как преобразование Media Foundation (MFT).

видеокодировщик ведет себя как DMO или файл MFT в зависимости от того, какие интерфейсы вы получаете и какая версия Windows выполняется. в следующей таблице показаны условия, при которых кодировщик видео ведет себя в виде DMO или MFT.



| Операционная система            | Поведение кодировщика                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | кодировщик Windows Media video всегда ведет себя как DMO.                                                                                                                |
| Windows Vista и Windows 7 | по умолчанию Windows кодировщика видео мультимедиа ведет себя как DMO. Если вы получаете интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) для видеокодировщика, он ведет себя как файл MFT. |



 

## <a name="input-formats"></a>Форматы входных данных

кодировщик видео Windows media поддерживает следующие входные подтипы носителей, когда он выступает в качестве DMO.

-   МЕДИАСУБТИПЕ \_ ийув
-   МЕДИАСУБТИПЕ \_ I420
-   МЕДИАСУБТИПЕ \_ YV12
-   МЕДИАСУБТИПЕ \_ NV11
-   МЕДИАСУБТИПЕ \_ NV12
-   МЕДИАСУБТИПЕ \_ YUY2
-   МЕДИАСУБТИПЕ \_ UYVY
-   МЕДИАСУБТИПЕ \_ ивю
-   МЕДИАСУБТИПЕ \_ RGB32
-   МЕДИАСУБТИПЕ \_ Rgb24
-   МЕДИАСУБТИПЕ \_ RGB565
-   МЕДИАСУБТИПЕ \_ RGB555
-   МЕДИАСУБТИПЕ \_ RGB8
-   МЕДИАСУБТИПЕ \_

кодировщик видео Windows media поддерживает следующие входные подтипы носителя, когда он выступает в качестве MFT.

-   Мфвидеоформат \_ ийув
-   Мфвидеоформат \_ I420
-   Мфвидеоформат \_ YV12
-   Мфвидеоформат \_ NV11
-   Мфвидеоформат \_ NV12
-   Мфвидеоформат \_ YUY2
-   Мфвидеоформат \_ UYVY
-   Мфвидеоформат \_ ивю
-   Мфвидеоформат \_ RGB32
-   Мфвидеоформат \_ Rgb24
-   Мфвидеоформат \_ RGB565
-   Мфвидеоформат \_ RGB555
-   Мфвидеоформат \_ RGB8
-   МЕДИАСУБТИПЕ \_

## <a name="output-formats"></a>Форматы выходных данных

в следующей таблице показаны коды из четырех символов (фаурккс) для типов выходных данных, поддерживаемых кодировщиком Windows Media Video 7/8.



| Категория              | FOURCC |
|-----------------------|--------|
| Windows Media Video 7 | "WMV1" |
| Windows Media Video 8 | "WMV2" |



 

## <a name="properties"></a>Свойства

кодировщик Windows Media Video 7/8 поддерживает следующие свойства.



<table>
<thead>
<tr class="header">
<th>Свойство</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></td>
<td>Указывает дополнительную нагрузку в байтах на пакет, необходимую для контейнера, используемого для хранения сжатого содержимого.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>Указывает среднюю частоту кадров содержимого видео в кадрах в секунду.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с средней скоростью (заданным <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).<br/> <dl> Windows XP и более поздних версий.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с пиковой скоростью (заданное <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).<br/> <dl> Windows XP и более поздних версий.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>Указывает, содержит ли закодированный поток видео значение полных буферов со всеми ключевыми кадрами.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>Указывает число кадров видео, закодированных кодеком.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>Указывает количество видеокадров, закодированных кодеком, который фактически содержит данные.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></td>
<td>Это свойство заменяется <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></td>
<td>Указывает сложность алгоритма кодировщика.<br/> <dl> Windows Vista и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>Задает числовое представление компромисса между плавностью движения и качеством изображения в выходных данных кодека.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Указывает шаблон соответствия устройства, которому соответствует закодированное содержимое.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>Указывает шаблон соответствия устройств, который вы хотите использовать для кодирования видео.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>Указывает число кадров видео, отброшенных во время кодирования.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Задает конец прохода кодирования.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>Указывает FOURCC, определяющую кодировщик, который вы хотите использовать.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>Указывает, следует ли использовать чередование выходных данных кодека.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>Указывает максимальное время в миллисекундах между опорными кадрами в выходных коде.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Указывает максимальное число проходов, поддерживаемое кодеком.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Указывает число проходов, которые кодек будет использовать для кодирования содержимого.<br/> <dl> Windows XP и более поздних версий.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>Указывает, создает ли кодировщик фиктивные записи кадра в битовом потоке для повторяющихся кадров.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>Указывает QP.<br/> <dl> Windows Vista и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>Указывает среднюю скорость потока в битах в секунду, используемую для 2-проходной кодировки с переменной скоростью (VBR).<br/> <dl> Windows XP и более поздних версий.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Указывает пиковую скорость потока (в битах в секунду), используемую для ограниченного 2-прохода переменной-разрядной скорости (VBR).<br/> <dl> Windows XP и более поздних версий.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>Указывает число кадров видео, переданных кодировщику во время процесса кодирования.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Указывает, будет ли кодек использовать кодирование с переменной скоростью (VBR).<br/> <dl> Windows XP и более поздних версий.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>Задает реальный уровень качества для кодирования с переменной скоростью (1 проход) с учетом качества (с частотой VBR).<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>Указывает объем содержимого в миллисекундах, который может поместиться в буфер модели.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>Указывает число пропущенных видеокадров, так как они являлись дубликатами предыдущих кадров.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows XP, Windows Vista или Windows 7<br/>                                       |
| Заголовок<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvxencd.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Реализация кодека](codecimplementation.md)
</dt> <dt>

[Идентификаторы GUID для подтипов видео](video-subtype-guids.md)
</dt> </dl>

 

 
