---
description: Графический конвейер Direct3D 10 представляет фундаментальное изменение архитектуры, которое перестраивается с нуля на оборудовании и программном обеспечении для обеспечения нового поколения игр и трехмерных мультимедийных приложений.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: Функции API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab12285509441bb429c78d995e68ed1753ceb5bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262565"
---
# <a name="api-features-direct3d-10"></a><span data-ttu-id="4e567-103">Функции API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="4e567-103">API Features (Direct3D 10)</span></span>

<span data-ttu-id="4e567-104">Графический конвейер Direct3D 10 представляет фундаментальное изменение архитектуры, которое перестраивается с нуля на оборудовании и программном обеспечении для обеспечения нового поколения игр и трехмерных мультимедийных приложений.</span><span class="sxs-lookup"><span data-stu-id="4e567-104">The Direct3D 10 graphics pipeline represents a fundamental architecture change, rebuilt from the ground-up in hardware and software to power the next-generation of games and 3D multimedia applications.</span></span> <span data-ttu-id="4e567-105">В нем используется модель WDDM, которая обеспечивает улучшения производительности и поведения, такие как виртуальная память GPU.</span><span class="sxs-lookup"><span data-stu-id="4e567-105">It uses the Windows Display Driver Model (WDDM), which enables performance and behavioral enhancements such as virtual GPU memory.</span></span>

<span data-ttu-id="4e567-106">Разработчики, знакомые с Direct3D 9, получат ряд функциональных улучшений и улучшений производительности в Direct3D 10, в том числе:</span><span class="sxs-lookup"><span data-stu-id="4e567-106">Developers familiar with Direct3D 9 will discover a series of functional enhancements and performance improvements in Direct3D 10, including:</span></span>

