---
title: Создание кисти линейного градиента
description: Показывает, как создать кисть линейного градиента с помощью Direct2D.
ms.assetid: 3cf5acc6-2f17-49d4-aca5-a84a846d1749
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 3a50a6e3ab421e2275644051ed647d5c4501f8e0
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103891377"
---
# <a name="how-to-create-a-linear-gradient-brush"></a><span data-ttu-id="1e3a6-103">Создание кисти линейного градиента</span><span class="sxs-lookup"><span data-stu-id="1e3a6-103">How to Create a Linear Gradient Brush</span></span>

<span data-ttu-id="1e3a6-104">Чтобы создать кисть линейного градиента, используйте метод [**креателинеарградиентбруш**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) и укажите свойства кисти линейного градиента и коллекцию ограничителей градиента.</span><span class="sxs-lookup"><span data-stu-id="1e3a6-104">To create a linear gradient brush, use the [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method and specify the linear gradient brush properties and the gradient stop collection.</span></span> <span data-ttu-id="1e3a6-105">Некоторые перегрузки позволяют задавать свойства кисти.</span><span class="sxs-lookup"><span data-stu-id="1e3a6-105">Some overloads enable you to specify the brush properties.</span></span> <span data-ttu-id="1e3a6-106">В следующем коде показано, как создать кисть линейного градиента для заливки квадрата и сплошную черную кисть для рисования контура квадрата.</span><span class="sxs-lookup"><span data-stu-id="1e3a6-106">The following code shows how to create a linear gradient brush to fill a square, and a solid black brush to draw the outline of the square.</span></span>

<span data-ttu-id="1e3a6-107">Код создает выходные данные, показанные на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="1e3a6-107">The code produces the output shown in the following illustration.</span></span>

![Иллюстрация квадрата, заполненного линейной градиентной кистью](images/brushes-ovw-lineargradient.png)

1.  <span data-ttu-id="1e3a6-109">Объявите переменную типа [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="1e3a6-109">Declare a variable of type [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span>
    ```C++
        ID2D1LinearGradientBrush *m_pLinearGradientBrush;
    ```

    

2.  <span data-ttu-id="1e3a6-110">Используйте метод [**ID2D1RenderTarget:: креатеградиентстопколлектион**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)) , чтобы создать коллекцию [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) с объявленным массивом структурных точек [**D2D1 \_ градиента \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="1e3a6-110">Use the [**ID2D1RenderTarget::CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)) method to create the [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) collection with a declared array of [**D2D1\_GRADIENT\_STOP**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) structures, as shown in the following code.</span></span>
    > [!Note]  
    > <span data-ttu-id="1e3a6-111">Начиная с Windows 8, вместо этого можно использовать метод [**ID2D1DeviceContext:: креатеградиентстопколлектион**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) для создания коллекции [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) .</span><span class="sxs-lookup"><span data-stu-id="1e3a6-111">Starting with Windows 8, you can use the [**ID2D1DeviceContext::CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) method to create a [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) collection instead.</span></span> <span data-ttu-id="1e3a6-112">Этот интерфейс добавляет градиенты высокого цвета и интерполяцию градиентов в виде прямых или прмултиплиед цветов.</span><span class="sxs-lookup"><span data-stu-id="1e3a6-112">This interface adds high-color gradients and the interpolation of gradients in either straight or prmultiplied colors.</span></span> <span data-ttu-id="1e3a6-113">Дополнительные сведения см. на странице **ID2DDeviceContext:: креатеградиентстопколлектион** .</span><span class="sxs-lookup"><span data-stu-id="1e3a6-113">See the **ID2DDeviceContext::CreateGradientStopCollection** page for more information.</span></span>

     

    ```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
    ```

    

3.  <span data-ttu-id="1e3a6-114">Используйте [**ID2D1RenderTarget:: креателинеарградиентбруш**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) для создания кисти линейного градиента, заливки квадрата кистью и рисования квадрата с черной цветовой кистью.</span><span class="sxs-lookup"><span data-stu-id="1e3a6-114">Use the [**ID2D1RenderTarget::CreateLinearGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) to create a linear gradient brush, fill the square with the brush, and draw the square with the black color brush.</span></span>
    ```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
    ```

    

    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="1e3a6-115">См. также</span><span class="sxs-lookup"><span data-stu-id="1e3a6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e3a6-116">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="1e3a6-116">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 
