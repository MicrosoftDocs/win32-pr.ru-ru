---
description: Запрашивает буфера кадров выход указанного целевого объекта отрисовки, события и кадра.
MS-HAID: vspixengine.IFrameBufferRequest\_RequestAsync\_DWORD\_EventID\_DWORD\_IFrameBufferCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифрамебуфферрекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 93E9BDFE-3913-4242-A973-7C113B6663FB
api_name:
- IFrameBufferRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 35c50b78486f25051e14ce2811382875e1fab240
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710617"
---
# <a name="span-idvspixengineiframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dwordspaniframebufferrequestrequestasync-method"></a><span data-ttu-id="15df6-103"><span id="vspixengine.iframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dword"></span>Метод Ифрамебуфферрекуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="15df6-103"><span id="vspixengine.iframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dword"></span>IFrameBufferRequest::RequestAsync method</span></span>

<span data-ttu-id="15df6-104">Запрашивает буфера кадров выход указанного целевого объекта отрисовки, события и кадра.</span><span class="sxs-lookup"><span data-stu-id="15df6-104">Requests framebuffer output of the specified render target, event, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="15df6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15df6-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   EventID                eventID,
   DWORD                  renderTargetIndex,
   IFrameBufferCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="15df6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="15df6-106">Parameters</span></span>

<span data-ttu-id="15df6-107">*фраменумбер* </span><span class="sxs-lookup"><span data-stu-id="15df6-107">*frameNumber* </span></span>  
<span data-ttu-id="15df6-108">Указанный кадр.</span><span class="sxs-lookup"><span data-stu-id="15df6-108">The specified frame.</span></span>

<span data-ttu-id="15df6-109">*1008* </span><span class="sxs-lookup"><span data-stu-id="15df6-109">*eventID* </span></span>  
<span data-ttu-id="15df6-110">Указанное событие.</span><span class="sxs-lookup"><span data-stu-id="15df6-110">The specified event.</span></span>

<span data-ttu-id="15df6-111">*рендертаржетиндекс* </span><span class="sxs-lookup"><span data-stu-id="15df6-111">*renderTargetIndex* </span></span>  
<span data-ttu-id="15df6-112">Индекс указанного целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="15df6-112">The index of the specified render target.</span></span>

<span data-ttu-id="15df6-113">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="15df6-113">*requestCallback* </span></span>  
<span data-ttu-id="15df6-114">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="15df6-114">The address of a callback used to notify the host of results.</span></span>

<span data-ttu-id="15df6-115">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="15df6-115">*requestCookie* </span></span>  
<span data-ttu-id="15df6-116">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="15df6-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="15df6-117">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="15df6-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="15df6-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="15df6-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="15df6-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15df6-119">Return value</span></span>

<span data-ttu-id="15df6-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="15df6-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="15df6-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="15df6-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="15df6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="15df6-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="15df6-123">Header</span><span class="sxs-lookup"><span data-stu-id="15df6-123">Header</span></span></p></td><td><span data-ttu-id="15df6-124">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="15df6-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="15df6-125"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="15df6-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="15df6-126">**ифрамебуфферрекуест**</span><span class="sxs-lookup"><span data-stu-id="15df6-126">**IFrameBufferRequest**</span></span>](/windows/desktop/direct3dtools/iframebufferrequest)

 

 
