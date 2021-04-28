---
description: '<span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>Метод Исингливентрекуест:: Рекуестасинк не используется.'
MS-HAID: vspixengine.ISingleEventRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IFrameEventsCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Исингливентрекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C85CAF18-6953-4C5D-9491-5F5A5F28C580
api_name:
- ISingleEventRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6365614d8a787ea4b252e04ae4e03c4e69ac2283
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107042"
---
# <a name="span-idvspixengineisingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspanisingleeventrequestrequestasync-method"></a><span data-ttu-id="26baf-103"><span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>Метод Исингливентрекуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="26baf-103"><span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>ISingleEventRequest::RequestAsync method</span></span>

<span data-ttu-id="26baf-104">Не используется.</span><span class="sxs-lookup"><span data-stu-id="26baf-104">Not used.</span></span>

## <a name="syntax"></a><span data-ttu-id="26baf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26baf-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  eventId,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IFrameEventsCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="26baf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="26baf-106">Parameters</span></span>

<span data-ttu-id="26baf-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="26baf-107">*eventId* </span></span>  
<span data-ttu-id="26baf-108">Не используется.</span><span class="sxs-lookup"><span data-stu-id="26baf-108">Not used.</span></span>

<span data-ttu-id="26baf-109">*нумколумнс* </span><span class="sxs-lookup"><span data-stu-id="26baf-109">*numColumns* </span></span>  
<span data-ttu-id="26baf-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="26baf-110">Not used.</span></span>

<span data-ttu-id="26baf-111">*count1 \_ столбцы* </span><span class="sxs-lookup"><span data-stu-id="26baf-111">*count1\_columns* </span></span>  
<span data-ttu-id="26baf-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="26baf-112">Not used.</span></span>

<span data-ttu-id="26baf-113">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="26baf-113">*requestCallback* </span></span>  
<span data-ttu-id="26baf-114">Не используется.</span><span class="sxs-lookup"><span data-stu-id="26baf-114">Not used.</span></span>

<span data-ttu-id="26baf-115">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="26baf-115">*requestCookie* </span></span>  
<span data-ttu-id="26baf-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="26baf-116">Not used.</span></span>

<span data-ttu-id="26baf-117">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="26baf-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="26baf-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="26baf-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="26baf-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26baf-119">Return value</span></span>

<span data-ttu-id="26baf-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="26baf-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26baf-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26baf-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="26baf-122">Требования</span><span class="sxs-lookup"><span data-stu-id="26baf-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="26baf-123">Header</span><span class="sxs-lookup"><span data-stu-id="26baf-123">Header</span></span></p></td><td><span data-ttu-id="26baf-124">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="26baf-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="26baf-125"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="26baf-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="26baf-126">**исингливентрекуест**</span><span class="sxs-lookup"><span data-stu-id="26baf-126">**ISingleEventRequest**</span></span>](/windows/desktop/direct3dtools/isingleeventrequest)

 

 
