---
description: Асинхронный запрос на получение исходных файлов, связанных с стеком вызовов события.
MS-HAID: vspixengine.ISourceFileInfoRequest\_RequestAsync\_EventID\_ISourceFileInfoCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Исаурцефилеинфорекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 257361ED-7400-4320-8433-59A9A07E69E4
api_name:
- ISourceFileInfoRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba5fddf153b2a771ab54bf89036f8087ad0f7524
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710661"
---
# <a name="span-idvspixengineisourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dwordspanisourcefileinforequestrequestasync-method"></a><span data-ttu-id="d544d-103"><span id="vspixengine.isourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dword"></span>Метод Исаурцефилеинфорекуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="d544d-103"><span id="vspixengine.isourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dword"></span>ISourceFileInfoRequest::RequestAsync method</span></span>

<span data-ttu-id="d544d-104">Асинхронный запрос на получение исходных файлов, связанных с стеком вызовов события.</span><span class="sxs-lookup"><span data-stu-id="d544d-104">An asynchronous request to get the source files associated with the callstack of an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="d544d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d544d-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   ISourceFileInfoCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="d544d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d544d-106">Parameters</span></span>

<span data-ttu-id="d544d-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="d544d-107">*eventID* </span></span>  
<span data-ttu-id="d544d-108">Указанное событие.</span><span class="sxs-lookup"><span data-stu-id="d544d-108">The specified event.</span></span>

<span data-ttu-id="d544d-109">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="d544d-109">*requestCallback* </span></span>  
<span data-ttu-id="d544d-110">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="d544d-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="d544d-111">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="d544d-111">*requestCookie* </span></span>  
<span data-ttu-id="d544d-112">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="d544d-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="d544d-113">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="d544d-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="d544d-114">Не используется.</span><span class="sxs-lookup"><span data-stu-id="d544d-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="d544d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d544d-115">Return value</span></span>

<span data-ttu-id="d544d-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d544d-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d544d-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d544d-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d544d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d544d-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d544d-119">Header</span><span class="sxs-lookup"><span data-stu-id="d544d-119">Header</span></span></p></td><td><span data-ttu-id="d544d-120">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="d544d-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d544d-121"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="d544d-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d544d-122">**исаурцефилеинфорекуест**</span><span class="sxs-lookup"><span data-stu-id="d544d-122">**ISourceFileInfoRequest**</span></span>](/windows/desktop/direct3dtools/isourcefileinforequest)

 

 
