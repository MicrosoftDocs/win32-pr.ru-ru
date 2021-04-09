---
description: Асинхронный запрос на получение указанных сведений об отдельном указанном кадре.
MS-HAID: vspixengine.IFrameEventsRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IFrameEventsCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифрамивентсрекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 821E7674-A960-46F6-A7AF-386298902ED6
api_name:
- IFrameEventsRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a001f6a29d17806271ca4f5d29dc80d6e36251bf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139647"
---
# <a name="span-idvspixengineiframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspaniframeeventsrequestrequestasync-method"></a><span data-ttu-id="fb29b-103"><span id="vspixengine.iframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>Метод Ифрамивентсрекуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="fb29b-103"><span id="vspixengine.iframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>IFrameEventsRequest::RequestAsync method</span></span>

<span data-ttu-id="fb29b-104">Асинхронный запрос на получение указанных сведений об отдельном указанном кадре.</span><span class="sxs-lookup"><span data-stu-id="fb29b-104">An asynchronous request to get specified information about a single specified frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb29b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb29b-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IFrameEventsCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="fb29b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb29b-106">Parameters</span></span>

<span data-ttu-id="fb29b-107">*фраменумбер* </span><span class="sxs-lookup"><span data-stu-id="fb29b-107">*frameNumber* </span></span>  
<span data-ttu-id="fb29b-108">Указанный кадр.</span><span class="sxs-lookup"><span data-stu-id="fb29b-108">The specified frame.</span></span>

<span data-ttu-id="fb29b-109">*нумколумнс* </span><span class="sxs-lookup"><span data-stu-id="fb29b-109">*numColumns* </span></span>  
<span data-ttu-id="fb29b-110">Указанные столбцы (поля).</span><span class="sxs-lookup"><span data-stu-id="fb29b-110">The specified columns (fields).</span></span>

<span data-ttu-id="fb29b-111">*count1 \_ столбцы* </span><span class="sxs-lookup"><span data-stu-id="fb29b-111">*count1\_columns* </span></span>  
<span data-ttu-id="fb29b-112">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="fb29b-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="fb29b-113">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="fb29b-113">*requestCallback* </span></span>  
<span data-ttu-id="fb29b-114">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="fb29b-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="fb29b-115">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="fb29b-115">*requestCookie* </span></span>  
<span data-ttu-id="fb29b-116">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="fb29b-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="fb29b-117">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="fb29b-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="fb29b-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="fb29b-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb29b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb29b-119">Return value</span></span>

<span data-ttu-id="fb29b-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="fb29b-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fb29b-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fb29b-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb29b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fb29b-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fb29b-123">Header</span><span class="sxs-lookup"><span data-stu-id="fb29b-123">Header</span></span></p></td><td><span data-ttu-id="fb29b-124">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="fb29b-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fb29b-125"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="fb29b-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fb29b-126">**ифрамивентсрекуест**</span><span class="sxs-lookup"><span data-stu-id="fb29b-126">**IFrameEventsRequest**</span></span>](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
