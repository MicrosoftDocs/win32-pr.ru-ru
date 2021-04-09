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
# <a name="how-to-create-a-linear-gradient-brush"></a>Создание кисти линейного градиента

Чтобы создать кисть линейного градиента, используйте метод [**креателинеарградиентбруш**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) и укажите свойства кисти линейного градиента и коллекцию ограничителей градиента. Некоторые перегрузки позволяют задавать свойства кисти. В следующем коде показано, как создать кисть линейного градиента для заливки квадрата и сплошную черную кисть для рисования контура квадрата.

Код создает выходные данные, показанные на следующем рисунке.

![Иллюстрация квадрата, заполненного линейной градиентной кистью](images/brushes-ovw-lineargradient.png)

1.  Объявите переменную типа [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).
    ```C++
        ID2D1LinearGradientBrush *m_pLinearGradientBrush;
    ```

    

2.  Используйте метод [**ID2D1RenderTarget:: креатеградиентстопколлектион**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)) , чтобы создать коллекцию [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) с объявленным массивом структурных точек [**D2D1 \_ градиента \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) , как показано в следующем коде.
    > [!Note]  
    > Начиная с Windows 8, вместо этого можно использовать метод [**ID2D1DeviceContext:: креатеградиентстопколлектион**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) для создания коллекции [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) . Этот интерфейс добавляет градиенты высокого цвета и интерполяцию градиентов в виде прямых или прмултиплиед цветов. Дополнительные сведения см. на странице **ID2DDeviceContext:: креатеградиентстопколлектион** .

     

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

    

3.  Используйте [**ID2D1RenderTarget:: креателинеарградиентбруш**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) для создания кисти линейного градиента, заливки квадрата кистью и рисования квадрата с черной цветовой кистью.
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

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по Direct2D](reference.md)
</dt> </dl>

 

 
