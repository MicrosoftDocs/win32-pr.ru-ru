---
description: Другие константы Direct3D
ms.assetid: 3e314f73-2653-481a-ac7d-1ce7db0591e2
title: Другие константы Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da78bf4ca08c8e1e2a09608a1a446d24e5846fb7
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342779"
---
# <a name="other-direct3d-constants"></a><span data-ttu-id="3c6a0-103">Другие константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="3c6a0-103">Other Direct3D Constants</span></span>

## <a name="sdk-version"></a><span data-ttu-id="3c6a0-104">Версия пакета SDK</span><span class="sxs-lookup"><span data-stu-id="3c6a0-104">SDK Version</span></span>

|  <span data-ttu-id="3c6a0-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="3c6a0-105">\#define</span></span>                   |
|---------------------|
| <span data-ttu-id="3c6a0-106">\_Версия пакета SDK для D3D \_</span><span class="sxs-lookup"><span data-stu-id="3c6a0-106">D3D\_SDK\_VERSION</span></span>   |
| <span data-ttu-id="3c6a0-107">\_Версия пакета SDK D3D9b \_</span><span class="sxs-lookup"><span data-stu-id="3c6a0-107">D3D9b\_SDK\_VERSION</span></span> |



 

<span data-ttu-id="3c6a0-108">Эти \# определения объявляются в d3d9. h.</span><span class="sxs-lookup"><span data-stu-id="3c6a0-108">These \#defines are declared in d3d9.h.</span></span>

## <a name="other-constants"></a><span data-ttu-id="3c6a0-109">Другие константы</span><span class="sxs-lookup"><span data-stu-id="3c6a0-109">Other Constants</span></span>

<span data-ttu-id="3c6a0-110">В следующей таблице перечислены константы, которые используются внутри:</span><span class="sxs-lookup"><span data-stu-id="3c6a0-110">The following table lists constants that are used internally:</span></span>



| <span data-ttu-id="3c6a0-111">\#определенно</span><span class="sxs-lookup"><span data-stu-id="3c6a0-111">\#define</span></span>                              | <span data-ttu-id="3c6a0-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3c6a0-112">Value</span></span>                                             | <span data-ttu-id="3c6a0-113">Описание</span><span class="sxs-lookup"><span data-stu-id="3c6a0-113">Description</span></span>                                                        |
|---------------------------------------|---------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="3c6a0-114">\_Максимальное число \_ одновременных \_ рендертаржетс D3D</span><span class="sxs-lookup"><span data-stu-id="3c6a0-114">D3D\_MAX\_SIMULTANEOUS\_RENDERTARGETS</span></span> | <span data-ttu-id="3c6a0-115">4</span><span class="sxs-lookup"><span data-stu-id="3c6a0-115">4</span></span>                                                 | <span data-ttu-id="3c6a0-116">Максимальное число рендертаржетс.</span><span class="sxs-lookup"><span data-stu-id="3c6a0-116">The maximum number of rendertargets.</span></span>                               |
| <span data-ttu-id="3c6a0-117">D3DDMAPSAMPLER</span><span class="sxs-lookup"><span data-stu-id="3c6a0-117">D3DDMAPSAMPLER</span></span>                        | <span data-ttu-id="3c6a0-118">256</span><span class="sxs-lookup"><span data-stu-id="3c6a0-118">256</span></span>                                               | <span data-ttu-id="3c6a0-119">Максимальное число выборок карт смещения.</span><span class="sxs-lookup"><span data-stu-id="3c6a0-119">The maximum number of displacement map samples.</span></span>                    |
| <span data-ttu-id="3c6a0-120">D3DDP \_ макстекскурд</span><span class="sxs-lookup"><span data-stu-id="3c6a0-120">D3DDP\_MAXTEXCOORD</span></span>                    | <span data-ttu-id="3c6a0-121">8</span><span class="sxs-lookup"><span data-stu-id="3c6a0-121">8</span></span>                                                 | <span data-ttu-id="3c6a0-122">Максимальное число координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="3c6a0-122">The maximum number of texture coordinates.</span></span>                         |
| <span data-ttu-id="3c6a0-123">MAXD3DDECLLENGTH</span><span class="sxs-lookup"><span data-stu-id="3c6a0-123">MAXD3DDECLLENGTH</span></span>                      | <span data-ttu-id="3c6a0-124">64 (не включает элемент вершины маркера "End")</span><span class="sxs-lookup"><span data-stu-id="3c6a0-124">64 (does not include "end" marker vertex element)</span></span> | <span data-ttu-id="3c6a0-125">Максимальное число элементов в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="3c6a0-125">Maximum number of elements in a vertex declaration.</span></span>                |
| <span data-ttu-id="3c6a0-126">MAXD3DDECLUSAGEINDEX</span><span class="sxs-lookup"><span data-stu-id="3c6a0-126">MAXD3DDECLUSAGEINDEX</span></span>                  | <span data-ttu-id="3c6a0-127">15</span><span class="sxs-lookup"><span data-stu-id="3c6a0-127">15</span></span>                                                | <span data-ttu-id="3c6a0-128">Максимальный индекс (0-15), который можно использовать в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="3c6a0-128">The maximum index (0-15) that can be used in a vertex declaration.</span></span> |



 

<span data-ttu-id="3c6a0-129">Эти \# определения объявляются в d3d9types. h.</span><span class="sxs-lookup"><span data-stu-id="3c6a0-129">These \#defines are declared in d3d9types.h.</span></span>

## <a name="constant-information"></a><span data-ttu-id="3c6a0-130">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="3c6a0-130">Constant Information</span></span>



| <span data-ttu-id="3c6a0-131">Требование</span><span class="sxs-lookup"><span data-stu-id="3c6a0-131">Requirement</span></span>                         | <span data-ttu-id="3c6a0-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3c6a0-132">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="3c6a0-133">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="3c6a0-133">Minimum operating system</span></span> | <span data-ttu-id="3c6a0-134">Windows 98</span><span class="sxs-lookup"><span data-stu-id="3c6a0-134">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3c6a0-135">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3c6a0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c6a0-136">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="3c6a0-136">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



