---
title: Плитки в буфере
description: Ресурс буфера разделен на плитки размером 64 КБ, причем в последней плитке имеется пустое пространство на случай, если размер не будет кратен 64 КБ.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fafa009e554499822c90c8fb6c0c8f34e47f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890708"
---
# <a name="buffer-tiling"></a><span data-ttu-id="d1e94-103">Плитки в буфере</span><span class="sxs-lookup"><span data-stu-id="d1e94-103">Buffer tiling</span></span>

<span data-ttu-id="d1e94-104">Ресурс [буфера](overviews-direct3d-11-resources-buffers.md) делится на 64 КБ, при этом некоторое пустое пространство на последнем плитке, если размер не КРАТЕН 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="d1e94-104">A [Buffer](overviews-direct3d-11-resources-buffers.md) resource is divided into 64KB tiles, with some empty space in the last tile if the size is not a multiple of 64KB.</span></span>

<span data-ttu-id="d1e94-105">Для разделения структурированных буферов на плитки буферы не должны иметь ограничений шага.</span><span class="sxs-lookup"><span data-stu-id="d1e94-105">Structured buffers must have no constraint on the stride to be tiled.</span></span> <span data-ttu-id="d1e94-106">Однако можно пожертвовать возможной оптимизацией производительности оборудования для использования объекта [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer), если все равно разделить буферы на плитки.</span><span class="sxs-lookup"><span data-stu-id="d1e94-106">But possible performance optimizations in hardware for using [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) can be sacrificed by making them tiled in the first place.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1e94-107">См. также</span><span class="sxs-lookup"><span data-stu-id="d1e94-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1e94-108">Мозаичное заполнение области мозаичного ресурса</span><span class="sxs-lookup"><span data-stu-id="d1e94-108">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 