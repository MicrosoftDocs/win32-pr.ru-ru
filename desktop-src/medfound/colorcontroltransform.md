---
description: Регулирует цветовые характеристики потока видео.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: Преобразование элемента управления цветом DSP (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c51321a8ffd725306f570619b9bcbe70fe7160e784358ce265157145b40347e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606214"
---
# <a name="color-control-transform-dsp"></a>Преобразование элемента управления цветом DSP

Регулирует цветовые характеристики потока видео.

## <a name="clsid"></a>CLSID

\_ККОЛОРКОНТРОЛДМО CLSID

## <a name="interfaces"></a>Интерфейсы

-   **имедиаобжект**
-   **имфтрансформ**
-   **ипропертисторе**

## <a name="formats"></a>Форматы

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   айув
-   UYVY
-   YUY2
-   YV12

## <a name="properties"></a>Свойства

-   [\_цветовая \_ яркость мфпкэй](mfpkey-color-brightness.md)
-   [\_ \_ контрастность цвета мфпкэй](mfpkey-color-contrast.md)
-   [\_цветовой \_ тон мфпкэй](mfpkey-color-hue.md)
-   [МФПКЭЙ \_ \_ насыщенность цвета](mfpkey-color-saturation.md)

## <a name="remarks"></a>Remarks

Этот DSP изменяет содержимое потока видео. Для воспроизведения можно повысить эффективность аналогичных эффектов с помощью интерфейса **имфвидеопроцессор** , который управляет обработкой видео в графической карте.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Обработчики цифровых сигналов](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




