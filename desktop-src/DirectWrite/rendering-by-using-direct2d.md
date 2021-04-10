---
title: Прорисовка с помощью Direct2D
description: Direct2D предоставляет методы для отрисовки текста с форматированием, описанным только Идвритетекстформат или Идвритетекстлайаут, на поверхность Direct2D.
ms.assetid: 4acd1aee-98bf-4ca3-b4dc-b73c96c6ca63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58af17e15bcb9bd52461a2da3110982fb04e4c0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070545"
---
# <a name="render-using-direct2d"></a>Прорисовка с помощью Direct2D

Direct2D предоставляет методы для отрисовки текста с форматированием, описанным только [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) или [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , на поверхность Direct2D.

## <a name="rendering-text-described-by-idwritetextformat"></a>Отрисовка текста, описываемого Идвритетекстформат

Чтобы отобразить строку с помощью объекта [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) для описания форматирования всей строки, используйте метод [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) , предоставляемый [Direct2D](../direct2d/direct2d-portal.md).

1.  Определите область для макета текста, извлекая размеры области отрисовки и создав [Direct2D](../direct2d/direct2d-portal.md) прямоугольник с теми же размерами.
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  Используйте метод [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) и объект [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) для отрисовки текста на экране. Метод **ID2D1RenderTarget::D равтекст** принимает следующие параметры:
    -   Строка для отображения.
    -   Указатель на интерфейс [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .
    -   Прямоугольник макета [Direct2D](../direct2d/direct2d-portal.md) .
    -   Указатель на интерфейс, предоставляющий [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

## <a name="rendering-a-idwritetext-layout-object"></a>Отрисовка объекта макета Идвритетекст

Чтобы нарисовать текст с параметрами макета текста, заданными в объекте [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , измените код в методе мултиформаттедтекст::D равтекст, чтобы использовать [**Идвритетекстлайаут::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).

1.  Делкаре переменную [**D2D1 \_ \_ 2F**](../direct2d/d2d1-point-2f.md) и установите ее в верхнюю левую точку окна.
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  Выведите текст на экран, вызвав метод [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) целевого объекта прорисовки [Direct2D](../direct2d/direct2d-portal.md) и передав указатель [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

 

 