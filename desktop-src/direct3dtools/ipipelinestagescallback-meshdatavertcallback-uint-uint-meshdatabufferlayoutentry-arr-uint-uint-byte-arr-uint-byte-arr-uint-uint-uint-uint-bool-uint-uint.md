---
description: Обратный вызов, уведомляющий узел о том, что данные сетки этапа конвейера возвращены запросом связана.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипипелинестажескаллбакк:: Мешдатаверткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E75EDE35-AC8E-4452-B79B-860C39B156F0
api_name:
- IPipeLineStagesCallback.MeshDataVertCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3c878851b0c3cfe32128d766f4dcb35a7437579d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537193"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span data-ttu-id="a3b73-103"><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>Метод Ипипелинестажескаллбакк:: Мешдатаверткаллбакк</span><span class="sxs-lookup"><span data-stu-id="a3b73-103"><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>IPipeLineStagesCallback::MeshDataVertCallback method</span></span>

<span data-ttu-id="a3b73-104">Обратный вызов, уведомляющий узел о том, что данные сетки этапа конвейера возвращены запросом связана.</span><span class="sxs-lookup"><span data-stu-id="a3b73-104">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3b73-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3b73-105">Syntax</span></span>


```C++
HRESULT MeshDataVertCallback(
   UINT                         numVertices,
   UINT                         numBufferLayoutEntries,
   MeshDataBufferLayoutEntry [] count1_entries,
   UINT                         stride,
   UINT                         numVBBytes,
   BYTE []                      count4_pVBData,
   UINT                         numIBBytes,
   BYTE []                      count6_pIBData,
   UINT                         indexSize,
   UINT                         IBOffset,
   UINT                         baseVertex,
   UINT                         minVertex,
   BOOL                         IBIndexesVB,
   UINT                         numIndices,
   UINT                         topology
);
```

## <a name="parameters"></a><span data-ttu-id="a3b73-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3b73-106">Parameters</span></span>

<span data-ttu-id="a3b73-107">*нумвертицес* </span><span class="sxs-lookup"><span data-stu-id="a3b73-107">*numVertices* </span></span>  
<span data-ttu-id="a3b73-108">Число вершин в результатах.</span><span class="sxs-lookup"><span data-stu-id="a3b73-108">The number of vertices in the results.</span></span>

<span data-ttu-id="a3b73-109">*нумбуфферлайаутентриес* </span><span class="sxs-lookup"><span data-stu-id="a3b73-109">*numBufferLayoutEntries* </span></span>  
<span data-ttu-id="a3b73-110">Число записей макета буфера в результатах.</span><span class="sxs-lookup"><span data-stu-id="a3b73-110">The number of buffer layout entries in the results.</span></span>

<span data-ttu-id="a3b73-111">*\_записи count1* </span><span class="sxs-lookup"><span data-stu-id="a3b73-111">*count1\_entries* </span></span>  
<span data-ttu-id="a3b73-112">Макет буфера целиком.</span><span class="sxs-lookup"><span data-stu-id="a3b73-112">The buffer layout entires.</span></span> <span data-ttu-id="a3b73-113">Они описывают выходную подпись шейдера.</span><span class="sxs-lookup"><span data-stu-id="a3b73-113">These describe the shader output signature.</span></span>

<span data-ttu-id="a3b73-114">*шага* </span><span class="sxs-lookup"><span data-stu-id="a3b73-114">*stride* </span></span>  
<span data-ttu-id="a3b73-115">Размер (STRIDE) всего выходного блока.</span><span class="sxs-lookup"><span data-stu-id="a3b73-115">The size (stride) of an entire output chunk.</span></span>

<span data-ttu-id="a3b73-116">*нумвббитес* </span><span class="sxs-lookup"><span data-stu-id="a3b73-116">*numVBBytes* </span></span>  
<span data-ttu-id="a3b73-117">Размер буфера вершин в байтах.</span><span class="sxs-lookup"><span data-stu-id="a3b73-117">The size of the vertex buffer in bytes.</span></span>

<span data-ttu-id="a3b73-118">*count4 \_ пвбдата* </span><span class="sxs-lookup"><span data-stu-id="a3b73-118">*count4\_pVBData* </span></span>  
<span data-ttu-id="a3b73-119">Буфер вершин.</span><span class="sxs-lookup"><span data-stu-id="a3b73-119">The vertex buffer.</span></span>

