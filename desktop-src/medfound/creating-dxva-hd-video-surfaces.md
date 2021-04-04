---
description: .
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: Создание видеоподсистем ДКСВА-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459504a312ec0d59cf3642f528f433ffce8ba094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896586"
---
# <a name="creating-dxva-hd-video-surfaces"></a><span data-ttu-id="7f9c8-103">Создание видеоподсистем ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="7f9c8-103">Creating DXVA-HD Video Surfaces</span></span>

<span data-ttu-id="7f9c8-104">Приложение должно создать одну или несколько поверхностей Direct3D для использования во входных кадрах.</span><span class="sxs-lookup"><span data-stu-id="7f9c8-104">The application must create one or more Direct3D surfaces to use for the input frames.</span></span> <span data-ttu-id="7f9c8-105">Они должны быть выделены в пуле памяти, указанном членом **инпутпул** структуры [**дксвахд \_ впдевкапс**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="7f9c8-105">These must be allocated in the memory pool specified by the **InputPool** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="7f9c8-106">Можно использовать следующие типы поверхности:</span><span class="sxs-lookup"><span data-stu-id="7f9c8-106">The following surface types can be used:</span></span>

-   <span data-ttu-id="7f9c8-107">Видеоповерхность, созданная путем вызова [**идксвахд \_ Device:: креатевидеосурфаце**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) и указания **дксвахд \_ Surface \_ \_ \_ input** или типа поверхности **дксвахд \_ тип \_ \_ видео \_ \_ Частная** поверхность.</span><span class="sxs-lookup"><span data-stu-id="7f9c8-107">A video surface created by calling [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) and specifying the **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT** or **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT\_PRIVATE** surface type.</span></span> <span data-ttu-id="7f9c8-108">Этот тип поверхности эквивалентен экранной простой поверхности.</span><span class="sxs-lookup"><span data-stu-id="7f9c8-108">This surface type is equivalent to an off-screen plain surface.</span></span>
-   <span data-ttu-id="7f9c8-109">Поверхность декодера визуализации, созданная путем вызова [**идиректксвидеоакцелератионсервице:: креатесурфаце**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) и указания типа **DXVA2 \_ видеодекодеррендертаржет** .</span><span class="sxs-lookup"><span data-stu-id="7f9c8-109">A decoder render-target surface, created by calling [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) and specifying the **DXVA2\_VideoDecoderRenderTarget** surface type.</span></span> <span data-ttu-id="7f9c8-110">Этот тип поверхности используется для декодирования ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="7f9c8-110">This surface type is used for DXVA decoding.</span></span>
-   <span data-ttu-id="7f9c8-111">Экранная простая поверхность.</span><span class="sxs-lookup"><span data-stu-id="7f9c8-111">An off-screen plain surface.</span></span>

<span data-ttu-id="7f9c8-112">В следующем коде показано, как выделить видеоповерхность с помощью [**креатевидеосурфаце**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span><span class="sxs-lookup"><span data-stu-id="7f9c8-112">The following code shows how to allocate a video surface, using [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7f9c8-113">См. также</span><span class="sxs-lookup"><span data-stu-id="7f9c8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f9c8-114">ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="7f9c8-114">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



