---
description: Асинхронный запрос на получение данных шейдера вычислений для указанной диспетчеризации.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderDataAsync\_EventID\_IPipeLineStagesCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPipeLineStagesRequest2:: Рекуесткомпутешадердатаасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F73EA7B4-9E20-4BFD-8F87-20CE0B6C96D8
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderDataAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cf0d4725d8d2172900a96e58b4c8786ca2a9c851
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710659"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderdataasync-method"></a><span data-ttu-id="2e672-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>Метод IPipeLineStagesRequest2:: Рекуесткомпутешадердатаасинк</span><span class="sxs-lookup"><span data-stu-id="2e672-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>IPipeLineStagesRequest2::RequestComputeShaderDataAsync method</span></span>

<span data-ttu-id="2e672-104">Асинхронный запрос на получение данных шейдера вычислений для указанной диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="2e672-104">An asynchronous request to get compute shader data for the specified dispatch.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e672-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e672-105">Syntax</span></span>


```C++
HRESULT RequestComputeShaderDataAsync(
   EventID                    eventID,
   IPipeLineStagesCallback2 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="2e672-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e672-106">Parameters</span></span>

<span data-ttu-id="2e672-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="2e672-107">*eventID* </span></span>  
<span data-ttu-id="2e672-108">Указанное событие диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="2e672-108">The specified dispatch event.</span></span>

<span data-ttu-id="2e672-109">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="2e672-109">*requestCallback* </span></span>  
<span data-ttu-id="2e672-110">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="2e672-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="2e672-111">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="2e672-111">*requestCookie* </span></span>  
<span data-ttu-id="2e672-112">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="2e672-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="2e672-113">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="2e672-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="2e672-114">Не используется.</span><span class="sxs-lookup"><span data-stu-id="2e672-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e672-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e672-115">Return value</span></span>

<span data-ttu-id="2e672-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2e672-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e672-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e672-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e672-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2e672-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2e672-119">Header</span><span class="sxs-lookup"><span data-stu-id="2e672-119">Header</span></span></p></td><td><span data-ttu-id="2e672-120">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="2e672-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="2e672-121"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="2e672-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="2e672-122">**IPipeLineStagesRequest2**</span><span class="sxs-lookup"><span data-stu-id="2e672-122">**IPipeLineStagesRequest2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
