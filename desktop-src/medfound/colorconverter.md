---
description: Преобразует видеопоток между цветовыми форматами.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: DSP цветового преобразователя (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a8418d6eeeffcf83a38452b19f18a6baa60bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496833"
---
# <a name="color-converter-dsp"></a>DSP цветового преобразователя

Преобразует видеопоток между цветовыми форматами.

## <a name="clsid"></a>CLSID

\_ККОЛОРКОНВЕРТДМО CLSID

## <a name="interfaces"></a>Интерфейсы

-   [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**имфреалтимеклиент**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [ивмколорконвпропс](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a>Форматы входных данных

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RGB 8
-   айув
-   I420
-   ийув
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   Y41P
-   Y41T
-   Y42T
-   YUY2
-   YV12
-   YVU9
-   ивю

## <a name="output-formats"></a>Форматы выходных данных

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RGB 8
-   айув
-   I420
-   ийув
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   YUY2
-   YV12
-   ивю

## <a name="properties"></a>Свойства

-   [МФПКЭЙ \_ колорконв \_ срклефт](mfpkey-colorconv-srcleft.md)
-   [МФПКЭЙ \_ колорконв \_ срктоп](mfpkey-colorconv-srctop.md)
-   [МФПКЭЙ \_ колорконв \_ дстлефт](mfpkey-colorconv-dstleft.md)
-   [МФПКЭЙ \_ колорконв \_ дсттоп](mfpkey-colorconv-dsttop.md)
-   [\_Ширина мфпкэй колорконв \_](mfpkey-colorconv-width.md)
-   [\_Высота мфпкэй колорконв \_](mfpkey-colorconv-height.md)
-   [\_режим КОЛОРКОНВ \_ мфпкэй](mfpkey-colorconv-mode.md)

## <a name="remarks"></a>Комментарии

DSP цветового преобразователя реализован в виде COM-объекта, который может использоваться в качестве объекта Директксмедиа (DMO) или преобразования Media Foundation (MFT). Объект имеет один идентификатор класса (CLSID), независимо от того, действует ли он как DMO или MFT. Сведения о том, когда DSP выступает в качестве DMO или MFT, см. в разделе [обработчики цифровых сигналов](windowsmediadigitalsignalprocessors.md).

Глобальные уникальные идентификаторы (GUID) для подтипов мультимедиа RGB различаются в зависимости от того, выступает ли DSP в роли DMO или MFT. Идентификаторы GUID для подтипов мультимедиа, отличных от RGB, одинаковы, независимо от того, выступает ли DSP в роли DMO или MFT. Сведения об идентификаторах GUID, представляющих подтипы мультимедиа, см. в разделе [GUID для подтипов видео](video-subtype-guids.md).

По умолчанию этот DSP копирует все исходное изображение в выходной буфер. При необходимости можно указать исходные и конечные прямоугольники. DSP копирует часть исходного изображения, определенное исходным прямоугольником, и записывает его в прямоугольник назначения в выходном буфере. DSP не выполняет масштабирования. исходный и конечный прямоугольники должны иметь одинаковый размер. Исходный и конечный прямоугольники не могут превышать границы видеокадра.

Все свойства, кроме [**\_ \_ режима колорконв мфпкэй**](mfpkey-colorconv-mode.md) , должны быть заданы в группе. Если задать любое из этих свойств, необходимо задать все остальные. В противном случае исходный и конечный прямоугольники могут быть недопустимыми. в этом случае методы [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) и [**Имедиаобжект::P роцессаутпут**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) будут возвращать **E \_ INVALIDARG**.

Преобразователь цветов не поддерживает все сочетания входного и выходного форматов. Как правило, следует задать формат мультимедиа, известный как ввод или вывод, а затем перечислить доступные форматы в противоположном потоке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Colorcnv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обработчики цифровых сигналов](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
