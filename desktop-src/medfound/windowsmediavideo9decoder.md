---
description: Декодер видео Windows Media 9 декодирует видеопотоки, закодированные кодировщиком Windows Media Video.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Декодер Windows Media Video 9 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d89e05f82ce503016a10d5591a23bc673d0db5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718023"
---
# <a name="windows-media-video-9-decoder"></a>Декодер Windows Media Video 9

Декодер видео Windows Media 9 декодирует видеопотоки, закодированные [**кодировщиком Windows Media Video**](windowsmediavideo9encoder.md). Кодировщик и декодер поддерживают следующие четыре категории закодированного видео.

-   Простой профиль Windows Media Video 9
-   Основной профиль Windows Media Video 9
-   Расширенный профиль Windows Media Video 9
-   Изображение Windows Media Video 9,1

## <a name="class-identifier"></a>Идентификатор класса

Идентификатор класса (CLSID) для видеодекодера Windows Media представлен константой **CLSID \_ квмвдекмедиаобжект**. Вы можете создать экземпляр видеодекодера, вызвав **CoCreateInstance**.

## <a name="interfaces"></a>Интерфейсы

Объект видеодекодера предоставляет интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , чтобы объект можно было использовать в качестве Media Foundation преобразования (MFT).

Видеодекодер ведет себя как DMO или файл MFT в зависимости от того, какие интерфейсы вы получаете и какая версия Windows выполняется. В следующей таблице показаны условия, при которых декодер видео ведет себя как DMO или MFT.



| Операционная система            | Поведение декодера                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Видеодекодер Windows Media всегда ведет себя как DMO.                                                                                                                |
| Windows Vista и Windows 7 | По умолчанию видеодекодер Windows Media ведет себя как DMO. Если вы получаете интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) для видеодекодера, он ведет себя как файл MFT. |



 

Начиная с Windows 7, декодер видео Windows Media реализует интерфейс [**идмокуалитиконтрол**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) .

## <a name="input-formats"></a>Форматы входных данных

В следующей таблице показаны 4-символьные коды (Фаурккс), соответствующие категориям закодированных входных данных, поддерживаемых декодером Windows Media Video.



| Категория                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Простой профиль Windows Media Video 9   | "WMV3"                                   |
| Основной профиль Windows Media Video 9     | "WMV3"                                   |
| Расширенный профиль Windows Media Video 9 | "WVC1"                                   |
| Изображение Windows Media Video 9,1          | "ВМВП" для 9,1, "WVP2" для 9,1 версии 2 |



 

## <a name="output-formats"></a>Форматы выходных данных

Декодер видео Windows Media поддерживает следующие подтипы выходных данных, когда он выступает в роли DMO.

-   МЕДИАСУБТИПЕ \_ NV12
-   МЕДИАСУБТИПЕ \_ YV12
-   МЕДИАСУБТИПЕ \_ YUY2
-   МЕДИАСУБТИПЕ \_ UYVY
-   МЕДИАСУБТИПЕ \_ ивю
-   МЕДИАСУБТИПЕ \_ NV11
-   МЕДИАСУБТИПЕ \_ RGB32
-   МЕДИАСУБТИПЕ \_ Rgb24
-   МЕДИАСУБТИПЕ \_ RGB565
-   МЕДИАСУБТИПЕ \_ RGB555
-   МЕДИАСУБТИПЕ \_ RGB8

Декодер видео Windows Media поддерживает следующие подтипы выходных данных, когда он выступает в качестве MFT.

-   Мфвидеоформат \_ NV12
-   Мфвидеоформат \_ YV12
-   Мфвидеоформат \_ YUY2
-   Мфвидеоформат \_ UYVY
-   Мфвидеоформат \_ ивю
-   Мфвидеоформат \_ NV11
-   Мфвидеоформат \_ RGB32
-   Мфвидеоформат \_ Rgb24
-   Мфвидеоформат \_ RGB565
-   Мфвидеоформат \_ RGB555
-   Мфвидеоформат \_ RGB8

## <a name="properties"></a>Свойства

Декодер видео Windows Media поддерживает следующие свойства.



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
<td><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></td>
<td>Указывает, будет ли кодек декодировать чередующиеся видеокадры из сжатого потока в виде прогрессивных кадров.<br/> <dl> Windows XP и более поздние версии.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></td>
<td>Указывает, будет ли декодер использовать аппаратное ускорение DirectX Video, если оно доступно.<br/> <dl> Windows XP и более поздние версии.<br />
Простой профиль, основной профиль, расширенный профиль.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></td>
<td>Задает уровень питания для декодера.<br/> <dl> Windows 7.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></td>
<td>Указывает, следует ли декодеру использовать интерполяцию кадров.<br/> <dl> Windows XP и более поздние версии.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></td>
<td>Указывает, поддерживает ли декодер интерполяцию кадров.<br/> <dl> Windows XP и более поздние версии.<br />
Простой профиль, основной профиль, расширенный профиль, изображение<br />
Только для чтения.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></td>
<td>Указывает число потоков, которые будет использовать декодер.<br/> <dl> Windows Vista и более поздние версии.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></td>
<td>Задает режим обработки, выполняемый для декодера.<br/> <dl> Windows Vista и более поздние версии.<br />
Простой профиль, основной профиль, расширенный профиль, изображение.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>g_wszWMVCNeedsDrain</strong></td>
<td>Указывает, следует ли сливировать декодер.<br/> <dl> Windows 8<br />
Только для чтения.<br />
</dl> Это свойство используется средой выполнения формата Windows Media. Тип свойства — <strong>VARIANT_BOOL</strong>. Если значение равно <strong>VARIANT_TRUE</strong>, декодер должен быть остановлен после небесперебойности. Дополнительные сведения о стоке MFT см. в разделе <a href="basic-mft-processing-model.md">Базовая модель обработки MFT</a>.<br/>
<blockquote>
[!Note]<br />
Чтобы запросить это свойство, используйте интерфейс <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>ипропертибаг</strong></a> .
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Комментарии

Максимально допустимое разрешение декодера Windows Media Video 9 — 4096x4096.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows XP, Windows Vista или Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvdecod.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Реализация кодека](codecimplementation.md)
</dt> </dl>

 

 
