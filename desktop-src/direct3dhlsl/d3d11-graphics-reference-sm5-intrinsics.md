---
title: Встроенные функции модели шейдеров 5
description: Модель шейдеров 5 реализует встроенные функции из модели шейдеров 4 и ниже (см. подставляемые функции (DirectX HLSL) для получения полного списка поддерживаемых функций), а также следующих новых функций.
ms.assetid: 6f91fb40-d6d0-459f-adf7-cff263d7d346
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0cd5976526f75b676a853ef7480d4e81e0e00a91
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412156"
---
# <a name="shader-model-5-intrinsic-functions"></a><span data-ttu-id="55475-103">Встроенные функции модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="55475-103">Shader Model 5 Intrinsic Functions</span></span>

<span data-ttu-id="55475-104">Модель шейдеров 5 реализует встроенные функции из модели шейдеров 4 и ниже (см. [**подставляемые функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) для получения полного списка поддерживаемых функций), а также следующие новые функции:</span><span class="sxs-lookup"><span data-stu-id="55475-104">Shader Model 5 implements the intrinsic functions from Shader Model 4 and below (see [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) for a complete list of supported functions), as well as the following new functions:</span></span>

-   [<span data-ttu-id="55475-105">**аллмеморибарриер**</span><span class="sxs-lookup"><span data-stu-id="55475-105">**AllMemoryBarrier**</span></span>](allmemorybarrier.md)
-   [<span data-ttu-id="55475-106">**аллмеморибарриервисграупсинк**</span><span class="sxs-lookup"><span data-stu-id="55475-106">**AllMemoryBarrierWithGroupSync**</span></span>](allmemorybarrierwithgroupsync.md)
-   [<span data-ttu-id="55475-107">**асдаубле**</span><span class="sxs-lookup"><span data-stu-id="55475-107">**asdouble**</span></span>](asdouble.md)
-   [<span data-ttu-id="55475-108">**асуинт**</span><span class="sxs-lookup"><span data-stu-id="55475-108">**asuint**</span></span>](asuint.md)
-   [<span data-ttu-id="55475-109">**каунтбитс**</span><span class="sxs-lookup"><span data-stu-id="55475-109">**countbits**</span></span>](countbits.md)
-   [<span data-ttu-id="55475-110">**DDX \_ грубая**</span><span class="sxs-lookup"><span data-stu-id="55475-110">**ddx\_coarse**</span></span>](ddx-coarse.md)
-   [<span data-ttu-id="55475-111">**ДДИ \_ грубое**</span><span class="sxs-lookup"><span data-stu-id="55475-111">**ddy\_coarse**</span></span>](ddy-coarse.md)
-   [<span data-ttu-id="55475-112">**девицемеморибарриер**</span><span class="sxs-lookup"><span data-stu-id="55475-112">**DeviceMemoryBarrier**</span></span>](devicememorybarrier.md)
-   [<span data-ttu-id="55475-113">**девицемеморибарриервисграупсинк**</span><span class="sxs-lookup"><span data-stu-id="55475-113">**DeviceMemoryBarrierWithGroupSync**</span></span>](devicememorybarrierwithgroupsync.md)
-   [<span data-ttu-id="55475-114">**евалуатеаттрибутеатцентроид**</span><span class="sxs-lookup"><span data-stu-id="55475-114">**EvaluateAttributeAtCentroid**</span></span>](evaluateattributeatcentroid.md)
-   [<span data-ttu-id="55475-115">**евалуатеаттрибутеатсампле**</span><span class="sxs-lookup"><span data-stu-id="55475-115">**EvaluateAttributeAtSample**</span></span>](evaluateattributeatsample.md)
-   [<span data-ttu-id="55475-116">**f16tof32**</span><span class="sxs-lookup"><span data-stu-id="55475-116">**f16tof32**</span></span>](f16tof32.md)
-   [<span data-ttu-id="55475-117">**f32tof16**</span><span class="sxs-lookup"><span data-stu-id="55475-117">**f32tof16**</span></span>](f32tof16.md)
-   [<span data-ttu-id="55475-118">**фирстбисигх**</span><span class="sxs-lookup"><span data-stu-id="55475-118">**firstbithigh**</span></span>](firstbithigh.md)
-   [<span data-ttu-id="55475-119">**фирстбитлов**</span><span class="sxs-lookup"><span data-stu-id="55475-119">**firstbitlow**</span></span>](firstbitlow.md)
-   [<span data-ttu-id="55475-120">**FMA**</span><span class="sxs-lookup"><span data-stu-id="55475-120">**fma**</span></span>](dx-graphics-hlsl-fma.md)
-   [<span data-ttu-id="55475-121">**граупмеморибарриер**</span><span class="sxs-lookup"><span data-stu-id="55475-121">**GroupMemoryBarrier**</span></span>](groupmemorybarrier.md)
-   [<span data-ttu-id="55475-122">**граупмеморибарриервисграупсинк**</span><span class="sxs-lookup"><span data-stu-id="55475-122">**GroupMemoryBarrierWithGroupSync**</span></span>](groupmemorybarrierwithgroupsync.md)
-   [<span data-ttu-id="55475-123">**интерлоккедадд**</span><span class="sxs-lookup"><span data-stu-id="55475-123">**InterlockedAdd**</span></span>](interlockedadd.md)
-   [<span data-ttu-id="55475-124">**интерлоккеданд**</span><span class="sxs-lookup"><span data-stu-id="55475-124">**InterlockedAnd**</span></span>](interlockedand.md)
-   [<span data-ttu-id="55475-125">**интерлоккедкомпариксчанже**</span><span class="sxs-lookup"><span data-stu-id="55475-125">**InterlockedCompareExchange**</span></span>](interlockedcompareexchange.md)
-   [<span data-ttu-id="55475-126">**интерлоккедкомпаресторе**</span><span class="sxs-lookup"><span data-stu-id="55475-126">**InterlockedCompareStore**</span></span>](interlockedcomparestore.md)
-   [<span data-ttu-id="55475-127">**интерлоккедексчанже**</span><span class="sxs-lookup"><span data-stu-id="55475-127">**InterlockedExchange**</span></span>](interlockedexchange.md)
-   [<span data-ttu-id="55475-128">**интерлоккедмакс**</span><span class="sxs-lookup"><span data-stu-id="55475-128">**InterlockedMax**</span></span>](interlockedmax.md)
-   [<span data-ttu-id="55475-129">**интерлоккедмин**</span><span class="sxs-lookup"><span data-stu-id="55475-129">**InterlockedMin**</span></span>](interlockedmin.md)
-   [<span data-ttu-id="55475-130">**Взаимоблокировка**</span><span class="sxs-lookup"><span data-stu-id="55475-130">**InterlockedOr**</span></span>](interlockedor.md)
-   [<span data-ttu-id="55475-131">**интерлоккедксор**</span><span class="sxs-lookup"><span data-stu-id="55475-131">**InterlockedXor**</span></span>](interlockedxor.md)
-   [<span data-ttu-id="55475-132">**msad4**</span><span class="sxs-lookup"><span data-stu-id="55475-132">**msad4**</span></span>](dx-graphics-hlsl-msad4.md)
-   [<span data-ttu-id="55475-133">**Process2DQuadTessFactorsAvg**</span><span class="sxs-lookup"><span data-stu-id="55475-133">**Process2DQuadTessFactorsAvg**</span></span>](process2dquadtessfactorsavg.md)
-   [<span data-ttu-id="55475-134">**Process2DQuadTessFactorsMax**</span><span class="sxs-lookup"><span data-stu-id="55475-134">**Process2DQuadTessFactorsMax**</span></span>](process2dquadtessfactorsmax.md)
-   [<span data-ttu-id="55475-135">**Process2DQuadTessFactorsMin**</span><span class="sxs-lookup"><span data-stu-id="55475-135">**Process2DQuadTessFactorsMin**</span></span>](process2dquadtessfactorsmin.md)
-   [<span data-ttu-id="55475-136">**процессисолинетессфакторс**</span><span class="sxs-lookup"><span data-stu-id="55475-136">**ProcessIsolineTessFactors**</span></span>](processisolinetessfactors.md)
-   [<span data-ttu-id="55475-137">**процесскуадтессфакторсавг**</span><span class="sxs-lookup"><span data-stu-id="55475-137">**ProcessQuadTessFactorsAvg**</span></span>](processquadtessfactorsavg.md)
-   [<span data-ttu-id="55475-138">**процесскуадтессфакторсмакс**</span><span class="sxs-lookup"><span data-stu-id="55475-138">**ProcessQuadTessFactorsMax**</span></span>](processquadtessfactorsmax.md)
-   [<span data-ttu-id="55475-139">**процесскуадтессфакторсмин**</span><span class="sxs-lookup"><span data-stu-id="55475-139">**ProcessQuadTessFactorsMin**</span></span>](processquadtessfactorsmin.md)
-   [<span data-ttu-id="55475-140">**процесстритессфакторсавг**</span><span class="sxs-lookup"><span data-stu-id="55475-140">**ProcessTriTessFactorsAvg**</span></span>](processtritessfactorsavg.md)
-   [<span data-ttu-id="55475-141">**процесстритессфакторсмакс**</span><span class="sxs-lookup"><span data-stu-id="55475-141">**ProcessTriTessFactorsMax**</span></span>](processtritessfactorsmax.md)
-   [<span data-ttu-id="55475-142">**процесстритессфакторсмин**</span><span class="sxs-lookup"><span data-stu-id="55475-142">**ProcessTriTessFactorsMin**</span></span>](processtritessfactorsmin.md)
-   [<span data-ttu-id="55475-143">**rcp**</span><span class="sxs-lookup"><span data-stu-id="55475-143">**rcp**</span></span>](rcp.md)
-   [<span data-ttu-id="55475-144">**реверсебитс**</span><span class="sxs-lookup"><span data-stu-id="55475-144">**reversebits**</span></span>](reversebits.md)

## <a name="related-topics"></a><span data-ttu-id="55475-145">См. также</span><span class="sxs-lookup"><span data-stu-id="55475-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55475-146">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="55475-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




