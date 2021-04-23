---
description: Асинхронный запрос на получение списка этапов, используемых для указанного фрейма и события.
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestSupportedStagesAsync\_DWORD\_EventID\_IPipeLineStagesCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипипелинестажесрекуест:: Рекуестсуппортедстажесасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C636FC40-0505-486B-B25D-9B424F5A584D
api_name:
- IPipeLineStagesRequest.RequestSupportedStagesAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0c3ebedee8dba4d7630d1bdff60bdaf479ea3561
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673093"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dwordspanipipelinestagesrequestrequestsupportedstagesasync-method"></a><span data-ttu-id="1d125-103"><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>Метод Ипипелинестажесрекуест:: Рекуестсуппортедстажесасинк</span><span class="sxs-lookup"><span data-stu-id="1d125-103"><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest::RequestSupportedStagesAsync method</span></span>

<span data-ttu-id="1d125-104">Асинхронный запрос на получение списка этапов, используемых для указанного фрейма и события.</span><span class="sxs-lookup"><span data-stu-id="1d125-104">An asynchronous request to get a list of stages used for the specified frame and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d125-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d125-105">Syntax</span></span>


```C++
HRESULT RequestSupportedStagesAsync(
   DWORD                     frameNumber,
   EventID                   eventID,
   IPipeLineStagesCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="1d125-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d125-106">Parameters</span></span>

<span data-ttu-id="1d125-107">*фраменумбер* </span><span class="sxs-lookup"><span data-stu-id="1d125-107">*frameNumber* </span></span>  
<span data-ttu-id="1d125-108">Указанный кадр.</span><span class="sxs-lookup"><span data-stu-id="1d125-108">The specified frame.</span></span>

<span data-ttu-id="1d125-109">*1008* </span><span class="sxs-lookup"><span data-stu-id="1d125-109">*eventID* </span></span>  
<span data-ttu-id="1d125-110">Указанное событие.</span><span class="sxs-lookup"><span data-stu-id="1d125-110">The specified event.</span></span>

<span data-ttu-id="1d125-111">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="1d125-111">*requestCallback* </span></span>  
<span data-ttu-id="1d125-112">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="1d125-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="1d125-113">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="1d125-113">*requestCookie* </span></span>  
<span data-ttu-id="1d125-114">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="1d125-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="1d125-115">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="1d125-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="1d125-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1d125-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d125-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d125-117">Return value</span></span>

<span data-ttu-id="1d125-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1d125-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1d125-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1d125-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d125-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1d125-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1d125-121">Header</span><span class="sxs-lookup"><span data-stu-id="1d125-121">Header</span></span></p></td><td><span data-ttu-id="1d125-122">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="1d125-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1d125-123"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="1d125-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1d125-124">**ипипелинестажесрекуест**</span><span class="sxs-lookup"><span data-stu-id="1d125-124">**IPipeLineStagesRequest**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
