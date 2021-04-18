---
title: Цветовые пространства HLS
description: HLSные цветовые пространства также широко используются исполнителями. Его цветовые компоненты — это оттенок, освещение и насыщенность (чрома).
ms.assetid: 8c80d200-c4d0-4233-8f53-a9637dff9ab2
keywords:
- Цветовая система Windows (WCS), HLS Color Spaces
- WCS (цветовая система Windows), цветовые пространства HLS
- Управление цветом изображений, цветовые пространства HLS
- Управление цветом, цветовые пространства HLS
- цвета, HLS цветовые пространства
- цветовые пространства, HLS
- HLS цветовые пространства
- цвет
- насыщенность
- освещенность
- нулевое насыщенность
- насыщенность яркости оттенок (HLS)
- HLS (насыщенность светлого оттенка)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613a62d4a998b51f9bfb22bd7431dd8645a72f3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "105719813"
---
# <a name="hls-color-spaces"></a><span data-ttu-id="d5d3d-117">Цветовые пространства HLS</span><span class="sxs-lookup"><span data-stu-id="d5d3d-117">HLS Color Spaces</span></span>

<span data-ttu-id="d5d3d-118">HLSные [цветовые пространства](c.md) также широко используются исполнителями.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-118">HLS [color spaces](c.md) are also widely used by artists.</span></span> <span data-ttu-id="d5d3d-119">Его цветовые компоненты — это оттенок, освещение и насыщенность (чрома).</span><span class="sxs-lookup"><span data-stu-id="d5d3d-119">Its color components are hue, lightness, and saturation (chroma).</span></span>

<span data-ttu-id="d5d3d-120">Оттенок имеет то же значение, что и модель HSV, за исключением того, что угол оттенка 0 соответствует синему в этой модели.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-120">Hue has the same meaning as the HSV model, except that a hue angle of 0 corresponds to blue in this model.</span></span> <span data-ttu-id="d5d3d-121">Пурпурный — 60, красный — 120.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-121">Magenta is at 60, red is at 120.</span></span> <span data-ttu-id="d5d3d-122">Как и в модели HSV, комплементарные цвета разбиваются на 180.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-122">As with the HSV model, complementary colors are 180 apart.</span></span>

<span data-ttu-id="d5d3d-123">Освещение — это количество черного или белого цвета в цвете.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-123">Lightness is the amount of black or white in a color.</span></span> <span data-ttu-id="d5d3d-124">При увеличении яркости к оттенку добавляется белый цвет.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-124">Increasing lightness adds white to the hue.</span></span> <span data-ttu-id="d5d3d-125">Уменьшение яркости приводит к добавлению черного цвета к оттенку.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-125">Decreasing lightness adds black to the hue.</span></span>

<span data-ttu-id="d5d3d-126">[Насыщенность](s.md) в модели HLS является мерой «чистоты» оттенка.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-126">[Saturation](s.md) in the HLS model is a measure of the "purity" of a hue.</span></span> <span data-ttu-id="d5d3d-127">При уменьшении насыщенности цветовой тон становится серым.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-127">As saturation is decreased, the hue becomes more gray.</span></span> <span data-ttu-id="d5d3d-128">Значение насыщенности, равное нулю, приводит к оттенку серого масштаба.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-128">A saturation value of zero results in a gray-scale value.</span></span>

<span data-ttu-id="d5d3d-129">На следующем рисунке показана линейная прорисовка HLS пространства, которая представляет собой двойное хексконе.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-129">The following figure is a line drawing of HLS space, which is a double hexcone.</span></span> <span data-ttu-id="d5d3d-130">Любой горизонтальный раздел цветового пространства HLS является шестиугольником.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-130">Any horizontal cross section of the HLS color space is a hexagon.</span></span> <span data-ttu-id="d5d3d-131">HLS — это нормализованное цветовое пространство.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-131">HLS is a normalized color space.</span></span> <span data-ttu-id="d5d3d-132">То есть значения яркости и насыщенности находятся в диапазоне от 0,0 до 1,0 включительно.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-132">That is, the lightness and saturation values range from 0.0 to 1.0 inclusive.</span></span> <span data-ttu-id="d5d3d-133">Цветовой тон может иметь значение от 0 до 360 включительно.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-133">Hue varies from 0 to 360 inclusive.</span></span>

![цветовое пространство HLS](images/hlsline.png)

<span data-ttu-id="d5d3d-135">Цветовые пространства HLS могут быть зависимыми от устройства или независимыми от устройства.</span><span class="sxs-lookup"><span data-stu-id="d5d3d-135">HLS color spaces can be device dependent or device independent.</span></span>

 

 




