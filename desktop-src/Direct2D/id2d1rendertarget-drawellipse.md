---
title: Методы DrawEllipse ID2D1RenderTarget (D2d1. h)
description: Рисует контур эллипса с заданными размерами и обводкой.
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
keywords:
- Методы DrawEllipse Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 2f43ce72bcce5be550eec109551efd10c46262bc2bd753e67fe53061aa27bb8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118002845"
---
# <a name="id2d1rendertargetdrawellipse-methods"></a>ID2D1RenderTarget: методы:D Равеллипсе

Рисует контур эллипса с заданными размерами и обводкой.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                 | Описание                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**DrawEllipse (D2D1 \_ ellipse&, ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))  | Рисует контур указанного эллипса с помощью указанного стиля Stroke. <br/> |
| [**DrawEllipse (D2D1 \_ Ellipse \* , ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) | Рисует контур указанного эллипса с помощью указанного стиля Stroke. <br/> |



## <a name="remarks"></a>Remarks

Метод **DrawEllipse** не возвращает код ошибки в случае сбоя. Чтобы определить, не завершилась ли операция рисования (например, **DrawEllipse**), проверьте результат, возвращенный методами [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Примеры

Пример см. в разделе [Рисование и заполнение базовой фигуры](how-to-draw-an-ellipse.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**филлеллипсе**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))
</dt> </dl>

�

�
