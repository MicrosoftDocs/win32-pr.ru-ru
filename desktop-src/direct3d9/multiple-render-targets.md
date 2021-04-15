---
description: Несколько целевых объектов рендеринга (MRT) — это возможность отображения на нескольких поверхностях (см. IDirect3D9Surface) с помощью одного вызова Draw.
ms.assetid: ae48c5ce-b7f5-4189-8b04-880836be3fe0
title: Несколько целевых объектов рендеринга (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb7aafeedb621e43abb288eb9bbceb17ddb0cc0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495288"
---
# <a name="multiple-render-targets-direct3d-9"></a><span data-ttu-id="2fe8d-103">Несколько целевых объектов рендеринга (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2fe8d-103">Multiple Render Targets (Direct3D 9)</span></span>

<span data-ttu-id="2fe8d-104">Несколько целевых объектов рендеринга (MRT) — это возможность отображения на нескольких поверхностях (см. [**IDirect3D9Surface**](/windows/desktop/api)) с помощью одного вызова Draw.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-104">Multiple Render Targets (MRT) refers to the ability to render to multiple surfaces (see [**IDirect3D9Surface**](/windows/desktop/api)) with a single draw call.</span></span> <span data-ttu-id="2fe8d-105">Эти поверхности можно создавать независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-105">These surfaces can be created independently of each other.</span></span> <span data-ttu-id="2fe8d-106">Целевые объекты отрисовки можно задать с помощью [**IDirect3DDevice9:: сетрендертаржет**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).</span><span class="sxs-lookup"><span data-stu-id="2fe8d-106">Render targets can be set using [**IDirect3DDevice9::SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).</span></span>

<span data-ttu-id="2fe8d-107">Несколько целевых объектов рендеринга имеют следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-107">Multiple render targets have the following restrictions:</span></span>

-   <span data-ttu-id="2fe8d-108">Все используемые поверхности целевого объекта отрисовки должны иметь одинаковую глубину цвета, но могут иметь разные форматы, если \_ не задано ограничение D3DPMISCCAPS мртиндепендентбитдепсс.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-108">All render target surfaces used together must have the same bit depth but can be of different formats, unless the D3DPMISCCAPS\_MRTINDEPENDENTBITDEPTHS cap is set.</span></span>
-   <span data-ttu-id="2fe8d-109">Все поверхности одного целевого объекта прорисовки должны иметь одинаковую ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-109">All surfaces of a multiple render target should have the same width and height.</span></span>
-   <span data-ttu-id="2fe8d-110">Некоторые реализации не могут выполнять операции шейдера после создания нескольких целевых объектов прорисовки, включая смешение, Альфа-тестирование, отсутствие фоггинг, смешение или маскировку, за исключением проверки z и набора элементов.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-110">Some implementations cannot perform post-pixel shader operations on multiple render targets, including: no dithering, alpha test, no fogging, no blending or masking, except the z-test and stencil test.</span></span> <span data-ttu-id="2fe8d-111">Устройства, поддерживающие операции шейдера после пикселей, устанавливают бит крепления D3DPMISCCAPS \_ мртпостпикселшадерблендинг.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-111">Devices that can support post-pixel shader operations set the cap bit to D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING.</span></span>

    <span data-ttu-id="2fe8d-112">Если \_ задано ограничение D3DPMISCCAPS мртпостпикселшадерблендинг, сначала необходимо обратиться к [**IDirect3D9:: чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) с запросом на использование \_ \_ постпикселшадер \_ смешивание результатов для конкретного формата поверхности.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-112">When the D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING cap is set, you must first consult the [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with the USAGE\_QUERY\_POSTPIXELSHADER\_BLENDING result for the specific surface format.</span></span> <span data-ttu-id="2fe8d-113">Если значение равно false, операции смешения построителей шейдеров не будут доступны для этого конкретного формата поверхности.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-113">If false, no post-pixel shader blending operations will be available for that specific surface format.</span></span> <span data-ttu-id="2fe8d-114">Если значение — true, устройство должно применить одно и то же состояние ко всем одновременным целевым объектам рендеринга следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2fe8d-114">If true, the device is expected to apply the same state to all simultaneous render targets as follows:</span></span>

    -   <span data-ttu-id="2fe8d-115">Альфа-смешение: значение цвета в oCi смешивается с целевым объектом i прорисовки.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-115">Alpha blend: The color value in oCi is blended with the ith render target.</span></span>
    -   <span data-ttu-id="2fe8d-116">Альфа-тест: сравнение произойдет с oC0.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-116">Alpha test: Comparison will happen with oC0.</span></span> <span data-ttu-id="2fe8d-117">Если сравнение завершается неудачно, то проверка пикселя завершается для всех целевых объектов прорисовки.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-117">If the comparison fails, the pixel test is terminated for all render targets.</span></span>
    -   <span data-ttu-id="2fe8d-118">Туман: целевой объект прорисовки 0 будет получать фогжед.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-118">Fog: Render target 0 will get fogged.</span></span> <span data-ttu-id="2fe8d-119">Другие целевые объекты отрисовки не определены.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-119">Other render targets are undefined.</span></span> <span data-ttu-id="2fe8d-120">Реализации могут выбрать, чтобы все они применялись к одному и тому же состоянию.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-120">Implementations can choose to fog them all using the same state.</span></span>
    -   <span data-ttu-id="2fe8d-121">Дизеринг: не определено.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-121">Dithering: Undefined.</span></span>

-   <span data-ttu-id="2fe8d-122">Сглаживание не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-122">No antialiasing is supported.</span></span>
-   <span data-ttu-id="2fe8d-123">Некоторые реализации не применяют маску выходной записи (D3DRS \_ колорвритинабле).</span><span class="sxs-lookup"><span data-stu-id="2fe8d-123">Some of the implementations do not apply the output write mask (D3DRS\_COLORWRITEENABLE).</span></span> <span data-ttu-id="2fe8d-124">Те, которые могут иметь независимые маски записи цвета.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-124">Those that can, have independent color write masks.</span></span> <span data-ttu-id="2fe8d-125">Это значение выражается с помощью нового бита возможностей.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-125">This is expressed using a new capability bit.</span></span> <span data-ttu-id="2fe8d-126">Количество доступных независимых цветовых масок записи будет равно максимальному количеству элементов, которое поддерживает устройство.</span><span class="sxs-lookup"><span data-stu-id="2fe8d-126">The number of independent color write masks available will be equal to the maximum number of elements the device is capable of.</span></span>

<span data-ttu-id="2fe8d-127">Новые ограничения оборудования:</span><span class="sxs-lookup"><span data-stu-id="2fe8d-127">New hardware caps:</span></span>


```
D3DCAPS9.NumSimultaneousRTs         
// The value is 1 for all hardware except those that  
//   can support this feature. It is never 0.
D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS - True if the hardware can support it
D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING - True if the hardware can support it
```



## <a name="related-topics"></a><span data-ttu-id="2fe8d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2fe8d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fe8d-129">Конвейер пикселей</span><span class="sxs-lookup"><span data-stu-id="2fe8d-129">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
