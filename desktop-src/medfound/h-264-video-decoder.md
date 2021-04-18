---
description: Видеодекодер Media Foundation H. 264 — это Media Foundation преобразование, которое поддерживает декодирование базовых, основных и высококачественных профилей до уровня 5,1.
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: Декодер видео H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75c4713b1a4e36d1ba085b2239c24ca0f6e4fae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496794"
---
# <a name="h264-video-decoder"></a>Декодер видео H. 264

Видеодекодер Media Foundation H. 264 — это [Media Foundation преобразование](media-foundation-transforms.md) , которое поддерживает декодирование базовых, основных и высококачественных профилей до уровня 5,1.

Декодер видео H. 264 предоставляет следующие интерфейсы.

-   [**Икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) (поддерживается в Windows 8)
-   [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**имфкуалитядвисе**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**имфреалтимеклиент**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Чтобы создать экземпляр декодера, выполните одно из следующих действий.

-   Вызовите функцию [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) или [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .
-   Вызов [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). Идентификатором CLSID для декодера является **CLSID \_ CMSH264DecoderMFT**, объявленный в вмкодекдсп. h.

## <a name="input-types"></a>Типы входных данных

Входной тип должен содержать по крайней мере два следующих атрибута:



| attribute                                                 | Описание                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**\_ \_ основной тип MF \_ MT**](mf-mt-major-type-attribute.md) | **\_Видео мфмедиатипе**                                                                        |
| [**подтип MF \_ MT \_**](mf-mt-subtype-attribute.md)        | [Мфвидеоформат \_ H264 Single bitrate](video-subtype-guids.md) или мфвидеоформат \_ H264 Single bitrate \_ ES |



 

Если тип входных данных содержит только эти два атрибута, декодер будет предлагать тип выхода по умолчанию, который выступает в качестве заполнителя. Когда декодер получает достаточное количество входных образцов для создания выходного фрейма, он сигнализирует об изменении формата, возвращая значение **MF \_ E \_ Преобразование \_ потока \_ преобразования** из [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Дополнительные сведения об обработке изменений формата см. в документации по **ProcessOutput** .

Чтобы избежать первоначального изменения формата, укажите как можно больше информации в типе входных данных, в том числе:



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
<td><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></td>
<td>Частота кадров.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></td>
<td>Размеры рамки.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></td>
<td>Режим чередования.
<blockquote>
[!Note]<br />
В видео H. 264 структура чересстрочную развертки может динамически изменяться, поэтому рекомендуемое значение этого атрибута — <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>. Сведения о развертке в потоке простейшего видео имеют приоритет над типом носителя. Дополнительные сведения см. в статье <a href="video-interlacing.md">чередование видео</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>Пропорция в пикселях.</td>
</tr>
</tbody>
</table>



 

Входной тип должен быть задан перед типом выходных данных. Пока тип входных данных не задан, метод [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) кодировщика возвращает **\_ тип преобразования MF E \_ \_ \_ не \_ задан**.

## <a name="output-types"></a>Типы вывода

Декодер поддерживает следующие выходные типы выходных данных:

-   **Мфвидеоформат \_ I420**
-   **Мфвидеоформат \_ ийув**
-   **Мфвидеоформат \_ NV12**
-   **Мфвидеоформат \_ YUY2**
-   **Мфвидеоформат \_ YV12**

Дополнительные сведения об этих подтипах см. в разделе [GUID подтипа видео](video-subtype-guids.md).

## <a name="transform-attributes"></a>Атрибуты преобразования

Декодер H. 264 реализует метод [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Приложения могут использовать этот метод для получения или установки следующих атрибутов.



| attribute                                                                                       | Описание                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [КОДЕКАПИ \_ авдеквидеоакцелератион \_ H264 Single bitrate](../directshow/avdecvideoacceleration-h264-property.md)            | Включает или отключает аппаратное ускорение.                                                 |
| [КОДЕКАПИ \_ авдеквидеосумбнаилженератионмоде](../directshow/avdecvideothumbnailgenerationmode-property.md) | Включает или отключает режим формирования эскизов.                                             |
| [С \_ \_ поддержкой D3D \_ SA](mf-sa-d3d-aware-attribute.md)                                             | Указывает, что декодер поддерживает ускорение видео DirectX (ДКСВА). Рассматривать как доступное только для чтения. |



 

В Windows 8 декодер H. 264 также поддерживает следующие атрибуты.



| attribute                                                                                                     | Описание                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [КОДЕКАПИ \_ авловлатенцимоде](codecapi-avlowlatencymode.md)                                                   | Включает или отключает режим декодирования с низкой задержкой.                                                              |
| [КОДЕКАПИ \_ авдекнумворкерсреадс](codecapi-avdecnumworkerthreads.md)                                         | Задает число рабочих потоков, используемых декодером.                                                      |
| [КОДЕКАПИ \_ авдеквидеомакскодедвидс](codecapi-avdecvideomaxcodedwidth.md)                                     | Задает максимальную ширину изображения, которую декодер будет принимать в качестве входного типа.                               |
| [КОДЕКАПИ \_ авдеквидеомакскодедхеигхт](codecapi-avdecvideomaxcodedheight.md)                                   | Задает максимальную высоту изображения, которую декодер будет принимать в качестве входного типа.                              |
| [\_ \_ минимальное \_ \_ число образцов выходных данных SA MF \_](mf-sa-minimum-output-sample-count.md)                               | Указывает максимальное число выборок выходных данных.                                                             |
| [\_декодер MFT \_ предоставляют \_ типы выходных данных \_ \_ в \_ собственном \_ порядке](mft-decoder-expose-output-types-in-native-order.md) | Указывает, предоставляет ли декодер выходные типы ИЙУВ/I420 (подходящие для перекодирования) перед другими форматами. |



 

В Windows 8 декодер H. 264 поддерживает интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) . Этот интерфейс предоставляет API алтернативате для установки следующих свойств кодека.

-   [КОДЕКАПИ \_ авдеквидеомакскодедвидс](codecapi-avdecvideomaxcodedwidth.md)
-   [КОДЕКАПИ \_ авдеквидеоакцелератион \_ H264 Single bitrate](../directshow/avdecvideoacceleration-h264-property.md)
-   [КОДЕКАПИ \_ авдеквидеомакскодедхеигхт](codecapi-avdecvideomaxcodedheight.md)
-   [КОДЕКАПИ \_ авдеквидеомакскодедвидс](codecapi-avdecvideomaxcodedwidth.md)
-   [КОДЕКАПИ \_ авдеквидеосумбнаилженератионмоде](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a>Ограничения формата

Декодер поддерживает следующие форматы:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Профили и уровни</td>
<td>Базовый, основной и высокий профили, вплоть до уровня 5,1. (Дополнительные сведения см. в спецификации ITU-T H. 264.)</td>
</tr>
<tr class="even">
<td>Форматы чрома</td>
<td>4:2:0 чрома или монохромный</td>
</tr>
<tr class="odd">
<td>Минимальное разрешение</td>
<td>48 × 48 пикселей</td>
</tr>
<tr class="even">
<td>Максимальное разрешение</td>
<td>4096 × 2304 пикселей<br/> Максимальное гарантированное разрешение для ускорения ДКСВА — 1920 × 1088 пикселей; при более высоком разрешении Декодирование выполняется с помощью ДКСВА, если оно поддерживается базовым оборудованием, в противном случае Декодирование выполняется с помощью программного обеспечения.<br/>
<blockquote>
[!Note]<br />
В Windows 7 максимальное поддерживаемое разрешение составляет 1920 × 1088 пикселей как для программного обеспечения, так и для декодирования ДКСВА.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>дксва</td>
<td>Декодер поддерживает ДКСВА версии 2, но не ДКСВА версии 1. Декодирование ДКСВА поддерживается только для основных параметров, совместимых с базовым, главным и высоким профилями битстреамс. (Базовые битстреамс, совместимые с main, определяются как <strong>profile_idc</strong>= 66 и <strong>constrained_set1_flag</strong>= 1.)</td>
</tr>
</tbody>
</table>



 

Входные данные должны соответствовать приложению B из ISO/IEC 14496-10. Данные должны включать начальные коды. Декодер пропускает байты, пока не найдет допустимый набор параметров последовательности (SPS) и набор параметров изображения (PPS) в байтовом потоке.

Декодер не поддерживает технологию зернистой пленки.

> [!Note]  
> Предыдущая версия документации неправильно объявила, что декодер поддерживается в Windows Server 2008 R2.

 

Если установлено обновление платформы для Windows Vista, видеодекодер H. 264 доступен в Windows Vista, но доступен только в Windows Vista с помощью [средства чтения исходного кода](source-reader.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                  |
| DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Поддержка MPEG-4 в Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Поддерживаемые форматы мультимедиа в Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Типы видеоклипов](video-media-types.md)
</dt> </dl>

 

 
