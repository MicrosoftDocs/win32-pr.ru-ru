---
description: Асинхронный запрос на получение изображений предварительного просмотра для окна "Этапы графического конвейера".
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestAsync\_EventID\_DWORD\_PipeLineStagesID\_arr\_DWORD\_DWORD\_IPipeLineStagesCallback\_ptr\_BOOL\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипипелинестажесрекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B725E541-EAC8-49DE-9EE7-C20698FE4A1F
api_name:
- IPipeLineStagesRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 89c67689668aa1c4227b33d861495c2504e5d626
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537541"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dwordspanipipelinestagesrequestrequestasync-method"></a><span data-ttu-id="67a55-103"><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>Метод Ипипелинестажесрекуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="67a55-103"><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>IPipeLineStagesRequest::RequestAsync method</span></span>

<span data-ttu-id="67a55-104">Асинхронный запрос на получение изображений предварительного просмотра для окна "Этапы графического конвейера".</span><span class="sxs-lookup"><span data-stu-id="67a55-104">An asynchronous request to get preview images for the graphics pipeline stages window.</span></span>

## <a name="syntax"></a><span data-ttu-id="67a55-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67a55-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   DWORD                     numStages,
   PipeLineStagesID []       count1_stageIds,
   DWORD                     width,
   DWORD                     height,
   IPipeLineStagesCallback * requestCallback,
   BOOL                      getMeshData,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="67a55-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="67a55-106">Parameters</span></span>

<span data-ttu-id="67a55-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="67a55-107">*eventID* </span></span>  
<span data-ttu-id="67a55-108">Идентификатор события графики, для которого запрашиваются изображения.</span><span class="sxs-lookup"><span data-stu-id="67a55-108">The ID of the graphics event that images are being requested for.</span></span>

<span data-ttu-id="67a55-109">*нумстажес* </span><span class="sxs-lookup"><span data-stu-id="67a55-109">*numStages* </span></span>  
<span data-ttu-id="67a55-110">Число стадий конвейера, для которых запрашиваются образы.</span><span class="sxs-lookup"><span data-stu-id="67a55-110">The number of pipeline stages that images are being requested for.</span></span>

<span data-ttu-id="67a55-111">*count1 \_ стажеидс* </span><span class="sxs-lookup"><span data-stu-id="67a55-111">*count1\_stageIds* </span></span>  
<span data-ttu-id="67a55-112">Идентификаторы этапов конвейера, для которых запрашиваются образы.</span><span class="sxs-lookup"><span data-stu-id="67a55-112">IDs of the pipeline stages that images are being requested for.</span></span>

<span data-ttu-id="67a55-113">*Ширина* </span><span class="sxs-lookup"><span data-stu-id="67a55-113">*width* </span></span>  
<span data-ttu-id="67a55-114">Ширина запрошенных изображений.</span><span class="sxs-lookup"><span data-stu-id="67a55-114">The width of the requested images.</span></span>

<span data-ttu-id="67a55-115">*равно* </span><span class="sxs-lookup"><span data-stu-id="67a55-115">*height* </span></span>  
<span data-ttu-id="67a55-116">Высота запрошенных изображений.</span><span class="sxs-lookup"><span data-stu-id="67a55-116">The height of the requested images.</span></span>

<span data-ttu-id="67a55-117">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="67a55-117">*requestCallback* </span></span>  
<span data-ttu-id="67a55-118">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="67a55-118">The address of the callback used to notify the host of results.</span></span>

<span data-ttu-id="67a55-119">*жетмешдата* </span><span class="sxs-lookup"><span data-stu-id="67a55-119">*getMeshData* </span></span>  
<span data-ttu-id="67a55-120">значение true, чтобы вернуть данные сетки; в противном случае — false.</span><span class="sxs-lookup"><span data-stu-id="67a55-120">true to return mesh data; otherwise false.</span></span>

<span data-ttu-id="67a55-121">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="67a55-121">*requestCookie* </span></span>  
<span data-ttu-id="67a55-122">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="67a55-122">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="67a55-123">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="67a55-123">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="67a55-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="67a55-124">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="67a55-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67a55-125">Return value</span></span>

<span data-ttu-id="67a55-126">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="67a55-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="67a55-127">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="67a55-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="67a55-128">Требования</span><span class="sxs-lookup"><span data-stu-id="67a55-128">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="67a55-129">Header</span><span class="sxs-lookup"><span data-stu-id="67a55-129">Header</span></span></p></td><td><span data-ttu-id="67a55-130">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="67a55-130">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="67a55-131"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="67a55-131"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="67a55-132">**ипипелинестажесрекуест**</span><span class="sxs-lookup"><span data-stu-id="67a55-132">**IPipeLineStagesRequest**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
