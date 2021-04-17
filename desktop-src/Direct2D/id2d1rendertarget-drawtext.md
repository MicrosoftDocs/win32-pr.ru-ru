---
title: ID2D1RenderTarget DrawText методы
description: Рисует указанный текст, используя сведения о форматировании, предоставленные объектом Идвритетекстформат.
ms.assetid: 7cda7854-f9df-48d3-bc62-6aaee769e6f9
keywords:
- Методы DrawText Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5ace5c64dc90f057ff9fdfe5a79d664137c38030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675127"
---
# <a name="id2d1rendertargetdrawtext-methods"></a>ID2D1RenderTarget: методы:D Равтекст

Рисует указанный текст, используя сведения о форматировании, предоставленные объектом [**идвритетекстформат**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                                                                                                                               | Описание                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText (WCHAR \* , идвритетекстформат \* , D2D1 \_ Rect \_ F&, ID2D1Brush \* , D2D1 \_ Draw \_ Text \_ , дврите \_ Text, \_ \_ метод измерения)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))  | Рисует указанный текст, используя сведения о форматировании, предоставленные объектом [**идвритетекстформат**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .<br/>  |
| [**DrawText (WCHAR \* , идвритетекстформат \* , D2D1 \_ Rect \_ F \* , ID2D1Brush \* , D2D1 \_ Draw \_ Text \_ , дврите \_ Text, \_ \_ метод измерения)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) | Рисует указанный текст, используя сведения о форматировании, предоставленные объектом [**идвритетекстформат**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) . <br/> |



## <a name="remarks"></a>Комментарии

Чтобы нарисовать текст с помощью Direct2D, используйте метод [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) для текста, имеющего один формат, или метод [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , если требуется несколько форматов, расширенные функции OpenType или проверка попадания. Эти методы используют API DirectWrite для обеспечения высокого качества отображения текста.

Этот метод не возвращает код ошибки в случае сбоя. Чтобы определить, не завершилась ли операция рисования (например, **DrawText**), проверьте результат, возвращенный методами [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Примеры

Пример см. в разделе [Рисование текста](how-to--draw-text.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**идвритетекстформат**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[Рисование текста](how-to--draw-text.md)
</dt> <dt>

[Общие сведения о форматировании и макете текста](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

