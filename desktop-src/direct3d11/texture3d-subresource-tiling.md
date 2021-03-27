---
title: Размещение на плитках вложенного ресурса Texture3D
description: В этой таблице показано, как размещаются на плитках вложенные ресурсы Texture3D.
ms.assetid: D0CDD652-AE8E-40A4-BA05-E743B0757AFA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7a668f499a2f6d3911716d5d7bad60df4cd9e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997170"
---
# <a name="texture3d-subresource-tiling"></a><span data-ttu-id="6029d-103">Размещение на плитках вложенного ресурса Texture3D</span><span class="sxs-lookup"><span data-stu-id="6029d-103">Texture3D subresource tiling</span></span>

<span data-ttu-id="6029d-104">В этой таблице показано, как выполняется мозаичное заполнение подресурсов [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) .</span><span class="sxs-lookup"><span data-stu-id="6029d-104">This table shows how [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) subresources are tiled.</span></span> <span data-ttu-id="6029d-105">Значения в этой таблице не учитывают упаковку хвостовых MIP-карт.</span><span class="sxs-lookup"><span data-stu-id="6029d-105">The values in this table don't count tail mip packing.</span></span>

<span data-ttu-id="6029d-106">В этой таблице берется размещение на плитках [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d), размеры по осям X и Y делятся на 4 каждое, и добавляется 16 уровней глубины.</span><span class="sxs-lookup"><span data-stu-id="6029d-106">This table takes the [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) tiling and divides the x/y dimensions by 4 each and adds 16 layers of depth.</span></span> <span data-ttu-id="6029d-107">Все плитки для первой плоскости (двухмерной плоскости плиток, определяющих первые 16 слоев глубины) отображаются перед последующими плоскостями.</span><span class="sxs-lookup"><span data-stu-id="6029d-107">All the tiles for the first plane (2D plane of tiles defining the first 16 layers of depth) appear before the subsequent planes.</span></span>

> [!Note]  
> <span data-ttu-id="6029d-108">Поддержка [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) в мозаичных ресурсах не предоставляется в первоначальной реализации мозаичных ресурсов, но здесь перечислены нужные фигуры мозаики, так как поддержка может быть рассмотрена в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="6029d-108">[**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) support in tiled resources isn't exposed in the initial implementation of tiled resources, but the desired tile shapes are listed here because support might be consideration in a future release.</span></span>

 



| <span data-ttu-id="6029d-109">Бит/пкс (1 семпл/пкс)</span><span class="sxs-lookup"><span data-stu-id="6029d-109">Bits/Pixel (1 sample/pixel)</span></span> | <span data-ttu-id="6029d-110">Размеры плиток (пиксели, ШxВxГ)</span><span class="sxs-lookup"><span data-stu-id="6029d-110">Tile Dimensions (Pixels, WxHxD)</span></span> |
|-----------------------------|---------------------------------|
| <span data-ttu-id="6029d-111">8</span><span class="sxs-lookup"><span data-stu-id="6029d-111">8</span></span>                           | <span data-ttu-id="6029d-112">64x32x32</span><span class="sxs-lookup"><span data-stu-id="6029d-112">64x32x32</span></span>                        |
| <span data-ttu-id="6029d-113">16</span><span class="sxs-lookup"><span data-stu-id="6029d-113">16</span></span>                          | <span data-ttu-id="6029d-114">32x32x32</span><span class="sxs-lookup"><span data-stu-id="6029d-114">32x32x32</span></span>                        |
| <span data-ttu-id="6029d-115">32</span><span class="sxs-lookup"><span data-stu-id="6029d-115">32</span></span>                          | <span data-ttu-id="6029d-116">32x32x16</span><span class="sxs-lookup"><span data-stu-id="6029d-116">32x32x16</span></span>                        |
| <span data-ttu-id="6029d-117">64</span><span class="sxs-lookup"><span data-stu-id="6029d-117">64</span></span>                          | <span data-ttu-id="6029d-118">32x16x16</span><span class="sxs-lookup"><span data-stu-id="6029d-118">32x16x16</span></span>                        |
| <span data-ttu-id="6029d-119">128</span><span class="sxs-lookup"><span data-stu-id="6029d-119">128</span></span>                         | <span data-ttu-id="6029d-120">16x16x16</span><span class="sxs-lookup"><span data-stu-id="6029d-120">16x16x16</span></span>                        |
| <span data-ttu-id="6029d-121">BC1,4</span><span class="sxs-lookup"><span data-stu-id="6029d-121">BC1,4</span></span>                       | <span data-ttu-id="6029d-122">128x64x16</span><span class="sxs-lookup"><span data-stu-id="6029d-122">128x64x16</span></span>                       |
| <span data-ttu-id="6029d-123">BC2,3,5,6,7</span><span class="sxs-lookup"><span data-stu-id="6029d-123">BC2,3,5,6,7</span></span>                 | <span data-ttu-id="6029d-124">64x64x16</span><span class="sxs-lookup"><span data-stu-id="6029d-124">64x64x16</span></span>                        |



 

<span data-ttu-id="6029d-125">Число битов формата не поддерживается для мозаичных ресурсов: 96, форматы видео, формат DXGI \_ \_ R1 \_ UNORM, формат DXGI \_ \_ R8G8 \_ B8G8 \_ UNORM и DXGI \_ Format \_ R8R8 G8B8 UNORM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6029d-125">Format bit counts not supported with tiled resources are 96 bpp formats, video formats, DXGI\_FORMAT\_R1\_UNORM, DXGI\_FORMAT\_R8G8\_B8G8\_UNORM, and DXGI\_FORMAT\_R8R8\_G8B8\_UNORM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6029d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="6029d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6029d-127">Мозаичное заполнение области мозаичного ресурса</span><span class="sxs-lookup"><span data-stu-id="6029d-127">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 