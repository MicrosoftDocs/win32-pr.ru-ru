---
title: Размещение на плитках вложенных ресурсов Texture2D и Texture2DArray
description: В таблицах ниже показано, как размещаются на плитках вложенные ресурсы Texture2D и Texture2DArray.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a7ded22fcb7e7e476a701c7db3063dfae33fda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413289"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a><span data-ttu-id="e49d6-103">Размещение на плитках вложенных ресурсов Texture2D и Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e49d6-103">Texture2D and Texture2DArray subresource tiling</span></span>

<span data-ttu-id="e49d6-104">В этих таблицах показано, как [**подTexture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) и перемещаются подресурсы [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) .</span><span class="sxs-lookup"><span data-stu-id="e49d6-104">These tables show how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources are tiled.</span></span> <span data-ttu-id="e49d6-105">Значения в этих таблицах не учитывают упаковку хвостовых MIP-карт.</span><span class="sxs-lookup"><span data-stu-id="e49d6-105">The values in these tables don't count tail mip packing.</span></span>

<span data-ttu-id="e49d6-106">В этой таблице показано, как размещаются на плитках вложенные ресурсы [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) и [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) с множественной дискретизацией и одной выборкой.</span><span class="sxs-lookup"><span data-stu-id="e49d6-106">This table shows how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources with multisample counts of 1 are tiled.</span></span>



| <span data-ttu-id="e49d6-107">Бит/пкс (1 семпл/пкс)</span><span class="sxs-lookup"><span data-stu-id="e49d6-107">Bits/Pixel (1 sample/pixel)</span></span> | <span data-ttu-id="e49d6-108">Размеры плиток (пиксели, ШxВ)</span><span class="sxs-lookup"><span data-stu-id="e49d6-108">Tile Dimensions (Pixels, WxH)</span></span> |
|-----------------------------|-------------------------------|
| <span data-ttu-id="e49d6-109">8</span><span class="sxs-lookup"><span data-stu-id="e49d6-109">8</span></span>                           | <span data-ttu-id="e49d6-110">256x256</span><span class="sxs-lookup"><span data-stu-id="e49d6-110">256x256</span></span>                       |
| <span data-ttu-id="e49d6-111">16</span><span class="sxs-lookup"><span data-stu-id="e49d6-111">16</span></span>                          | <span data-ttu-id="e49d6-112">256x128</span><span class="sxs-lookup"><span data-stu-id="e49d6-112">256x128</span></span>                       |
| <span data-ttu-id="e49d6-113">32</span><span class="sxs-lookup"><span data-stu-id="e49d6-113">32</span></span>                          | <span data-ttu-id="e49d6-114">128x128</span><span class="sxs-lookup"><span data-stu-id="e49d6-114">128x128</span></span>                       |
| <span data-ttu-id="e49d6-115">64</span><span class="sxs-lookup"><span data-stu-id="e49d6-115">64</span></span>                          | <span data-ttu-id="e49d6-116">128x64</span><span class="sxs-lookup"><span data-stu-id="e49d6-116">128x64</span></span>                        |
| <span data-ttu-id="e49d6-117">128</span><span class="sxs-lookup"><span data-stu-id="e49d6-117">128</span></span>                         | <span data-ttu-id="e49d6-118">64x64</span><span class="sxs-lookup"><span data-stu-id="e49d6-118">64x64</span></span>                         |
| <span data-ttu-id="e49d6-119">BC1,4</span><span class="sxs-lookup"><span data-stu-id="e49d6-119">BC1,4</span></span>                       | <span data-ttu-id="e49d6-120">512x256</span><span class="sxs-lookup"><span data-stu-id="e49d6-120">512x256</span></span>                       |
| <span data-ttu-id="e49d6-121">BC2,3,5,6,7</span><span class="sxs-lookup"><span data-stu-id="e49d6-121">BC2,3,5,6,7</span></span>                 | <span data-ttu-id="e49d6-122">256x256</span><span class="sxs-lookup"><span data-stu-id="e49d6-122">256x256</span></span>                       |



 

