---
title: Создание сплошной кисти цвета
description: Показывает, как создать сплошную цветовую кисть с помощью Direct2D.
ms.assetid: 70700b82-2294-46be-b1c0-fc89def441e2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 395652a33f8541a825bab9f2ababcceb4b31d7c8d46458a08148e63c85b2afff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259462"
---
# <a name="how-to-create-a-solid-color-brush"></a>Создание сплошной кисти цвета

Чтобы создать сплошную цветную кисть, используйте метод [**ID2DRenderTarget:: креатесолидколорбруш**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) и укажите цвет, с которым необходимо рисовать заливку. Некоторые перегрузки **креатесолидколорбруш** также позволяют указать непрозрачность кисти.

В следующем коде показано, как создать сплошную желтую кисть зеленого цвета для заполнения квадрата и сплошную черную кисть для рисования контура квадрата. Код создает выходные данные, показанные на следующем рисунке.

![Иллюстрация прямоугольника, заполненного сплошным желтым зеленым цветом](images/brushes-ovw-solidcolor.png)

1.  Объявите два указателя [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) : один для рисования черного, а другой для рисования желтого зеленого цвета.
    ```C++
        ID2D1SolidColorBrush *m_pBlackBrush;
        ID2D1SolidColorBrush *m_pYellowGreenBrush;
    ```

    

2.  Вызовите метод [**креатесолидколорбруш**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) , чтобы создать кисти:
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
            &m_pBlackBrush
            );
    }

    // Create a solid color brush with its rgb value 0x9ACD32.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
            &m_pYellowGreenBrush
            );
    }
    ```

    

3.  Вызовите метод [**филлректангле**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) , чтобы закрасить внутреннюю часть прямоугольника с желтой зеленой кистью и методом [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) для рисования контура прямоугольника с помощью черной кисти:
    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по Direct2D](reference.md)
</dt> </dl>

 

 