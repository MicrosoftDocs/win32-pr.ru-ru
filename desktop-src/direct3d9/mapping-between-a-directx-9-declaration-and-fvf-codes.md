---
description: Эта таблица сопоставляет члены объявления D3DVERTEXELEMENT9 с кодом ФВФ.
ms.assetid: be4357b5-5b92-44ca-9100-ec9473930446
title: Сопоставление между объявлением Direct3D и кодами ФВФ (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4831af7b8c03ae4abd5ac2847351d2a6c921fb97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139971"
---
# <a name="mapping-between-a-direct3d-declaration-and-fvf-codes-direct3d-9"></a><span data-ttu-id="d9d53-103">Сопоставление между объявлением Direct3D и кодами ФВФ (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9d53-103">Mapping between a Direct3D Declaration and FVF Codes (Direct3D 9)</span></span>

<span data-ttu-id="d9d53-104">Эта таблица сопоставляет члены объявления [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) с кодом фвф.</span><span class="sxs-lookup"><span data-stu-id="d9d53-104">This table maps members of a [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) declaration to a FVF code.</span></span>



| <span data-ttu-id="d9d53-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d9d53-105">Data type</span></span>             | <span data-ttu-id="d9d53-106">Использование</span><span class="sxs-lookup"><span data-stu-id="d9d53-106">Usage</span></span>                      | <span data-ttu-id="d9d53-107">Индекс использования</span><span class="sxs-lookup"><span data-stu-id="d9d53-107">Usage index</span></span> | <span data-ttu-id="d9d53-108">фвф</span><span class="sxs-lookup"><span data-stu-id="d9d53-108">FVF</span></span>                       |
|-----------------------|----------------------------|-------------|---------------------------|
| <span data-ttu-id="d9d53-109">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="d9d53-109">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="d9d53-110">D3DDECLUSAGEное \_ расположение</span><span class="sxs-lookup"><span data-stu-id="d9d53-110">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="d9d53-111">0</span><span class="sxs-lookup"><span data-stu-id="d9d53-111">0</span></span>           | <span data-ttu-id="d9d53-112">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="d9d53-112">D3DFVF\_XYZ</span></span>               |
| <span data-ttu-id="d9d53-113">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="d9d53-113">D3DDECLTYPE\_FLOAT4</span></span>   | <span data-ttu-id="d9d53-114">D3DDECLUSAGE \_ позиций</span><span class="sxs-lookup"><span data-stu-id="d9d53-114">D3DDECLUSAGE\_POSITIONT</span></span>    | <span data-ttu-id="d9d53-115">0</span><span class="sxs-lookup"><span data-stu-id="d9d53-115">0</span></span>           | <span data-ttu-id="d9d53-116">D3DFVF \_ ксизрхв</span><span class="sxs-lookup"><span data-stu-id="d9d53-116">D3DFVF\_XYZRHW</span></span>            |
| <span data-ttu-id="d9d53-117">D3DDECLTYPE \_ флоатн</span><span class="sxs-lookup"><span data-stu-id="d9d53-117">D3DDECLTYPE\_FLOATn</span></span>   | <span data-ttu-id="d9d53-118">D3DDECLUSAGE \_ блендвеигхт</span><span class="sxs-lookup"><span data-stu-id="d9d53-118">D3DDECLUSAGE\_BLENDWEIGHT</span></span>  | <span data-ttu-id="d9d53-119">0</span><span class="sxs-lookup"><span data-stu-id="d9d53-119">0</span></span>           | <span data-ttu-id="d9d53-120">D3DFVF \_ ксизбн</span><span class="sxs-lookup"><span data-stu-id="d9d53-120">D3DFVF\_XYZBn</span></span>             |
| <span data-ttu-id="d9d53-121">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="d9d53-121">D3DDECLTYPE\_UBYTE4</span></span>   | <span data-ttu-id="d9d53-122">D3DDECLUSAGE \_ блендиндицес</span><span class="sxs-lookup"><span data-stu-id="d9d53-122">D3DDECLUSAGE\_BLENDINDICES</span></span> | <span data-ttu-id="d9d53-123">0</span><span class="sxs-lookup"><span data-stu-id="d9d53-123">0</span></span>           | <span data-ttu-id="d9d53-124">D3DFVF \_ ксизб (нвеигхтс + 1)</span><span class="sxs-lookup"><span data-stu-id="d9d53-124">D3DFVF\_XYZB (nWeights+1)</span></span> |
| <span data-ttu-id="d9d53-125">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="d9d53-125">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="d9d53-126">D3DDECLUSAGE, \_ Обычная</span><span class="sxs-lookup"><span data-stu-id="d9d53-126">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="d9d53-127">0</span><span class="sxs-lookup"><span data-stu-id="d9d53-127">0</span></span>           | <span data-ttu-id="d9d53-128">D3DFVF, \_ Обычная</span><span class="sxs-lookup"><span data-stu-id="d9d53-128">D3DFVF\_NORMAL</span></span>            |
| <span data-ttu-id="d9d53-129">D3DDECLTYPE \_ FLOAT1</span><span class="sxs-lookup"><span data-stu-id="d9d53-129">D3DDECLTYPE\_FLOAT1</span></span>   | <span data-ttu-id="d9d53-130">D3DDECLUSAGE \_ псизе</span><span class="sxs-lookup"><span data-stu-id="d9d53-130">D3DDECLUSAGE\_PSIZE</span></span>        | <span data-ttu-id="d9d53-131">0</span><span class="sxs-lookup"><span data-stu-id="d9d53-131">0</span></span>           | <span data-ttu-id="d9d53-132">D3DFVF \_ псизе</span><span class="sxs-lookup"><span data-stu-id="d9d53-132">D3DFVF\_PSIZE</span></span>             |
| <span data-ttu-id="d9d53-133">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="d9d53-133">D3DDECLTYPE\_D3DCOLOR</span></span> | <span data-ttu-id="d9d53-134">\_Цвет D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="d9d53-134">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="d9d53-135">0</span><span class="sxs-lookup"><span data-stu-id="d9d53-135">0</span></span>           | <span data-ttu-id="d9d53-136">D3DFVF \_ диффузный</span><span class="sxs-lookup"><span data-stu-id="d9d53-136">D3DFVF\_DIFFUSE</span></span>           |
| <span data-ttu-id="d9d53-137">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="d9d53-137">D3DDECLTYPE\_D3DCOLOR</span></span> | <span data-ttu-id="d9d53-138">\_Цвет D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="d9d53-138">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="d9d53-139">1</span><span class="sxs-lookup"><span data-stu-id="d9d53-139">1</span></span>           | <span data-ttu-id="d9d53-140">\_Зеркальное отражение D3DFVF</span><span class="sxs-lookup"><span data-stu-id="d9d53-140">D3DFVF\_SPECULAR</span></span>          |
| <span data-ttu-id="d9d53-141">D3DDECLTYPE \_ флоатм</span><span class="sxs-lookup"><span data-stu-id="d9d53-141">D3DDECLTYPE\_FLOATm</span></span>   | <span data-ttu-id="d9d53-142">D3DDECLUSAGE \_ текскурд</span><span class="sxs-lookup"><span data-stu-id="d9d53-142">D3DDECLUSAGE\_TEXCOORD</span></span>     | <span data-ttu-id="d9d53-143">n</span><span class="sxs-lookup"><span data-stu-id="d9d53-143">n</span></span>           | <span data-ttu-id="d9d53-144">D3DFVF \_ текскурдсизем (n)</span><span class="sxs-lookup"><span data-stu-id="d9d53-144">D3DFVF\_TEXCOORDSIZEm(n)</span></span>  |
| <span data-ttu-id="d9d53-145">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="d9d53-145">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="d9d53-146">D3DDECLUSAGEное \_ расположение</span><span class="sxs-lookup"><span data-stu-id="d9d53-146">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="d9d53-147">1</span><span class="sxs-lookup"><span data-stu-id="d9d53-147">1</span></span>           | <span data-ttu-id="d9d53-148">Недоступно</span><span class="sxs-lookup"><span data-stu-id="d9d53-148">N/A</span></span>                       |
| <span data-ttu-id="d9d53-149">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="d9d53-149">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="d9d53-150">D3DDECLUSAGE, \_ Обычная</span><span class="sxs-lookup"><span data-stu-id="d9d53-150">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="d9d53-151">1</span><span class="sxs-lookup"><span data-stu-id="d9d53-151">1</span></span>           | <span data-ttu-id="d9d53-152">Недоступно</span><span class="sxs-lookup"><span data-stu-id="d9d53-152">N/A</span></span>                       |



 

## <a name="related-topics"></a><span data-ttu-id="d9d53-153">См. также</span><span class="sxs-lookup"><span data-stu-id="d9d53-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9d53-154">Объявление вершины</span><span class="sxs-lookup"><span data-stu-id="d9d53-154">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 



