---
title: Создание сплошной кисти цвета
description: Показывает, как создать сплошную цветовую кисть с помощью Direct2D.
ms.assetid: 70700b82-2294-46be-b1c0-fc89def441e2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: bc6fbf5df42386f5e0e5a843a1906d36d4fc8c71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987592"
---
# <a name="how-to-create-a-solid-color-brush"></a><span data-ttu-id="33f15-103">Создание сплошной кисти цвета</span><span class="sxs-lookup"><span data-stu-id="33f15-103">How to Create a Solid Color Brush</span></span>

<span data-ttu-id="33f15-104">Чтобы создать сплошную цветную кисть, используйте метод [**ID2DRenderTarget:: креатесолидколорбруш**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) и укажите цвет, с которым необходимо рисовать заливку.</span><span class="sxs-lookup"><span data-stu-id="33f15-104">To create a solid color brush, use the [**ID2DRenderTarget::CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method and specify the color with which you want to paint.</span></span> <span data-ttu-id="33f15-105">Некоторые перегрузки **креатесолидколорбруш** также позволяют указать непрозрачность кисти.</span><span class="sxs-lookup"><span data-stu-id="33f15-105">Some of the **CreateSolidColorBrush** overloads also enable you to specify the opacity of the brush.</span></span>

<span data-ttu-id="33f15-106">В следующем коде показано, как создать сплошную желтую кисть зеленого цвета для заполнения квадрата и сплошную черную кисть для рисования контура квадрата.</span><span class="sxs-lookup"><span data-stu-id="33f15-106">The following code shows how to create a solid yellow-green brush to fill a square, and a solid black brush to draw the outline of the square.</span></span> <span data-ttu-id="33f15-107">Код создает выходные данные, показанные на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="33f15-107">The code produces the output shown in the following illustration.</span></span>

![Иллюстрация прямоугольника, заполненного сплошным желтым зеленым цветом](images/brushes-ovw-solidcolor.png)

1.  <span data-ttu-id="33f15-109">Объявите два указателя [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) : один для рисования черного, а другой для рисования желтого зеленого цвета.</span><span class="sxs-lookup"><span data-stu-id="33f15-109">Declare two [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) pointers: one for painting black and one for painting yellow green.</span></span>
    ```C++
        ID2D1SolidColorBrush *m_pBlackBrush;
        ID2D1SolidColorBrush *m_pYellowGreenBrush;
    ```

    

2.  <span data-ttu-id="33f15-110">Вызовите метод [**креатесолидколорбруш**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) , чтобы создать кисти:</span><span class="sxs-lookup"><span data-stu-id="33f15-110">Call the [**CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method to create the brushes:</span></span>
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

    

3.  <span data-ttu-id="33f15-111">Вызовите метод [**филлректангле**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) , чтобы закрасить внутреннюю часть прямоугольника с желтой зеленой кистью и методом [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) для рисования контура прямоугольника с помощью черной кисти:</span><span class="sxs-lookup"><span data-stu-id="33f15-111">Call the [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) method to paint the interior of the rectangle with the yellow green brush and the [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method to paint the outline of the rectangle with the black brush:</span></span>
    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="33f15-112">См. также</span><span class="sxs-lookup"><span data-stu-id="33f15-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33f15-113">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="33f15-113">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 