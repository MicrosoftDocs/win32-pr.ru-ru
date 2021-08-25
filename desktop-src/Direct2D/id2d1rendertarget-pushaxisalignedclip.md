---
title: Методы Пушаксисалигнедклип ID2D1RenderTarget (D2d1 \_ 1. h)
description: Задает прямоугольник, на который обрезаются все последующие операции рисования.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- Методы Пушаксисалигнедклип Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3ce76db0608ccd79ecd8ea1be716f8cbdf4313f95bfdda9cfac7b63474e3f412
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873994"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a>ID2D1RenderTarget: методы:P Ушаксисалигнедклип

Задает прямоугольник, на который обрезаются все последующие операции рисования.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                         | Описание                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**Пушаксисалигнедклип (D2D1 \_ \_ F&, \_ режим сглаживания D2D1 \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))  | Задает прямоугольник, на который обрезаются все последующие операции рисования. <br/> |
| [**Пушаксисалигнедклип (D2D1 \_ Rect \_ F \* , \_ режим сглаживания D2D1 \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) | Задает прямоугольник, на который обрезаются все последующие операции рисования. <br/> |



## <a name="remarks"></a>Remarks

Пара [**пушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) и [**попаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) может возникать или внутри [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) и [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), но не может перекрываться. Например, последовательность **пушаксисалигнедклип**, [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **поплайер**, **Попаксисалигнедклип** является допустимой, но последовательность **пушаксисалигнедклип**, **пушлайер**, **PopAxisAlignedClip**, **PopLayer** недопустима.

Этот метод не возвращает код ошибки в случае сбоя. Чтобы определить, не завершилась ли операция рисования (например, **пушаксисалигнедклип**), проверьте результат, возвращенный методами [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Примеры

Пример см. в разделе [как обрезать с помощью прямоугольника Axis-Aligned Clip](how-to-clip-with-axis-aligned-rects.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D2d1 \_ 1. h (включение D2d1. h)</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
