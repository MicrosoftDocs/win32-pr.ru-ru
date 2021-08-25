---
description: Создание видеоподсистем ДКСВА-HD
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: Создание видеоподсистем ДКСВА-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40058a02c179a8f9f0690eea9cce777bdd0563d5d27b36ddcb3d34f8fff8a07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829054"
---
# <a name="creating-dxva-hd-video-surfaces"></a>Создание видеоподсистем ДКСВА-HD

Приложение должно создать одну или несколько поверхностей Direct3D для использования во входных кадрах. Они должны быть выделены в пуле памяти, указанном членом **инпутпул** структуры [**дксвахд \_ впдевкапс**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) . Можно использовать следующие типы поверхности:

-   Видеоповерхность, созданная путем вызова [**идксвахд \_ Device:: креатевидеосурфаце**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) и указания **дксвахд \_ Surface \_ \_ \_ input** или типа поверхности **дксвахд \_ тип \_ \_ видео \_ \_ Частная** поверхность. Этот тип поверхности эквивалентен экранной простой поверхности.
-   Поверхность декодера визуализации, созданная путем вызова [**идиректксвидеоакцелератионсервице:: креатесурфаце**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) и указания типа **DXVA2 \_ видеодекодеррендертаржет** . Этот тип поверхности используется для декодирования ДКСВА.
-   Экранная простая поверхность.

В следующем коде показано, как выделить видеоповерхность с помощью [**креатевидеосурфаце**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):


```C++
    // Create the video surface for the primary video stream.
    hr = pDXVAHD->CreateVideoSurface(
        VIDEO_WIDTH,
        VIDEO_HEIGHT,
        VIDEO_FORMAT,
        caps.InputPool,
        0,  // Usage
        DXVAHD_SURFACE_TYPE_VIDEO_INPUT,
        1,      // Number of surfaces to create
        &pSurf, // Array of surface pointers
        NULL
        );
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[ДКСВА-HD](dxva-hd.md)
</dt> </dl>

 

 



