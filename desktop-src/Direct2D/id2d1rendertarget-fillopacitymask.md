---
title: ID2D1RenderTarget ФиллопаЦитимаск методы
description: Применяет маску непрозрачности, описываемую указанным растровым изображением к кисти, и использует эту кисть для рисования области целевого объекта отрисовки.
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- Методы ФиллопаЦитимаск Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 362043696e4cbd21dd64783f210cf2e24066645e7dac5e303a16cd83abb31307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874084"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a>Методы ID2D1RenderTarget:: ФиллопаЦитимаск

Применяет маску непрозрачности, описываемую указанным растровым изображением к кисти, и использует эту кисть для рисования области целевого объекта отрисовки.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                                                                          | Описание                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**ФиллопаЦитимаск (ID2D1Bitmap \* , ID2D1Brush \* , D2D1 \_ непрозрачная \_ маска,&, "f", \_ модуль D2D, f \_ \_ \_ \_&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))       | Применяет маску непрозрачности, описываемую указанным растровым изображением к кисти, и использует эту кисть для рисования области целевого объекта отрисовки. <br/> |
| [**ФиллопаЦитимаск (ID2D1Bitmap \* , ID2D1Brush \* , D2D1 \_ непрозрачность- \_ \_ содержимое, D2D, \_ прямоугольник \_ f \* , D2D \_ \_ -прямоугольник f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f)) | Применяет маску непрозрачности, описываемую указанным растровым изображением к кисти, и использует эту кисть для рисования области целевого объекта отрисовки. <br/> |



## <a name="remarks"></a>Remarks

Для правильной работы этого метода целевой объект прорисовки должен использовать режим сглаживания с [**\_ \_ \_ псевдонимом D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) . Режим сглаживания можно задать, вызвав метод [**ID2D1RenderTarget:: сетантиалиасмоде**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) .

Этот метод не возвращает код ошибки в случае сбоя. Чтобы определить, не завершилась ли операция рисования (например, **филлопаЦитимаск**), проверьте результат, возвращенный методами [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

