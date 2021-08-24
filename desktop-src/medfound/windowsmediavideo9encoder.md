---
description: кодировщик видео Windows Media 9 кодирует видеопотоки.
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: Windows Кодировщик Media Video 9 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852d3d3e7feb06cfbe9e9149fd9fd55d76ecf5abe2fbe0d6eea6ac961a0561ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398244"
---
# <a name="windows-media-video-9-encoder"></a>Windows Кодировщик Media Video 9

кодировщик видео Windows Media 9 кодирует видеопотоки. Кодировщик поддерживает следующие четыре категории закодированных выходных данных.

-   Windows Простой профиль Media Video 9
-   Windows Основной профиль Media Video 9
-   Windows Расширенный профиль Media Video 9
-   Windows Изображение Media Video 9,1

## <a name="class-identifier"></a>Идентификатор класса

идентификатор класса (CLSID) для кодировщика Windows Media Video представлен константой **CLSID \_ CWMV9EncMediaObject**. Вы можете создать экземпляр кодировщика видео, вызвав **CoCreateInstance**.

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

В следующей таблице показаны 4-символьные коды (Фаурккс), соответствующие категориям закодированных выходных данных.



| Категория                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows Простой профиль Media Video 9   | "WMV3"                                   |
| Windows Основной профиль Media Video 9     | "WMV3"                                   |
| Windows Расширенный профиль Media Video 9 | "WVC1"                                   |
| Windows Изображение Media Video 9,1          | "ВМВП" для 9,1, "WVP2" для 9,1 версии 2 |



 

Чтобы различать простой профиль и основной профиль, задайте свойство [**мфпкэй \_ декодеркомплекситирекуестед**](mfpkey-decodercomplexityrequestedproperty.md) .

## <a name="properties"></a>Свойства

