---
description: Видеодекодер MPEG4 часть 2 декодирует видеопотоки, закодированные в соответствии со стандартом MPEG4 (часть 2).
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: Видеодекодер MPEG-4 Part 2 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777e6144684c799eb58f75afd4811ccc8871a46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263510"
---
# <a name="mpeg-4-part-2-video-decoder"></a>Видеодекодер MPEG-4 Part 2

Видеодекодер MPEG4 часть 2 декодирует видеопотоки, закодированные в соответствии со стандартом MPEG4 (часть 2).

Вы можете создать экземпляр видеодекодера версии MPEG4 Part 2, вызвав **CoCreateInstance**. Чтобы создать экземпляр декодера, который ведет себя как объект мультимедиа DirectX (DMO), используйте идентификатор класса **CLSID \_ CMpeg4sDecMediaObject**. Чтобы создать истанце декодера, который ведет себя как Media Foundation преобразование (MFT), используйте идентификатор класса **CLSID \_ CMpeg4sDecMFT**.

## <a name="input-types"></a>Типы входных данных

Видеодекодер MPEG4 Part 2 поддерживает следующие входные типы носителей.

-   МЕДИАСУБТИПЕ \_ M4S2
-   МЕДИАСУБТИПЕ \_ m4s2
-   МЕДИАСУБТИПЕ \_ MP4V
-   МЕДИАСУБТИПЕ \_ MP4V
-   МЕДИАСУБТИПЕ \_ MP4 со множественной (не рекомендуется)
-   МЕДИАСУБТИПЕ \_ MP4 со множественной (не рекомендуется)

## <a name="output-types"></a>Типы вывода

Видеодекодер MPEG4 Part 2 поддерживает следующие выходные подтипы выходных данных, когда он выступает в роли DMO.

-   МЕДИАСУБТИПЕ \_ YV12
-   МЕДИАСУБТИПЕ \_ NV12
-   МЕДИАСУБТИПЕ \_ YUY2
-   МЕДИАСУБТИПЕ \_ UYVY
-   МЕДИАСУБТИПЕ \_ ивю
-   МЕДИАСУБТИПЕ \_ NV11
-   МЕДИАСУБТИПЕ \_ RGB32
-   МЕДИАСУБТИПЕ \_ Rgb24
-   МЕДИАСУБТИПЕ \_ RGB565
-   МЕДИАСУБТИПЕ \_ RGB555
-   МЕДИАСУБТИПЕ \_ RGB8

Видеодекодер MPEG4 Part 2 поддерживает следующие выходные типы выходных данных, когда он выступает в качестве MFT.

-   МЕДИАСУБТИПЕ \_ NV12
-   МЕДИАСУБТИПЕ \_ YV12

## <a name="formats"></a>Форматы

Видеодекодер MPEG4 Part 2 принимает следующие форматы.

-   [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)
-   [**мфвидеоинфо**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (используется только часть VIH2 заголовка).

## <a name="interfaces-for-the-dmo"></a>Интерфейсы DMO

Если вы создаете в виде DMO экземпляр видеодекодера MPEG4 Part 2, декодер предоставляет следующие интерфейсы.

-   [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi)

Вы можете получить интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) , вызвав **CoCreateInstance**, а также получить интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) путем вызова **QueryInterface**.

## <a name="interfaces-for-the-mft"></a>Интерфейсы для MFT

Если вы создаете в MFT экземпляр видеодекодера MPEG2 Part 2, декодер предоставляет следующие интерфейсы.

-   [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**имфкуалитядвисе**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

Можно получить указатель на интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , вызвав **CoCreateInstance**, и можно получить указатель на интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , вызвав [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). Указатель на интерфейс [**имфкуалитядвисе**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) или [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) можно получить, вызвав **QueryInterface** в MFT. Вы можете получить указатель на интерфейс [**имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) или [**имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) , вызвав [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) и передав **\_ \_ \_ службе управления тарифным курсом** Service идентификатор MF.

## <a name="profiles-and-levels"></a>Профили и уровни

Спецификация MPEG4 определяет несколько профилей, каждый из которых задает инструменты, которые кодировщик может использовать для создания закодированного потока. Декодер видео MPEG4 M89 поддерживает два профиля: простой визуальный профиль и расширенный простой профиль. Иными словами, видеодекодер MPEG4 Part 2 может декодировать потоки, закодированные в соответствии с простым визуальным профилем или расширенным простым профилем.

Простой визуальный профиль поддерживает базовую передачу видео с низкой скоростью передачи данных в прогрессивном режиме. Он поддерживает только рисунки внутри и прогноза. Он также поддерживает короткий режим заголовков, который обратно совместим с базовым профилем H. 263. Начиная с Windows 10 видеодекодер MPEG-4 Part 2 также поддерживает H. 263v2 (H. 263 +), который поддерживает пользовательские размеры изображений.

Расширенный простой профиль поддерживает все средства простого визуального профиля, а также поддерживает чередование видео, B-кадров, квартальной компенсации движения в PEL, дополнительные дискретизация таблицы и глобальную компенсацию движения.

Спецификация MPEG4 также определяет несколько уровней, каждый из которых задает ограничения для выходного потока, созданного кодировщиком.

В следующей таблице показаны профили и уровни, а также типичные разрешения, поддерживаемые видеодекодером MPEG4 Part 2.



| Профиль         | Level | Типичное разрешение |
|-----------------|-------|--------------------|
| Простой визуальный элемент   | 0     | 176 x 144          |
| Простой визуальный элемент   | 1     | 176 x 144          |
| Простой визуальный элемент   | 2     | 352 x 288          |
| Простой визуальный элемент   | 3     | 352 x 288          |
| симплевисуал    | 4a    | 640 x 480          |
| Простой визуальный элемент   | 5     | 720 x 576          |
| Расширенный простой | 0     | 176 x 144          |
| Расширенный простой | 1     | 176 x 144          |
| Расширенный простой | 2     | 352 x 288          |
| Расширенный простой | 3     | 352 x 288          |
| Расширенный простой | 3б    | 352 x 288          |
| Расширенный простой | 4     | 352 x 756          |
| Расширенный простой | 5     | 720 x 576          |



 

Дополнительные сведения о профилях и уровнях см. в спецификации MPEG4 Part 2 (ISO/IEC 14496-2): информационные технологии — Программирование звуковых визуальных объектов — часть 2: Visual.

## <a name="decoder-properties"></a>Свойства декодера

Чтобы задать свойства видеодекодера 1 части MPEG4, используйте интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) или интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Видеодекодер MPEG4 Part 2 поддерживает следующие свойства.



<table>
<thead>
<tr class="header">
<th>Свойство</th>
<th>Описание</th>
<th>Значение по умолчанию</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></td>
<td>Задает уровень питания.<br/> <dl> Windows 7.<br />
Доступный только на запись.<br />
</dl></td>
<td>100</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></td>
<td>Задает режим формирования эскиза.<br/> <dl> Windows 7.<br />
Доступный только на запись.<br />
</dl></td>
<td><strong>VARIANT_FALSE</strong></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Комментарии

Глобальные уникальные идентификаторы (GUID) для подтипов мультимедиа RGB различаются в зависимости от того, выступает ли декодер в качестве DMO или MFT. Идентификаторы GUID для подтипов мультимедиа, отличных от RGB, одинаковы, независимо от того, выступает ли декодер в качестве DMO или MFT. Сведения об идентификаторах GUID, представляющих подтипы мультимедиа, см. в разделе [типы носителей](media-types.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP4SDecd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> </dl>

 

 