<span data-ttu-id="a3b73-120">*нумиббитес* </span><span class="sxs-lookup"><span data-stu-id="a3b73-120">*numIBBytes* </span></span>  
<span data-ttu-id="a3b73-121">Размер буфера индекса в байтах.</span><span class="sxs-lookup"><span data-stu-id="a3b73-121">The size of the index buffer in bytes.</span></span>

<span data-ttu-id="a3b73-122">*count6 \_ пибдата* </span><span class="sxs-lookup"><span data-stu-id="a3b73-122">*count6\_pIBData* </span></span>  
<span data-ttu-id="a3b73-123">Буфер индекса.</span><span class="sxs-lookup"><span data-stu-id="a3b73-123">The index buffer.</span></span>

<span data-ttu-id="a3b73-124">*indexSize* </span><span class="sxs-lookup"><span data-stu-id="a3b73-124">*indexSize* </span></span>  
<span data-ttu-id="a3b73-125">Размер каждого индекса в байтах.</span><span class="sxs-lookup"><span data-stu-id="a3b73-125">The size of each index in bytes.</span></span>

<span data-ttu-id="a3b73-126">*ибоффсет* </span><span class="sxs-lookup"><span data-stu-id="a3b73-126">*IBOffset* </span></span>  
<span data-ttu-id="a3b73-127">Смещение в буфере индекса, указывающее, где должны начинаться индексы.</span><span class="sxs-lookup"><span data-stu-id="a3b73-127">An offset into the index buffer that specifies where indices should start being used.</span></span>

<span data-ttu-id="a3b73-128">*басевертекс* </span><span class="sxs-lookup"><span data-stu-id="a3b73-128">*baseVertex* </span></span>  
<span data-ttu-id="a3b73-129">Смещение в буфере вершин, которое указывает, где следует начинать использовать вершины.</span><span class="sxs-lookup"><span data-stu-id="a3b73-129">An offset into the vertex buffer that specifies where vertices should start being used.</span></span>

<span data-ttu-id="a3b73-130">*минвертекс*</span><span class="sxs-lookup"><span data-stu-id="a3b73-130">*minVertex*</span></span>   

<span data-ttu-id="a3b73-131">*ибиндексесвб* </span><span class="sxs-lookup"><span data-stu-id="a3b73-131">*IBIndexesVB* </span></span>  
<span data-ttu-id="a3b73-132">значение true, если используется буфер индекса; в противном случае — false.</span><span class="sxs-lookup"><span data-stu-id="a3b73-132">true when the index buffer is used; otherwise false.</span></span>

<span data-ttu-id="a3b73-133">*нуминдицес* </span><span class="sxs-lookup"><span data-stu-id="a3b73-133">*numIndices* </span></span>  
<span data-ttu-id="a3b73-134">Количество используемых индексов.</span><span class="sxs-lookup"><span data-stu-id="a3b73-134">The number of indices used.</span></span>

<span data-ttu-id="a3b73-135">*Topology* </span><span class="sxs-lookup"><span data-stu-id="a3b73-135">*topology* </span></span>  
<span data-ttu-id="a3b73-136">Тополологи шейдера.</span><span class="sxs-lookup"><span data-stu-id="a3b73-136">The topolology of the shader.</span></span> <span data-ttu-id="a3b73-137">Это не обязательно то же самое, что и топология связанного вызова Draw.</span><span class="sxs-lookup"><span data-stu-id="a3b73-137">This is not necessarily the same as the topology of the associated draw call.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3b73-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3b73-138">Return value</span></span>

<span data-ttu-id="a3b73-139">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a3b73-139">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a3b73-140">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a3b73-140">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3b73-141">Требования</span><span class="sxs-lookup"><span data-stu-id="a3b73-141">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a3b73-142">Header</span><span class="sxs-lookup"><span data-stu-id="a3b73-142">Header</span></span></p></td><td><span data-ttu-id="a3b73-143">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="a3b73-143">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a3b73-144"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="a3b73-144"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a3b73-145">**ипипелинестажескаллбакк**</span><span class="sxs-lookup"><span data-stu-id="a3b73-145">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
