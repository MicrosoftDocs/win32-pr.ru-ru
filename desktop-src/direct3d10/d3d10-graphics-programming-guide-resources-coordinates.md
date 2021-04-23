---
description: Системы координат для Direct3D 10 определяются для пикселей и пикселей текстуры.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Системы координат (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba84cd7d807474a1ff41f873d16cbd7eee07224
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807877"
---
# <a name="coordinate-systems-direct3d-10"></a><span data-ttu-id="9f780-103">Системы координат (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="9f780-103">Coordinate Systems (Direct3D 10)</span></span>

<span data-ttu-id="9f780-104">Системы координат для Direct3D 10 определяются для пикселей и пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="9f780-104">Coordinate systems for Direct3D 10 are defined for pixels and texels.</span></span>



|                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f780-105">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="9f780-105">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="9f780-106">Direct3D 10 определяет верхний левый угол верхнего левого пикселя в качестве источника для целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="9f780-106">Direct3D 10 defines the upper-left corner of the upper-left pixel as the origin of a render target.</span></span><br/> <span data-ttu-id="9f780-107">Direct3D 9 определяет центр верхнего левого пикселя в качестве источника для целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="9f780-107">Direct3D 9 defines the center of the upper-left pixel as the origin of a render target.</span></span><br/> |



 

-   [<span data-ttu-id="9f780-108">Пиксельная система координат</span><span class="sxs-lookup"><span data-stu-id="9f780-108">Pixel Coordinate System</span></span>](#pixel-coordinate-system)
    -   [<span data-ttu-id="9f780-109">Пиксельная система координат для Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="9f780-109">Pixel Coordinate System for Direct3D 9</span></span>](#pixel-coordinate-system-for-direct3d-9)
-   [<span data-ttu-id="9f780-110">Система координат шаг текселя</span><span class="sxs-lookup"><span data-stu-id="9f780-110">Texel Coordinate System</span></span>](#texel-coordinate-system)
    -   [<span data-ttu-id="9f780-111">Система координат шаг текселя</span><span class="sxs-lookup"><span data-stu-id="9f780-111">Texel Coordinate System</span></span>](#texel-coordinate-system)
-   [<span data-ttu-id="9f780-112">См. также</span><span class="sxs-lookup"><span data-stu-id="9f780-112">Related topics</span></span>](#related-topics)

## <a name="pixel-coordinate-system"></a><span data-ttu-id="9f780-113">Система координат для пикселей</span><span class="sxs-lookup"><span data-stu-id="9f780-113">Pixel Coordinate System</span></span>

<span data-ttu-id="9f780-114">Пиксельная система координат в Direct3D 10 определяет источник целевого объекта отрисовки в левом верхнем углу.</span><span class="sxs-lookup"><span data-stu-id="9f780-114">The pixel coordinate system in Direct3D 10 defines the origin of a render target at the upper-left corner.</span></span> <span data-ttu-id="9f780-115">как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="9f780-115">as shown in the following diagram.</span></span> <span data-ttu-id="9f780-116">Центры пикселей смещены на (0,5f, 0,5f) от целочисленных расположений.</span><span class="sxs-lookup"><span data-stu-id="9f780-116">Pixel centers are offset by (0.5f,0.5f) from integer locations.</span></span>

![схема системы координат для пикселей в direct3d 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a><span data-ttu-id="9f780-118">Пиксельная система координат для Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="9f780-118">Pixel Coordinate System for Direct3D 9</span></span>

<span data-ttu-id="9f780-119">Для справки ниже приведена система координат пикселей для Direct3D 9, которая определила источник или целевой объект отрисовки в качестве центра верхнего левого пикселя (0,5, 0,5) от левого верхнего угла, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="9f780-119">For reference, here is the pixel coordinate system for Direct3D 9, which defined the origin or a render target as the center of the upper-left pixel, (0.5,0.5) away from the upper left corner, as shown in the following diagram.</span></span> <span data-ttu-id="9f780-120">В Direct3D 9 пиксельные центры находятся в целых местах.</span><span class="sxs-lookup"><span data-stu-id="9f780-120">In Direct3D 9, pixel centers are at integer locations.</span></span>

![Схема пиксельной системы координат в Direct3D 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a><span data-ttu-id="9f780-122">Система координат для текселей</span><span class="sxs-lookup"><span data-stu-id="9f780-122">Texel Coordinate System</span></span>

<span data-ttu-id="9f780-123">Начало системы координат для текселей расположено в верхнем левом углу текстуры, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="9f780-123">The texel coordinate system has its origin at the top-left corner of the texture, as shown in the following diagram.</span></span> <span data-ttu-id="9f780-124">Это делает отрисовку текстурно-ориентированного изображения тривиальными (в Direct3D 10), так как система координат в пикселях согласована с системой координат шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="9f780-124">This makes rendering screen-aligned textures trivial (in Direct3D 10), as the pixel coordinate system is aligned with the texel coordinate system.</span></span>

![схема системы координат для текселей](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a><span data-ttu-id="9f780-126">Система координат для текселей</span><span class="sxs-lookup"><span data-stu-id="9f780-126">Texel Coordinate System</span></span>

<span data-ttu-id="9f780-127">Координаты текстуры представлены в виде нормализованного или скалярного числа; каждая координата текстуры сопоставляется определенному текселю следующим образом.</span><span class="sxs-lookup"><span data-stu-id="9f780-127">Texture coordinates are represented with either a normalized or a scaled number; each texture coordinate is mapped to a specific texel as follows:</span></span>

<span data-ttu-id="9f780-128">Для нормализованной координаты:</span><span class="sxs-lookup"><span data-stu-id="9f780-128">For a normalized coordinate:</span></span>

-   <span data-ttu-id="9f780-129">Выборка точек: шаг текселя \# = floor ( \* Ширина в U)</span><span class="sxs-lookup"><span data-stu-id="9f780-129">Point sampling: Texel \# = floor(U \* Width)</span></span>
-   <span data-ttu-id="9f780-130">Линейная выборка: левый шаг текселя \# = floor ( \* Ширина в U), правый шаг текселя \# = Left шаг текселя \# + 1</span><span class="sxs-lookup"><span data-stu-id="9f780-130">Linear sampling: Left Texel \# = floor(U \* Width), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="9f780-131">Для скалярной координаты:</span><span class="sxs-lookup"><span data-stu-id="9f780-131">For a scaled coordinate:</span></span>

-   <span data-ttu-id="9f780-132">Выборка точек: шаг текселя \# = floor (U)</span><span class="sxs-lookup"><span data-stu-id="9f780-132">Point sampling: Texel \# = floor(U)</span></span>
-   <span data-ttu-id="9f780-133">Линейная выборка: Left шаг текселя \# = этаж (U-0,5), Right шаг текселя \# = Left шаг текселя \# + 1</span><span class="sxs-lookup"><span data-stu-id="9f780-133">Linear sampling: Left Texel \# = floor(U - 0.5), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="9f780-134">Где ширина — это ширина текстуры (в текселях).</span><span class="sxs-lookup"><span data-stu-id="9f780-134">Where the width, is the width of the texture (in texels).</span></span>

<span data-ttu-id="9f780-135">Упаковка адреса текстуры происходит после расчета расположения текселя.</span><span class="sxs-lookup"><span data-stu-id="9f780-135">Texture address wrapping occurs after the texel location is computed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f780-136">См. также</span><span class="sxs-lookup"><span data-stu-id="9f780-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f780-137">Ресурсы (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="9f780-137">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