кодировщик Windows Media Video 9 поддерживает следующие свойства.



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
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>Указывает среднюю частоту кадров содержимого видео в кадрах в секунду.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с средней скоростью (заданным <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></td>
<td>Указывает Дельта-увеличение между рисунком куантизер фрейма привязки и изображением куантизер в B-кадре.<br/> <dl> Windows XP и более поздних версий.<br />
Основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с пиковой скоростью (заданное <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>Указывает, содержит ли закодированный поток видео значение полных буферов со всеми ключевыми кадрами.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></td>
<td>Задает шаблон кодировки, используемый в начале группы изображений.<br/> <dl> Windows Vista и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>Указывает число кадров видео, закодированных кодеком.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>Указывает количество видеокадров, закодированных кодеком, который фактически содержит данные.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
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
Простой профиль, основной профиль. Расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></td>
<td>указывает тип оптимизации для использования кодека расширенного профиля Windows Media Video 9.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>Задает числовое представление компромисса между плавностью движения и качеством изображения в выходных данных кодека.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></td>
<td>Не используется.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Указывает шаблон соответствия устройства, которому соответствует закодированное содержимое.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>Указывает шаблон соответствия устройств, который вы хотите использовать для кодирования видео.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></td>
<td>Указывает метод, используемый для кодирования сведений о векторе движения.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></td>
<td>Указывает, будет ли кодек использовать фильтр шума при кодировании.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Задает требуемый уровень качества для кодирования с переменной скоростью (1 проход) с учетом качества (с частотой VBR).<br/> <dl> Windows Vista и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>Указывает число кадров видео, отброшенных во время кодирования.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Задает конец прохода кодирования.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></td>
<td>Задает промежуточную высоту кадра для кодированного видео.<br/> <dl> Windows XP и более поздних версий.<br />
Расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></td>
<td>Задает промежуточную ширину кадра для кодированного видео.<br/> <dl> Windows XP и более поздних версий.<br />
Расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></td>
<td>Указывает, должен ли кодек использовать медианную фильтрацию во время кодирования.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>Указывает FOURCC, определяющую кодировщик, который вы хотите использовать.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></td>
<td>Является устаревшей.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></td>
<td>Указывает, разрешено ли кодировщику удалять фреймы.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>Указывает, следует ли использовать чередование выходных данных кодека.<br/> <dl> Windows XP и более поздних версий.<br />
Расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>Указывает максимальное время в миллисекундах между опорными кадрами в выходных коде.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></td>
<td>Не используется.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></td>
<td>Указывает число кадров после текущего кадра, которое будет вычислено кодеком перед кодированием текущего кадра.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></td>
<td>Указывает, должен ли кодек использовать фильтр для деблокировки в процессе кодирования.<br/> <dl> Windows XP и более поздних версий.<br />
Основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></td>
<td>Указывает метод стоимости, используемый кодеком для определения используемого режима макроблокк.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></td>
<td>Указывает метод, используемый для сопоставления движения.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></td>
<td>Указывает типы видеоданных, используемых в операциях поиска движения.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></td>
<td>Указывает диапазон, используемый при поиске движения.<br/> <dl> Windows XP и более поздних версий.<br />
Основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></td>
<td>Указывает, должен ли кодек попытаться обнаружить шумы в кадрах и удалить их.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></td>
<td>Задает число двунаправленных прогнозирующих кадров (B-кадров).<br/> <dl> Windows XP и более поздних версий.<br />
Основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></td>
<td>Указывает количество потоков, которые кодек будет использовать для кодирования.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Указывает максимальное число проходов, поддерживаемое кодеком.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Указывает число проходов, которые кодек будет использовать для кодирования содержимого.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></td>
<td>Указывает, должен ли кодек использовать консервативную оптимизацию искусственного при кодировании.<br/> <dl> Windows XP и более поздних версий.<br />
Основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>Указывает, создает ли кодировщик фиктивные записи кадра в битовом потоке для повторяющихся кадров.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>Указывает QP.<br/> <dl> Windows Vista и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></td>
<td>Указывает степень, до которой кодек должен уменьшить действующий цветовой диапазон видео.<br/> <dl> Windows XP и более поздних версий.<br />
Расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>Указывает среднюю скорость потока в битах в секунду, используемую для 2-проходной кодировки с переменной скоростью (VBR).<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></td>
<td>Указывает, использует ли кодировщик Поиск по подпикселям МВ на основе удаленных рабочих столов. <br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></td>
<td>Для повторной кодировки сегмента указывает размер буфера.<br/> <dl> Windows Vista и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></td>
<td>Для повторной кодировки сегмента указывает длительность сегмента для повторной кодировки.<br/> <dl> Windows Vista и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></td>
<td>Для повторной кодировки сегмента указывает куантизер кадра перед начальным сегментом.<br/> <dl> Windows Vista и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></td>
<td>Для повторной кодировки сегмента задает заполнение начального буфера.<br/> <dl> Windows Vista и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Указывает пиковую скорость потока (в битах в секунду), используемую для ограниченного 2-прохода переменной-разрядной скорости (VBR).<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>Указывает число кадров видео, переданных кодировщику во время процесса кодирования.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Указывает, будет ли кодек использовать кодирование с переменной скоростью (VBR).<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>Задает реальный уровень качества для кодирования с переменной скоростью (1 проход) с учетом качества (с частотой VBR).<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></td>
<td>Указывает, будет ли кодек использовать оптимизацию масштабирования видео.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>Указывает объем содержимого в миллисекундах, который может поместиться в буфер модели.<br/> <dl> Windows XP и более поздних версий.<br />
Расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></td>
<td>Для повторной кодировки сегмента указывает закрытые данные кодека файла, для которого выполняется повторная кодировка.<br/> <dl> Windows Vista и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></td>
<td>Указывает тип логики, которую кодек будет использовать для обнаружения чередующихся исходных видео.<br/> <dl> Windows XP и более поздних версий.<br />
Расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>Указывает число пропущенных видеокадров, так как они являлись дубликатами предыдущих кадров.<br/> <dl> Windows XP и более поздних версий.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
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
| DLL<br/>    | <dl> <dt>Wmvencod.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Реализация кодека](codecimplementation.md)
</dt> </dl>

 

 
