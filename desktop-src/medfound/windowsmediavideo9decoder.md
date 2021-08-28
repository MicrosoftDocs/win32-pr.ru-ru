---
description: декодер media video 9 Windows декодирует видеопотоки, закодированные Windowsным кодировщиком мультимедиа.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Windows Декодер Media Video 9 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df973e78f69e1f1ff0e649b2c4f5637380be9f27
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474310"
---
# <a name="windows-media-video-9-decoder"></a>Windows Декодер Media Video 9

декодер media video 9 Windows декодирует видеопотоки, закодированные [**Windowsным кодировщиком мультимедиа**](windowsmediavideo9encoder.md). Кодировщик и декодер поддерживают следующие четыре категории закодированного видео.

-   Windows Простой профиль Media Video 9
-   Windows Основной профиль Media Video 9
-   Windows Расширенный профиль Media Video 9
-   Windows Изображение Media Video 9,1

## <a name="class-identifier"></a>Идентификатор класса

идентификатор класса (CLSID) для декодера Windows Media Video представлен константой **CLSID \_ квмвдекмедиаобжект**. Вы можете создать экземпляр видеодекодера, вызвав **CoCreateInstance**.

## <a name="interfaces"></a>Интерфейсы

объект видеодекодера предоставляет интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , чтобы объект можно было использовать как преобразование Media Foundation (MFT).

видеодекодер ведет себя как DMO или файл MFT в зависимости от того, какие интерфейсы вы получаете и какая версия Windows выполняется. в следующей таблице показаны условия, при которых декодер видео ведет себя в виде DMO или MFT.



| Операционная система            | Поведение декодера                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | декодер видео Windows Media всегда ведет себя как DMO.                                                                                                                |
| Windows Vista и Windows 7 | по умолчанию видеодекодер Windows мультимедиа ведет себя как DMO. Если вы получаете интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) для видеодекодера, он ведет себя как файл MFT. |



 

начиная с Windows 7, декодер видео с Windows Media реализует интерфейс [**идмокуалитиконтрол**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) .

## <a name="input-formats"></a>Форматы входных данных

в следующей таблице показаны коды из четырех символов (фаурккс), соответствующие категориям закодированных входных данных, которые поддерживаются декодером Windows Media Video.



| Категория                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows Простой профиль Media Video 9   | "WMV3"                                   |
| Windows Основной профиль Media Video 9     | "WMV3"                                   |
| Windows Расширенный профиль Media Video 9 | "WVC1"                                   |
| Windows Изображение Media Video 9,1          | "ВМВП" для 9,1, "WVP2" для 9,1 версии 2 |



 

## <a name="output-formats"></a>Форматы выходных данных

декодер видео Windows media поддерживает следующие подтипы выходных данных, когда он выступает в качестве DMO.

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

декодер видео Windows media поддерживает следующие подтипы выходных данных, когда он выступает в качестве MFT.

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

декодер видео Windows Media поддерживает следующие свойства.




| Свойство | Описание | 
|----------|-------------|
| <a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a> | Указывает, будет ли кодек декодировать чередующиеся видеокадры из сжатого потока в виде прогрессивных кадров.<br /><dl> Windows XP и более поздних версий.<br />Простой профиль, основной профиль, расширенный профиль.<br />Read/write.<br /></dl> | 
| <a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a> | Указывает, будет ли декодер использовать аппаратное ускорение DirectX Video, если оно доступно.<br /><dl> Windows XP и более поздних версий.<br />Простой профиль, основной профиль, расширенный профиль.<br />Доступный только на запись.<br /></dl> | 
| <a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a> | Задает уровень питания для декодера.<br /><dl> Windows 7.<br />Простой профиль, основной профиль, расширенный профиль, изображение.<br />Read/write.<br /></dl> | 
| <a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a> | Указывает, следует ли декодеру использовать интерполяцию кадров.<br /><dl> Windows XP и более поздних версий.<br />Простой профиль, основной профиль, расширенный профиль, изображение.<br />Доступный только на запись.<br /></dl> | 
| <a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a> | Указывает, поддерживает ли декодер интерполяцию кадров.<br /><dl> Windows XP и более поздних версий.<br />Простой профиль, основной профиль, расширенный профиль, изображение<br />Только для чтения.<br /></dl> | 
| <a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a> | Указывает число потоков, которые будет использовать декодер.<br /><dl> Windows Vista и более поздних версий.<br />Простой профиль, основной профиль, расширенный профиль, изображение.<br />Read/write.<br /></dl> | 
| <a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a> | Задает режим обработки, выполняемый для декодера.<br /><dl> Windows Vista и более поздних версий.<br />Простой профиль, основной профиль, расширенный профиль, изображение.<br />Доступный только на запись.<br /></dl> | 
| <strong>g_wszWMVCNeedsDrain</strong> | Указывает, следует ли сливировать декодер.<br /><dl> Windows 8<br />Только для чтения.<br /></dl> это свойство используется средой выполнения Windows Media Format. Тип свойства — <strong>VARIANT_BOOL</strong>. Если значение равно <strong>VARIANT_TRUE</strong>, декодер должен быть остановлен после небесперебойности. Дополнительные сведения о стоке MFT см. в разделе <a href="basic-mft-processing-model.md">Базовая модель обработки MFT</a>.<br /><blockquote>[!Note]<br />Чтобы запросить это свойство, используйте интерфейс <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>ипропертибаг</strong></a> .</blockquote><br /> | 




 

## <a name="remarks"></a>Комментарии

максимальное разрешение, разрешенное декодером Windows Media Video 9, — 4096x4096.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows XP, Windows Vista или Windows 7<br/>                                       |
| Заголовок<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvdecod.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Реализация кодека](codecimplementation.md)
</dt> </dl>

 

 
