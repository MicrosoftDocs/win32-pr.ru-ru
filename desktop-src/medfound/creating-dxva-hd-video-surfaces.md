---
description: Создание видеоподсистем ДКСВА-HD
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: Создание видеоподсистем ДКСВА-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20dea8f34a275aab59b2d57f68ca76d46b1c1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102552"
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



## <a name="related-topics"></a>Связанные разделы

<dl> <dt>

[ДКСВА-HD](dxva-hd.md)
</dt> </dl>

 

 



