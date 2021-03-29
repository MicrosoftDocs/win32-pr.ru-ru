---
description: Кодировщик видео Media Foundation H. 265 — это Media Foundation преобразование, которое поддерживает кодирование содержимого в формат H. 265/HEVC.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: H. 265/HEVC видео Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015295792a72f3250c47389192586dbc00566858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991380"
---
# <a name="h265--hevc-video-encoder"></a>H. 265/HEVC видео Encoder

Кодировщик видео Media Foundation H. 265 — это [Media Foundation преобразование](media-foundation-transforms.md) , которое поддерживает кодирование содержимого в формат H. 265/HEVC. Кодировщик поддерживает следующие профили:

-   Профиль Main

Кодировщик видео H. 265 предоставляет следующие интерфейсы:

-   [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Типы входных данных

Входной тип носителя должен иметь один из следующих подтипов:

-   **Мфвидеоформат \_ ийув**
-   **Мфвидеоформат \_ NV12**
-   **Мфвидеоформат \_ YUY2**
-   **Мфвидеоформат \_ YV12**

Дополнительные сведения об этих подтипах см. в разделе [GUID подтипа видео](video-subtype-guids.md).

Тип выходных данных должен быть задан перед входным типом. Пока тип выходных данных не задан, метод [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) кодировщика возвращает **\_ \_ \_ \_ не \_ установленный тип преобразования MF E**.

## <a name="output-types"></a>Типы вывода

Кодировщик поддерживает один выходной подтип:

-   **Мфвидеоформат \_ H265**

Задайте следующие атрибуты для выходного типа носителя.



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
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Основной тип. Необходимо <strong>MFMediaType_Video</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Подтип видео. Необходимо <strong>MFVideoFormat_HEVC</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></td>
<td>Средняя скорость кодирования (бит в секунду). Должен быть больше нуля.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></td>
<td>Частота кадров.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></td>
<td>Размер кадра.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></td>
<td>Режим чередования.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></td>
<td>Профиль кодирования H. 265.<br/> Поддерживаются такие значения: <br/>
<ul>
<li><strong>eAVEncH265VProfile_Main_420_8</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></td>
<td>Задает уровень закодированного видео. Дополнительные сведения об ограничениях профиля и уровня см. в приложении A из ITU-T H. 265.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>Необязательный элемент. Задает пропорцию в пикселях. Значение по умолчанию — 1:1.</td>
</tr>
</tbody>
</table>



 

После установки типа выходных данных кодировщик видео обновляет тип, добавляя атрибут [**\_ \_ \_ \_ заголовка последовательностей MF MT MPEG**](mf-mt-mpeg-sequence-header-attribute.md) . Этот атрибут содержит заголовок последовательности.

## <a name="supported-imftransform-methods"></a>Поддерживаемые методы Имфтрансформ

Для кодировщика H. 265/HEVC поддерживаются следующие методы интерфейса [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) :

-   [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [**жетинпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [**жетинпуткурренттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [**жетинпутстатус**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [**жетинпутстреаминфо**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [**жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [**жетаутпуткурренттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [**жетаутпутстатус**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [**жетаутпутстреаминфо**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [**жетстреамкаунт**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [**жетстреамлимитс**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [**процессевент**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [**сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [**сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [**сетаутпутбаундс**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

Все остальные методы [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) будут возвращать ошибку E \_ нотимпл.

## <a name="supported-icodecapi-methods"></a>Поддерживаемые методы Икодекапи

Для кодировщика H. 265/HEVC поддерживаются следующие методы интерфейса [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) :

-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**жетпараметерранже**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**жетпараметервалуес**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

Все остальные методы [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) будут возвращать ошибку E \_ нотимпл.

## <a name="codec-properties"></a>Свойства кодека

Кодировщик H. 265 реализует интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) для установки параметров кодирования. Он поддерживает следующие свойства:

Требования к кодеку для ХКК кодировщика см. в разделе " **сертифицированный аппаратный кодировщик** " ниже.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Свойство</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></td>
<td>Задает режим управления скоростью. Ниже приведены поддерживаемые режимы.<br/>
<ul>
<li><strong>eAVEncCommonRateControlMode_CBR</strong></li>
<li><strong>eAVEncCommonRateControlMode_Quality</strong></li>
</ul>
Если указаны другие режимы, будет использоваться контроль скорости <strong>eAVEncCommonRateControlMode_CBR</strong> .<br/> Это VT_UI4 значение.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></td>
<td>Задает среднюю скорость потока в битах в секунду. <br/> Допустимый диапазон: [1... 2 ³ ² – 1]. <br/> Это VT_UI4 значение.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></td>
<td>Задает размер буфера (в байтах) для кодирования с постоянной скоростью (CBR).<br/> Допустимый диапазон: [1... 2 ³ ² – 1]. <br/> Это VT_UI4 значение.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></td>
<td>Задает максимальную скорость для режимов управления скоростью, которая обеспечивает пиковую скорость. <br/> Допустимый диапазон: [1... 2 ³ ² – 1]. <br/> Это VT_UI4 значение.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></td>
<td>Задает число изображений из одного заголовка GOP к следующему, включая начальную привязку, но не следующую. <br/> Допустимый диапазон: [0... 2 ³ ² – 1]. Если значение равно нулю, кодировщик выбирает размер GOP. Значение по умолчанию равно нулю. <br/> Это VT_UI4 значение.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></td>
<td>Включает или отключает режим низкой задержки. <br/> Это VT_BOOL значение.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></td>
<td>Задает компромисс качества и скорости. Это значение влияет на то, как кодировщик выполняет различные операции кодирования, такие как компенсация движения. На более высоких уровнях сложности кодировщик работает медленнее, но обеспечивает лучшее качество с той же скоростью. <br/> Допустимый диапазон: 0 – 100. На внутреннем уровне это значение сопоставляется с небольшим набором уровней качества и скорости, поддерживаемых кодировщиком.<br/> Это VT_UI4 значение.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></td>
<td>Заставляет кодировщик кодировать следующий кадр как ключевой кадр.<br/> Это VT_UI4 значение.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></td>
<td>Если это свойство задано, кодировщик будет использовать указанный обработчик запросов для кодирования следующего кадра и всех последующих кадров до тех пор, пока не будет указан новый элемент QP. <br/> Допустимый диапазон: 0 – 51, включительно <br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></td>
<td>Это свойство установит ограничение на минимальное количество запросов, которое кодировщик может использовать во время CBR ратеконтрол.<br/> Это VT_UI4 значение.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></td>
<td>Это свойство установит ограничение на максимальное количество запросов на использование, которое кодировщик может использовать во время CBR ратеконтрол.<br/> Это VT_UI4 значение.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></td>
<td>Определяет, является ли содержимое полноэкранным, в отличие от содержимого экрана, которое может иметь меньшее окно видео или вообще не иметь видео.<br/> Это VT_UI4 значение.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></td>
<td>Задает число потоков, используемых для выполнения операции сжатия. Кодировщик будет разделять фрейм на плитки таким, что число потоков равно числу плиток.<br/>
<ul>
<li>Число логических процессоров. Число потоков должно быть меньше или равно числу логических процессоров.</li>
<li>Размер рамки. Размер плитки должен быть больше или равен 265x64 пикселей.</li>
<li>С контролем четности. Число потоков должно быть четным. Если указанное значение нечетное, будет использоваться следующее меньшее четное значение.</li>
</ul>
Это VT_UI4 значение.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="certified-hardware-encoder"></a>Сертифицированный аппаратный кодировщик

Если имеется сертифицированный аппаратный кодировщик, он обычно используется вместо кодировщика системы входящей почты для Media Foundation связанных сценариев. Сертифицированные кодировщики требуются для поддержки определенного набора свойств **икодекапи** и могут дополнительно поддерживать другой набор свойств. Процесс сертификации должен гарантировать, что требуемые свойства должным образом поддерживались, и, если необязательное свойство поддерживается, оно также должно поддерживаться надлежащим образом.

Ниже приведен набор обязательных и необязательных свойств **икодекапи** для кодировщиков, которые проходят сертификацию кодировщика ХКК.

-   [КОДЕКАПИ \_ авенккоммонратеконтролмоде](../directshow/avenccommonratecontrolmode-property.md)
-   [КОДЕКАПИ \_ авенккоммонкуалити](../directshow/avenccommonquality-property.md)
-   [КОДЕКАПИ \_ авенккоммонмеанбитрате](../directshow/avenccommonmeanbitrate-property.md)
-   [КОДЕКАПИ \_ авенккоммонбуфферсизе](../directshow/avenccommonbuffersize-property.md)
-   [КОДЕКАПИ \_ авенкмпвгопсизе](../directshow/avencmpvgopsize-property.md)
-   [КОДЕКАПИ \_ авенквидеоенкодекп](codecapi-avencvideoencodeqp.md)
-   [КОДЕКАПИ \_ авенквидеофорцекэйфраме](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                              |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh265enc.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> </dl>

 

 
