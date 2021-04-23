---
title: Цветовые пространства
description: Человеческий глаз часто может обнаруживать гораздо больше цветов, чем цифровые устройства могут воспроизводить.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Цветовая система Windows (WCS), цветовые пространства
- WCS (цветовая система Windows), цветовые пространства
- Управление цветом изображений, цветовые пространства
- Управление цветом, цветовые пространства
- цвета, цветовые пространства
- цветовые пространства, сведения
- цветовые каналы
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ded035d773956f09949b51cafc6680f66725b82
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "105719781"
---
# <a name="color-spaces"></a><span data-ttu-id="8af4d-110">Цветовые пространства</span><span class="sxs-lookup"><span data-stu-id="8af4d-110">Color Spaces</span></span>

<span data-ttu-id="8af4d-111">Человеческий глаз часто может обнаруживать гораздо больше цветов, чем цифровые устройства могут воспроизводить.</span><span class="sxs-lookup"><span data-stu-id="8af4d-111">The human eye is often able to detect many more colors than digital devices can reproduce.</span></span> <span data-ttu-id="8af4d-112">Например, если взглянуть на пустую, белую страницу бумаги, то глаз, вероятно, обнаружит по крайней мере 100 различных оттенков белого цвета.</span><span class="sxs-lookup"><span data-stu-id="8af4d-112">For instance, if you look at a blank, white page of paper, your eye is probably detecting at least 100 distinct shades of white.</span></span> <span data-ttu-id="8af4d-113">Белая стенка может легко иметь 1500 оттенков белого цвета.</span><span class="sxs-lookup"><span data-stu-id="8af4d-113">A white wall can easily have 1500 shades of white.</span></span>

<span data-ttu-id="8af4d-114">Высококачественные цифровые камеры, сканеры и другие устройства для получения изображений также могут обнаруживать сотни тысяч или даже миллионов цветов.</span><span class="sxs-lookup"><span data-stu-id="8af4d-114">High-quality digital cameras, scanners, and other image acquisition devices can also detect hundreds of thousands or even millions of colors.</span></span> <span data-ttu-id="8af4d-115">Из-за наличия настолько большого количества обнаруживаемых цветов, специалисты по обработке изображений имеют вымышленные модели для указания цветов.</span><span class="sxs-lookup"><span data-stu-id="8af4d-115">Because of the presence of so many detectable colors, imaging professionals have invented models for specifying colors.</span></span> <span data-ttu-id="8af4d-116">Эти модели называются *цветовыми пространствами*.</span><span class="sxs-lookup"><span data-stu-id="8af4d-116">These models are called *color spaces*.</span></span>

<span data-ttu-id="8af4d-117">Причина, по которой эти модели называются цветовыми пространствами, заключается в том, что большинство из них можно сопоставить с двухмерной, трехмерной или 4-D системой координат, как в декартовой системе координат.</span><span class="sxs-lookup"><span data-stu-id="8af4d-117">The reason these models are referred to as color spaces is that most of them can be mapped into a 2-D, 3-D, or 4-D coordinate system similar to a Cartesian coordinate system.</span></span> <span data-ttu-id="8af4d-118">Таким образом, можно сказать, что цвета состоят из координат в плоском, трехмерном или 4-D пространстве.</span><span class="sxs-lookup"><span data-stu-id="8af4d-118">Hence colors can be said to be composed of coordinates in a 2-D, 3-D, or 4-D space.</span></span> <span data-ttu-id="8af4d-119">Цветовые компоненты в пространстве цветов также называются *каналами цвета*.</span><span class="sxs-lookup"><span data-stu-id="8af4d-119">The color components in a color space are also referred to as *color channels*.</span></span>

<span data-ttu-id="8af4d-120">Некоторые цветовые пространства должны быть независимыми от любого устройства, используемого для создания цветовых изображений.</span><span class="sxs-lookup"><span data-stu-id="8af4d-120">Some color spaces are intended to be independent of any device that is used to produce color images.</span></span> <span data-ttu-id="8af4d-121">Некоторые из них зависят от устройства.</span><span class="sxs-lookup"><span data-stu-id="8af4d-121">Some are very device dependent.</span></span> <span data-ttu-id="8af4d-122">Как аппаратные, так и аппаратно-независимые цветовые пространства обсуждаются в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="8af4d-122">Both device-dependent and device-independent color spaces are discussed in the following sections:</span></span>

-   [<span data-ttu-id="8af4d-123">Цветовые пространства RGB</span><span class="sxs-lookup"><span data-stu-id="8af4d-123">RGB Color Spaces</span></span>](rgb-color-spaces.md)
-   [<span data-ttu-id="8af4d-124">Цветовые пространства HSV</span><span class="sxs-lookup"><span data-stu-id="8af4d-124">HSV Color Spaces</span></span>](hsv-color-spaces.md)
-   [<span data-ttu-id="8af4d-125">Цветовые пространства HLS</span><span class="sxs-lookup"><span data-stu-id="8af4d-125">HLS Color Spaces</span></span>](hls-color-spaces.md)
-   [<span data-ttu-id="8af4d-126">Цветовые пространства CMY и CMYK</span><span class="sxs-lookup"><span data-stu-id="8af4d-126">CMY and CMYK Color Spaces</span></span>](cmy-and-cmyk-color-spaces.md)
-   [<span data-ttu-id="8af4d-127">Аппаратно-зависимые цветовые пространства</span><span class="sxs-lookup"><span data-stu-id="8af4d-127">Device-Dependent Color Spaces</span></span>](device-dependent-color-spaces.md)
-   [<span data-ttu-id="8af4d-128">Аппаратно-независимые цветовые пространства</span><span class="sxs-lookup"><span data-stu-id="8af4d-128">Device-Independent Color Spaces</span></span>](device-independent-color-spaces.md)

 

 




