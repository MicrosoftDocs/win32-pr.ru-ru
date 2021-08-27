---
description: В этом разделе описывается использование различных типов кистей в объектной модели XPS.
ms.assetid: 392ca1d5-283e-4eed-ae21-6477c469014d
title: OM-кисти XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbca4174c406e0d2fda63d932ee85f2f3c3123b7255b43f77a2365bf0f05e2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971133"
---
# <a name="xps-om-brushes"></a>OM-кисти XPS

В этом разделе описывается использование различных типов кистей в объектной модели XPS.

Кисти в модели XPS основаны на [**интерфейсе икспсомбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) и включают следующее:

<dl> Мозаичные кисти

-   [**Интерфейс Икспсомтилебруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
-   [**Интерфейс Икспсомсолидколорбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
-   [**Интерфейс Икспсомвисуалбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
-   [**Интерфейс Икспсомимажебруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)

  
Градиентные кисти

-   [**Интерфейс Икспсомградиентбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
-   [**Интерфейс Икспсомлинеарградиентбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
-   [**Интерфейс Икспсомрадиалградиентбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)

  
</dl>

## <a name="code-examples"></a>Примеры кода

### <a name="create-a-solid-color-brush"></a>Создание кисти с сплошным цветом

В следующем примере кода создается кисть с сплошным цветом на основе значения цвета, определенного в коде.


```C++
    HRESULT                hr = S_OK;

    XPS_COLOR              xpsColor;
    IXpsOMSolidColorBrush  *brush;

    // creates a solid red brush
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0xFF;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    hr = xpsFactory->CreateSolidColorBrush(
       &xpsColor, 
       NULL, 
       reinterpret_cast<IXpsOMSolidColorBrush**>(&brush));
    
    // use brush

    // when finished with brush, release pointer
    brush->Release();
```



### <a name="create-a-visual-brush"></a>Создание визуальной кисти

В следующем примере кода создается кисть на основе визуального объекта.


```C++
    HRESULT                       hr = S_OK;
    IXpsOMVisualBrush             *brush;

    XPS_RECT viewBoxRect = {0,0,0,0};
    XPS_RECT viewPortRect = {0,0,0,0};

    // set viewBoxRect to define the portion of the visual to use
    // as the brush.
    //
    // set viewPortRect to define the location and size of the 
    // the brush in the destination 
    //
    // create the brush
    hr = xpsFactory->CreateVisualBrush (
        &viewBoxRect,
        &viewPortRect,
        reinterpret_cast<IXpsOMVisualBrush**>(&brush));

    // assign the visual object
    //   brushVisual points to a visual
    //   that is defined outside of this example

    hr = brush->SetVisualLocal (brushVisual);
    
    // use brush
    
    // when finished with brush, release pointer
    brush->Release();
    
```



### <a name="create-an-image-brush"></a>Создание кисти изображения

См. пример кода на [месте изображений в OM-образной модели XPS](place-images-in-an-xps-om.md).

### <a name="create-a-linear-gradient-brush"></a>Создание кисти линейного градиента

В следующем примере кода создается кисть линейного градиента. Градиент имеет две остановки градиента.


```C++
    HRESULT                       hr = S_OK;
    XPS_COLOR                     xpsColorStop;
    IXpsOMGradientStop            *xpsGradientStop1, *xpsGradientStop2;
    IXpsOMLinearGradientBrush     *brush;
    XPS_POINT                     startPoint, endPoint;

    // define the start color
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xE4;
    xpsColorStop.value.sRGB.green = 0x3B;
    xpsColorStop.value.sRGB.blue  = 0x2F;
    
    // create a gradient stop by setting the color and location 
    // for the beginning of the gradient
    hr = xpsFactory->CreateGradientStop(
        &xpsColorStop, 
        NULL, 
        0.0f,
        &xpsGradientStop1);
    startPoint.x = 375.75f;
    startPoint.y = 18.0f;

    // define the end color
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xEF;
    xpsColorStop.value.sRGB.green = 0x79;
    xpsColorStop.value.sRGB.blue  = 0x2F;

    // create a gradient stop by setting the color and  location
    //  for the end of the gradient
    hr = xpsFactory->CreateGradientStop(
        &xpsColorStop,
        NULL, 
        1.0f, 
        &xpsGradientStop2);
    endPoint.x   = 375.75f;
    endPoint.y   = 134.6f;

    // create the brush
    hr = xpsFactory->CreateLinearGradientBrush(
        xpsGradientStop1, 
        xpsGradientStop2, 
        &startPoint, 
        &endPoint, 
        &brush);
    // release gradient stops after creating brush
    xpsGradientStop1->Release();
    xpsGradientStop2->Release();

    // when finished with brush, release pointer to brush
    brush->Release();
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Икспсомградиентбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
</dt> <dt>

[**Интерфейс Икспсомимажебруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)
</dt> <dt>

[**Интерфейс Икспсомлинеарградиентбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
</dt> <dt>

[**Интерфейс Икспсомрадиалградиентбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)
</dt> <dt>

[**Интерфейс Икспсомсолидколорбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[**Интерфейс Икспсомтилебруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
</dt> <dt>

[**Интерфейс Икспсомвисуалбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
</dt> <dt>

[**\_Цвет XPS**](xps-color.md)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