<span data-ttu-id="e49d6-123">Число битов формата не поддерживается для мозаичных ресурсов: 96, форматы видео, формат DXGI \_ \_ R1 \_ UNORM, формат DXGI \_ \_ R8G8 \_ B8G8 \_ UNORM и DXGI \_ Format \_ R8R8 G8B8 UNORM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e49d6-123">Format bit counts not supported with tiled resources are 96 bpp formats, video formats, DXGI\_FORMAT\_R1\_UNORM, DXGI\_FORMAT\_R8G8\_B8G8\_UNORM, and DXGI\_FORMAT\_R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="e49d6-124">В этой таблице показано, как размещаются на плитках вложенные ресурсы [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) и [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) с множественной дискретизацией и различным числом выборок.</span><span class="sxs-lookup"><span data-stu-id="e49d6-124">This table shows how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources with various multisample counts are tiled.</span></span>



| <span data-ttu-id="e49d6-125">Число выборок</span><span class="sxs-lookup"><span data-stu-id="e49d6-125">Multisample Count</span></span>           | <span data-ttu-id="e49d6-126">Разделить размеры мозаики выше на (Вксх)</span><span class="sxs-lookup"><span data-stu-id="e49d6-126">Divide Tile Dimensions Above by (WxH)</span></span> |
|-----------------------------|-------------------------------|
| <span data-ttu-id="e49d6-127">1</span><span class="sxs-lookup"><span data-stu-id="e49d6-127">1</span></span>                           | <span data-ttu-id="e49d6-128">1x1</span><span class="sxs-lookup"><span data-stu-id="e49d6-128">1x1</span></span>                           |
| <span data-ttu-id="e49d6-129">2</span><span class="sxs-lookup"><span data-stu-id="e49d6-129">2</span></span>                           | <span data-ttu-id="e49d6-130">2x1</span><span class="sxs-lookup"><span data-stu-id="e49d6-130">2x1</span></span>                           |
| <span data-ttu-id="e49d6-131">4</span><span class="sxs-lookup"><span data-stu-id="e49d6-131">4</span></span>                           | <span data-ttu-id="e49d6-132">2x2</span><span class="sxs-lookup"><span data-stu-id="e49d6-132">2x2</span></span>                           |
| <span data-ttu-id="e49d6-133">8</span><span class="sxs-lookup"><span data-stu-id="e49d6-133">8</span></span>                           | <span data-ttu-id="e49d6-134">4x2</span><span class="sxs-lookup"><span data-stu-id="e49d6-134">4x2</span></span>                           |
| <span data-ttu-id="e49d6-135">16</span><span class="sxs-lookup"><span data-stu-id="e49d6-135">16</span></span>                          | <span data-ttu-id="e49d6-136">4x4</span><span class="sxs-lookup"><span data-stu-id="e49d6-136">4x4</span></span>                           |



 

<span data-ttu-id="e49d6-137">Для использования с мозаичным ресурсом необходимо использовать только счетчики выборки 1 и 4.</span><span class="sxs-lookup"><span data-stu-id="e49d6-137">Only sample counts 1 and 4 are required (and allowed) to be supported with tiled resources.</span></span> <span data-ttu-id="e49d6-138">В настоящее время мозаичные ресурсы не поддерживают 2, 8 и 16, даже если они показаны.</span><span class="sxs-lookup"><span data-stu-id="e49d6-138">Tiled resources don't currently support 2, 8, and 16 even though they are shown.</span></span>

<span data-ttu-id="e49d6-139">Реализации могут поддерживать 2, 8 и/или 16 образцов многовыборочного сглаживания (MSAA) для ресурсов без мозаичного заполнения, даже если они не поддерживаются мозаичным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="e49d6-139">Implementations can choose to support 2, 8, and/or 16 sample multisample antialiasing (MSAA) mode for non-tiled resources even though tiled resource don't support them.</span></span>

<span data-ttu-id="e49d6-140">Мозаичные ресурсы с количеством выборок больше 1 не могут использовать форматы в 128 бит/с.</span><span class="sxs-lookup"><span data-stu-id="e49d6-140">Tiled resources with sample counts larger than 1 can't use 128 bpp formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e49d6-141">См. также</span><span class="sxs-lookup"><span data-stu-id="e49d6-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e49d6-142">Мозаичное заполнение области мозаичного ресурса</span><span class="sxs-lookup"><span data-stu-id="e49d6-142">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 