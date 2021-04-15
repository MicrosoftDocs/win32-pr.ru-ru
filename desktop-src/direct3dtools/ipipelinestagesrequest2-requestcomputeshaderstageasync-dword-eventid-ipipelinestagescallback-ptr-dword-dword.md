---
description: Асинхронный запрос, получающий, использовался ли этап шейдера вычислений для указанного фрейма и события.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderStageAsync\_DWORD\_EventID\_IPipeLineStagesCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPipeLineStagesRequest2:: Рекуесткомпутешадерстажеасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EC5695A6-70B5-4F7D-A235-974A0A59A44F
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderStageAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ec7fe36a35e73ae2d047be11a2d5cf72f65825f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495270"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderstageasync-method"></a><span data-ttu-id="d61d8-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>Метод IPipeLineStagesRequest2:: Рекуесткомпутешадерстажеасинк</span><span class="sxs-lookup"><span data-stu-id="d61d8-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest2::RequestComputeShaderStageAsync method</span></span>

<span data-ttu-id="d61d8-104">Асинхронный запрос, получающий, использовался ли этап шейдера вычислений для указанного фрейма и события.</span><span class="sxs-lookup"><span data-stu-id="d61d8-104">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="d61d8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d61d8-105">Syntax</span></span>


```C++
HRESULT RequestComputeShaderStageAsync(
   DWORD                     frameNumber,
   EventID                   eventID,
   IPipeLineStagesCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="d61d8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d61d8-106">Parameters</span></span>

<span data-ttu-id="d61d8-107">*фраменумбер* </span><span class="sxs-lookup"><span data-stu-id="d61d8-107">*frameNumber* </span></span>  
<span data-ttu-id="d61d8-108">Указанный кадр.</span><span class="sxs-lookup"><span data-stu-id="d61d8-108">The specified frame.</span></span>

<span data-ttu-id="d61d8-109">*1008* </span><span class="sxs-lookup"><span data-stu-id="d61d8-109">*eventID* </span></span>  
<span data-ttu-id="d61d8-110">Указанное событие.</span><span class="sxs-lookup"><span data-stu-id="d61d8-110">The specified event.</span></span>

<span data-ttu-id="d61d8-111">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="d61d8-111">*requestCallback* </span></span>  
<span data-ttu-id="d61d8-112">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="d61d8-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="d61d8-113">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="d61d8-113">*requestCookie* </span></span>  
<span data-ttu-id="d61d8-114">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="d61d8-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="d61d8-115">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="d61d8-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="d61d8-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="d61d8-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="d61d8-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d61d8-117">Return value</span></span>

<span data-ttu-id="d61d8-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d61d8-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d61d8-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d61d8-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d61d8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d61d8-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d61d8-121">Header</span><span class="sxs-lookup"><span data-stu-id="d61d8-121">Header</span></span></p></td><td><span data-ttu-id="d61d8-122">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="d61d8-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d61d8-123"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="d61d8-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d61d8-124">**IPipeLineStagesRequest2**</span><span class="sxs-lookup"><span data-stu-id="d61d8-124">**IPipeLineStagesRequest2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