-   <span data-ttu-id="4e567-107">Возможность обработки целых примитивов на новом [этапе создания шейдера Geometry](/previous-versions//bb205146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e567-107">The ability to process entire primitives in the new [geometry-shader stage](/previous-versions//bb205146(v=vs.85)).</span></span>
-   <span data-ttu-id="4e567-108">Возможность вывода данных вершин, созданных конвейером, в память с помощью [этапа потокового вывода](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).</span><span class="sxs-lookup"><span data-stu-id="4e567-108">The ability to output pipeline-generated vertex data to memory using the [stream-output stage](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).</span></span>
-   <span data-ttu-id="4e567-109">Организация состояния конвейера в 5 неизменяемых [объектов состояния](d3d10-graphics-programming-guide-api-features-state-objects.md), что позволяет быстро настроить конвейер.</span><span class="sxs-lookup"><span data-stu-id="4e567-109">Organization of pipeline state into 5 immutable [state objects](d3d10-graphics-programming-guide-api-features-state-objects.md), enabling fast configuration of the pipeline.</span></span>
-   <span data-ttu-id="4e567-110">Организация констант шейдера в [постоянные буферы](d3d10-graphics-programming-guide-resources-types.md), минимизация расходов на пропускную способность для предоставления данных с константами шейдера.</span><span class="sxs-lookup"><span data-stu-id="4e567-110">Organization of shader constants into [constant buffers](d3d10-graphics-programming-guide-resources-types.md), minimizing bandwidth overhead for supplying shader-constant data.</span></span>
-   <span data-ttu-id="4e567-111">Возможность выполнять перестановку и настройку материала для отдельных примитивов с помощью шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="4e567-111">The ability to perform per-primitive material swapping and setup using a geometry shader.</span></span>
-   <span data-ttu-id="4e567-112">Новые [типы ресурсов](d3d10-graphics-programming-guide-resources-types.md) (включая массивы текстур, которые можно индексировать из шейдеров) и форматы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e567-112">New [resource types](d3d10-graphics-programming-guide-resources-types.md) (including texture arrays that can be indexed from shaders) and resource formats.</span></span>
-   <span data-ttu-id="4e567-113">Улучшена обобщение доступа к ресурсам с помощью [представления](d3d10-graphics-programming-guide-resources-access-views.md).</span><span class="sxs-lookup"><span data-stu-id="4e567-113">Increased generalization of resource access using a [view](d3d10-graphics-programming-guide-resources-access-views.md).</span></span>
-   <span data-ttu-id="4e567-114">Устаревшие биты возможностей оборудования (CAP) были удалены в пользу обширного набора гарантированных функциональных возможностей, которые нацелены на оборудование класса Direct3D 10 (минимальное значение).</span><span class="sxs-lookup"><span data-stu-id="4e567-114">Legacy hardware capability bits (caps) have been removed in favor of a rich set of guaranteed functionality, which targets Direct3D 10-class hardware (minimum).</span></span>
-   <span data-ttu-id="4e567-115">[Многоуровневая среда выполнения](d3d10-graphics-programming-guide-api-features-layers.md) . API Direct3D 10 строится с помощью слоев, начиная с базовой функциональности ядра и создавая дополнительные функциональные возможности для разработчиков (Отладка и т. д.) во внешних слоях.</span><span class="sxs-lookup"><span data-stu-id="4e567-115">[Layered Runtime](d3d10-graphics-programming-guide-api-features-layers.md) - The Direct3D 10 API is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality (debug, etc.) in outer layers.</span></span>
-   <span data-ttu-id="4e567-116">Полная интеграция HLSL. все шейдеры Direct3D 10 написаны на HLSL и реализованы в [ядре общего шейдера](../direct3dhlsl/dx-graphics-hlsl-common-core.md).</span><span class="sxs-lookup"><span data-stu-id="4e567-116">Full HLSL integration - All Direct3D 10 shaders are written in HLSL and implemented with the [common-shader core](../direct3dhlsl/dx-graphics-hlsl-common-core.md).</span></span>
-   <span data-ttu-id="4e567-117">Увеличение числа целевых объектов рендеринга, текстур и проб.</span><span class="sxs-lookup"><span data-stu-id="4e567-117">An increase in the number of render targets, textures, and samplers.</span></span> <span data-ttu-id="4e567-118">Кроме того, длина шейдера не ограничена.</span><span class="sxs-lookup"><span data-stu-id="4e567-118">There is also no shader length limit.</span></span>
-   <span data-ttu-id="4e567-119">Операции с целочисленными и побитовыми шейдерами.</span><span class="sxs-lookup"><span data-stu-id="4e567-119">Integer and bitwise shader operations.</span></span>
-   <span data-ttu-id="4e567-120">Реадбакк поверхности или многовыборочный ресурс, когда он больше не привязан в качестве целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="4e567-120">Readback of a depth/stencil surface or a multisampled resource, once it is no longer bound as a render target.</span></span>
-   <span data-ttu-id="4e567-121">Многовыборочная поддержка альфа-покрытия.</span><span class="sxs-lookup"><span data-stu-id="4e567-121">Multisampled alpha-to-coverage support.</span></span>

<span data-ttu-id="4e567-122">Существуют дополнительные различия в поведении, которые разработчики Direct3D 9 также должны учитывать (см. [рекомендации по Direct3D 9 и Direct3D 10](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).</span><span class="sxs-lookup"><span data-stu-id="4e567-122">There are additional behavioral differences that Direct3D 9 developers should also be aware of (see [Direct3D 9 to Direct3D 10 Considerations](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).</span></span>

<span data-ttu-id="4e567-123">Ниже приведен список функций Direct3D 9, которые больше не поддерживаются или были пересмотрены в Direct3D 10 (см. раздел [устаревшие функции](d3d10-graphics-programming-guide-api-features-deprecated.md)).</span><span class="sxs-lookup"><span data-stu-id="4e567-123">Here is a list of Direct3D 9 features that either are no longer supported, or have been revised in Direct3D 10 (see [Deprecated Features](d3d10-graphics-programming-guide-api-features-deprecated.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e567-124">См. также</span><span class="sxs-lookup"><span data-stu-id="4e567-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e567-125">Рекомендации по программированию для Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="4e567-125">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
