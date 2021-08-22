---
description: кодировщик экрана Windows Media видео 9 оптимизирован для кодирования последовательных снимков экрана от компьютерных мониторов.
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: Windows Кодировщик экрана Media Video 9 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6d9fbe59671d978fb7374acbbc8ed1d8e9ea5afded0154242c4d1ccb4df3d4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713144"
---
# <a name="windows-media-video-9-screen-encoder"></a>Windows Кодировщик экрана видео в Media 9

кодировщик экрана Windows Media видео 9 оптимизирован для кодирования последовательных снимков экрана от компьютерных мониторов.

## <a name="class-identifier"></a>Идентификатор класса

идентификатор класса (CLSID) для кодировщика экрана Windows Media Video 9 представлен константой **CLSID \_ CMSSCEncMediaObject2**. Экземпляр кодировщика можно создать, вызвав **CoCreateInstance**.

## <a name="input-types"></a>Типы входных данных

Кодировщик экрана версии 9 поддерживает следующие типы входных данных, когда он используется в качестве объекта мультимедиа DirectX (DMO).

-   МЕДИАСУБТИПЕ \_ Rgb24
-   МЕДИАСУБТИПЕ \_ RGB32
-   МЕДИАСУБТИПЕ \_ ARGB32
-   МЕДИАСУБТИПЕ \_ RGB565
-   МЕДИАСУБТИПЕ \_ RGB555
-   МЕДИАСУБТИПЕ \_ RGB8

Кодировщик экрана версии 9 поддерживает следующие типы входных данных, когда он используется в качестве Media Foundation преобразования (MFT).

-   Мфвидеоформат \_ Rgb24
-   Мфвидеоформат \_ RGB32
-   Мфвидеоформат \_ ARGB32
-   Мфвидеоформат \_ RGB565
-   Мфвидеоформат \_ RGB555
-   Мфвидеоформат \_ RGB8

## <a name="output-types"></a>Типы вывода

код из четырех символов (FOURCC) для содержимого в формате Windows Media Video экрана версии 9 — "MSS2".

Кодировщик экрана версии 9 поддерживает следующие типы выходных данных.

-   МЕДИАСУБТИПЕ \_ MSS2

## <a name="encoder-properties"></a>Свойства кодировщика

кодировщик экрана Windows Media видео 9 поддерживает следующие свойства.



<table>
<thead>
<tr class="header">
<th>Свойство</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></td>
<td>Указывает накладные расходы (в байтах на пакет), необходимые для контейнера, используемого для хранения сжатого содержимого.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></td>
<td>Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с средней скоростью (заданным <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).<br/> <dl> Windows XP и более поздних версий.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></td>
<td>Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с пиковой скоростью (заданное <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).<br/> <dl> Windows XP и более поздних версий.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></td>
<td>Указывает, содержит ли закодированный поток видео значение полных буферов со всеми ключевыми кадрами.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></td>
<td>Указывает число кадров видео, закодированных кодеком.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></td>
<td>Указывает количество видеокадров, закодированных кодеком, который фактически содержит данные.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></td>
<td>Это свойство заменяется <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></td>
<td>Указывает сложность алгоритма кодировщика.<br/> <dl> Windows Vista и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></td>
<td>Задает числовое представление компромисса между плавностью движения и качеством изображения в выходных данных кодека.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></td>
<td>Указывает число кадров видео, отброшенных во время кодирования.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></td>
<td>Задает конец прохода кодирования.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></td>
<td>Указывает FOURCC, определяющую кодировщик, который вы хотите использовать.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></td>
<td>Указывает максимальное время в миллисекундах между опорными кадрами в выходных коде.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></td>
<td>Является устаревшей.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></td>
<td>Указывает максимальное число проходов, поддерживаемое кодеком.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></td>
<td>Windows XP и более поздних версий. Read/write.<br/> Указывает число проходов, которые кодек будет использовать для кодирования содержимого.<br/> <dl> Windows XP и более поздних версий.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></td>
<td>Указывает QP. Возможные значения — от 1,0 до 31,0.<br/> <dl> Windows Vista и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></td>
<td>Указывает среднюю скорость потока в битах в секунду, используемую для 2-проходной кодировки с переменной скоростью (VBR).<br/> <dl> Windows XP и более поздних версий.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></td>
<td>Указывает пиковую скорость потока (в битах в секунду), используемую для ограниченного 2-прохода с переменной скоростью (VBR).<br/> <dl> Windows XP и более поздних версий.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></td>
<td>Указывает число кадров видео, переданных кодировщику во время процесса кодирования.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></td>
<td>Указывает, будет ли кодек использовать кодирование с переменной скоростью (VBR).<br/> <dl> Windows XP и более поздних версий.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></td>
<td>Задает реальный уровень качества для кодирования с переменной скоростью (1 проход) с учетом качества (с частотой VBR).<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></td>
<td>Объем содержимого в миллисекундах, который может поместиться в буфер модели.<br/> <dl> Windows XP и более поздних версий<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></td>
<td>Указывает число пропущенных видеокадров, так как они являлись дубликатами предыдущих кадров.<br/> <dl> Windows XP и более поздних версий.<br />
Только для чтения.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Remarks

объект кодировщика экрана предоставляет интерфейс **имедиаобжект** , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс **имфтрансформ** , чтобы объект можно было использовать как преобразование Media Foundation (MFT).

кодировщик экрана ведет себя как DMO или MFT в зависимости от того, какие интерфейсы вы получаете и какая версия Windows выполняется. в следующей таблице показаны условия, при которых кодировщик экрана ведет себя в виде DMO или MFT.



| Операционная система            | Поведение кодировщика                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | кодировщик экрана Windows Media всегда ведет себя как DMO.                                                                                             |
| Windows Vista и Windows 7 | по умолчанию кодировщик экрана Windows мультимедиа ведет себя как DMO. При получении интерфейса **имфтрансформ** на экране кодировщика он ведет себя как MFT. |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows XP, Windows Vista или Windows 7<br/>                                       |
| Заголовок<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsencd.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Реализация кодека](codecimplementation.md)
</dt> <dt>

[экранный кодек Windows Media видео 9](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Windows Экранный декодер видео 9](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 




