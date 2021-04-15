---
description: Не используется.
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
ms.openlocfilehash: 6e6c78a7402082e4ca5222038bd3f5bd63c3cf7b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537292"
---
# <a name="span-idvspixengineisingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspanisingleeventrequestrequestasync-method"></a><span data-ttu-id="bafee-103"><span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>Метод Исингливентрекуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="bafee-103"><span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>ISingleEventRequest::RequestAsync method</span></span>

<span data-ttu-id="bafee-104">Не используется.</span><span class="sxs-lookup"><span data-stu-id="bafee-104">Not used.</span></span>

## <a name="syntax"></a><span data-ttu-id="bafee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bafee-105">Syntax</span></span>


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

## <a name="parameters"></a><span data-ttu-id="bafee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bafee-106">Parameters</span></span>

<span data-ttu-id="bafee-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="bafee-107">*eventId* </span></span>  
<span data-ttu-id="bafee-108">Не используется.</span><span class="sxs-lookup"><span data-stu-id="bafee-108">Not used.</span></span>

<span data-ttu-id="bafee-109">*нумколумнс* </span><span class="sxs-lookup"><span data-stu-id="bafee-109">*numColumns* </span></span>  
<span data-ttu-id="bafee-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="bafee-110">Not used.</span></span>

<span data-ttu-id="bafee-111">*count1 \_ столбцы* </span><span class="sxs-lookup"><span data-stu-id="bafee-111">*count1\_columns* </span></span>  
<span data-ttu-id="bafee-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="bafee-112">Not used.</span></span>

<span data-ttu-id="bafee-113">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="bafee-113">*requestCallback* </span></span>  
<span data-ttu-id="bafee-114">Не используется.</span><span class="sxs-lookup"><span data-stu-id="bafee-114">Not used.</span></span>

<span data-ttu-id="bafee-115">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="bafee-115">*requestCookie* </span></span>  
<span data-ttu-id="bafee-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="bafee-116">Not used.</span></span>

<span data-ttu-id="bafee-117">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="bafee-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="bafee-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="bafee-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="bafee-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bafee-119">Return value</span></span>

<span data-ttu-id="bafee-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="bafee-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bafee-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bafee-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bafee-122">Требования</span><span class="sxs-lookup"><span data-stu-id="bafee-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="bafee-123">Header</span><span class="sxs-lookup"><span data-stu-id="bafee-123">Header</span></span></p></td><td><span data-ttu-id="bafee-124">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="bafee-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="bafee-125"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="bafee-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="bafee-126">**исингливентрекуест**</span><span class="sxs-lookup"><span data-stu-id="bafee-126">**ISingleEventRequest**</span></span>](/windows/desktop/direct3dtools/isingleeventrequest)

 

 
