---
description: Другие константы Direct3D
ms.assetid: 3e314f73-2653-481a-ac7d-1ce7db0591e2
title: Другие константы Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990dc0a2ef06850fb9fc0839fd7a0be361832d65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710687"
---
# <a name="other-direct3d-constants"></a><span data-ttu-id="d0e1c-103">Другие константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="d0e1c-103">Other Direct3D Constants</span></span>

## <a name="sdk-version"></a><span data-ttu-id="d0e1c-104">Версия пакета SDK</span><span class="sxs-lookup"><span data-stu-id="d0e1c-104">SDK Version</span></span>



|                     |
|---------------------|
| <span data-ttu-id="d0e1c-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="d0e1c-105">\#define</span></span>            |
| <span data-ttu-id="d0e1c-106">\_Версия пакета SDK для D3D \_</span><span class="sxs-lookup"><span data-stu-id="d0e1c-106">D3D\_SDK\_VERSION</span></span>   |
| <span data-ttu-id="d0e1c-107">\_Версия пакета SDK D3D9b \_</span><span class="sxs-lookup"><span data-stu-id="d0e1c-107">D3D9b\_SDK\_VERSION</span></span> |



 

<span data-ttu-id="d0e1c-108">Эти \# определения объявляются в d3d9. h.</span><span class="sxs-lookup"><span data-stu-id="d0e1c-108">These \#defines are declared in d3d9.h.</span></span>

## <a name="other-constants"></a><span data-ttu-id="d0e1c-109">Другие константы</span><span class="sxs-lookup"><span data-stu-id="d0e1c-109">Other Constants</span></span>

<span data-ttu-id="d0e1c-110">В следующей таблице перечислены константы, которые используются внутри:</span><span class="sxs-lookup"><span data-stu-id="d0e1c-110">The following table lists constants that are used internally:</span></span>



|                                       |                                                   |                                                                    |
|---------------------------------------|---------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d0e1c-111">\#определенно</span><span class="sxs-lookup"><span data-stu-id="d0e1c-111">\#define</span></span>                              | <span data-ttu-id="d0e1c-112">Значение</span><span class="sxs-lookup"><span data-stu-id="d0e1c-112">Value</span></span>                                             | <span data-ttu-id="d0e1c-113">Описание</span><span class="sxs-lookup"><span data-stu-id="d0e1c-113">Description</span></span>                                                        |
| <span data-ttu-id="d0e1c-114">\_Максимальное число \_ одновременных \_ рендертаржетс D3D</span><span class="sxs-lookup"><span data-stu-id="d0e1c-114">D3D\_MAX\_SIMULTANEOUS\_RENDERTARGETS</span></span> | <span data-ttu-id="d0e1c-115">4</span><span class="sxs-lookup"><span data-stu-id="d0e1c-115">4</span></span>                                                 | <span data-ttu-id="d0e1c-116">Максимальное число рендертаржетс.</span><span class="sxs-lookup"><span data-stu-id="d0e1c-116">The maximum number of rendertargets.</span></span>                               |
| <span data-ttu-id="d0e1c-117">D3DDMAPSAMPLER</span><span class="sxs-lookup"><span data-stu-id="d0e1c-117">D3DDMAPSAMPLER</span></span>                        | <span data-ttu-id="d0e1c-118">256</span><span class="sxs-lookup"><span data-stu-id="d0e1c-118">256</span></span>                                               | <span data-ttu-id="d0e1c-119">Максимальное число выборок карт смещения.</span><span class="sxs-lookup"><span data-stu-id="d0e1c-119">The maximum number of displacement map samples.</span></span>                    |
| <span data-ttu-id="d0e1c-120">D3DDP \_ макстекскурд</span><span class="sxs-lookup"><span data-stu-id="d0e1c-120">D3DDP\_MAXTEXCOORD</span></span>                    | <span data-ttu-id="d0e1c-121">8</span><span class="sxs-lookup"><span data-stu-id="d0e1c-121">8</span></span>                                                 | <span data-ttu-id="d0e1c-122">Максимальное число координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="d0e1c-122">The maximum number of texture coordinates.</span></span>                         |
| <span data-ttu-id="d0e1c-123">MAXD3DDECLLENGTH</span><span class="sxs-lookup"><span data-stu-id="d0e1c-123">MAXD3DDECLLENGTH</span></span>                      | <span data-ttu-id="d0e1c-124">64 (не включает элемент вершины маркера "End")</span><span class="sxs-lookup"><span data-stu-id="d0e1c-124">64 (does not include "end" marker vertex element)</span></span> | <span data-ttu-id="d0e1c-125">Максимальное число элементов в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="d0e1c-125">Maximum number of elements in a vertex declaration.</span></span>                |
| <span data-ttu-id="d0e1c-126">MAXD3DDECLUSAGEINDEX</span><span class="sxs-lookup"><span data-stu-id="d0e1c-126">MAXD3DDECLUSAGEINDEX</span></span>                  | <span data-ttu-id="d0e1c-127">15</span><span class="sxs-lookup"><span data-stu-id="d0e1c-127">15</span></span>                                                | <span data-ttu-id="d0e1c-128">Максимальный индекс (0-15), который можно использовать в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="d0e1c-128">The maximum index (0-15) that can be used in a vertex declaration.</span></span> |



 

<span data-ttu-id="d0e1c-129">Эти \# определения объявляются в d3d9types. h.</span><span class="sxs-lookup"><span data-stu-id="d0e1c-129">These \#defines are declared in d3d9types.h.</span></span>

## <a name="constant-information"></a><span data-ttu-id="d0e1c-130">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="d0e1c-130">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="d0e1c-131">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="d0e1c-131">Minimum operating system</span></span> | <span data-ttu-id="d0e1c-132">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d0e1c-132">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d0e1c-133">См. также</span><span class="sxs-lookup"><span data-stu-id="d0e1c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0e1c-134">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="d0e1c-134">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



