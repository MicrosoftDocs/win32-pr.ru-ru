---
description: Изменяет частоту кадров потока видео.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: Средство преобразования частоты кадров DSP (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca4a728f37caa43ee99a0d293d5113e9c26cfb1dcfe51f399482fb614283737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600494"
---
# <a name="frame-rate-converter-dsp"></a>Средство преобразования частоты кадров DSP

Изменяет частоту кадров потока видео.

## <a name="clsid"></a>CLSID

\_КФРАМЕРАТЕКОНВЕРТДМО CLSID

## <a name="interfaces"></a>Интерфейсы

-   **имедиаобжект**
-   **имфтрансформ**
-   **ипропертисторе**

## <a name="formats"></a>Форматы

-   ARGB 32
-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   айув
-   ийув
-   UYVY
-   Y211
-   Y411
-   Y41P
-   YUY2
-   юив
-   YV12
-   ивю

## <a name="properties"></a>Свойства

-   [МФПКЭЙ \_ , \_ инпутфрамерате](mfpkey-conv-inputframerate.md)
-   [МФПКЭЙ \_ , \_ аутпутфрамерате](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a>Remarks

Этот DSP изменяет частоту кадров путем повторения или удаления кадров.

По умолчанию DSP получает частоту кадров из типов мультимедиа. Кроме того, можно указать частоту кадров, задав свойства МФПКЭЙ, \_ \_ ИНПУТФРАМЕРАТЕ и мфпкэй \_ \_ . Эти значения переопределяют частоту кадров, заданную в типе носителя. Однако при использовании этого DSP в конвейере Media Foundation не следует задавать эти свойства.

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

 

 




