---
title: Создание кисти радиального градиента
description: Демонстрирует создание кисти радиального градиента с помощью Direct2D.
ms.assetid: 663743c9-16e9-4e3a-90b2-883ef0b8d5cf
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe3509a80f80132f4a5e5d65f62476be1cac61d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260924"
---
# <a name="how-to-create-a-radial-gradient-brush"></a>Создание кисти радиального градиента

Чтобы создать кисть радиального градиента, используйте метод [**ID2DRenderTarget:: креатерадиалградиентбруш**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) и укажите свойства кисти радиального градиента и коллекцию ограничителей градиента. Некоторые перегрузки позволяют задавать свойства кисти. В следующем коде показано, как создать кисть радиального градиента для заполнения окружности и сплошную черную кисть для рисования контура окружности.

Код создает выходные данные, показанные на следующем рисунке.

![Иллюстрация круга, заполненного радиальной градиентной кистью](images/brushes-ovw-radials.png)

1.  Объявите переменную типа [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).
    ```C++
        ID2D1RadialGradientBrush *m_pRadialGradientBrush;
    ```

    

2.  Создайте массив [**\_ ограничителей D2D1 градиента \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) для постановки в коллекцию ограничителей градиента. Структура **\_ ограничителя \_ градиента D2D1** содержит позиции и цвет ограничителя градиента. Позиция указывает относительное расположение ограничителя градиента в кисти. Значение находится в диапазоне \[ 0,0 f, 1,0 f \] , как показано в следующем коде.

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

    

3.  Используйте метод [**ID2D1RenderTarget:: креатеградиентстопколлектион**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) , чтобы создать коллекцию [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) из ранее объявленного массива структур [**\_ ограничителей D2D1 \_ градиента**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) . Затем используйте [**креатерадиалградиентбруш**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) для создания кисти радиального градиента.

    > [!Note]  
    > Начиная с Windows 8, можно использовать метод [**ID2D1DeviceContext:: креатеградиентстопколлектион**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) для создания коллекции [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) вместо метода [**ID2D1RenderTarget:: креатеградиентстопколлектион**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) . Этот интерфейс добавляет градиенты высокого цвета и интерполяцию градиентов в виде прямых или прмултиплиед цветов. Дополнительные сведения см. на странице **ID2DDeviceContext:: креатеградиентстопколлектион** .

     

    ```C++
    // The center of the gradient is in the center of the box.
    // The gradient origin offset was set to zero(0, 0) or center in this case.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateRadialGradientBrush(
            D2D1::RadialGradientBrushProperties(
                D2D1::Point2F(75, 75),
                D2D1::Point2F(0, 0),
                75,
                75),
            pGradientStops,
            &m_pRadialGradientBrush
            );
    }
    ```

    

    ```C++
    m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
    m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по Direct2D](reference.md)
</dt> </dl>

 

 